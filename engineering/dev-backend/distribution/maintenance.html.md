---
layout: markdown_page
title: "Distribution Team Infrastructure and Maintenance"
---

## On this page

- TOC
{:toc}

## Common links

* [Distribution Team Handbook](/handbook/engineering/dev-backend/distribution/)

## Infrastructure

As part of the team tasks, team has responsibility towards the following nodes:

* dev.gitlab.org - Nightly GitLab CE package is installed on the node
* Build Machines
  * build-runners.gitlab.org
  * build-trigger-runner-manager.gitlab.org
  * omnibus-builder-runners-manager.gitlab.org
* packages.gitlab.com - No maintenance tasks, using as tool

Below we list more details on what the node is, how it is structured and
examples of what kind of maintenance tasks can be carried out.

### dev.gitlab.org

Every day at 1:30 UTC, a nightly build gets triggered on dev.gitlab.org. The cron trigger times are currently defined
at [the scheduled pipeline page on dev.gitlab.org](https://dev.gitlab.org/gitlab/omnibus-gitlab/pipeline_schedules).

Every day at 7:20 UTC, the nightly CE packages gets automatically deployed on dev.gitlab.org. Any errors in
the install process will be logged in [Sentry](https://sentry.gitlap.com/gitlab/devgitlaborg/). Slack notifications
will appear in #dev-gitlab.
The cron task is currently defined in [dev.gitlab.org role](https://dev.gitlab.org/cookbooks/chef-repo/blob/4f90a2061a8d1fa2a0c6d5aeb33499df14c040a3/job-families/dev-gitlab-org.json#L183-190).

#### Manually upgrading/downgrading packages

In case of an issue with the latest deploy, we might need to revert the installation to a previous nightly version and lock the deployment until the
fixes are ready. This is done to ensure stability of dev.gitlab.org for others using the instance.

To start, create an issue in a team-tasks [issue-tracker] detailing that
you will be downgrading installed version, and adding links to related issues.
Assign the issue to yourself.

Next, make an announcement in `#announcements` slack channel before
downgrading the package:

```
I will be manually downgrading package on dev.gitlab.org to <version> as latest nightly is not working as expected. <link to issue>
```

Stop sidekiq and unicorn to be sure that data doesn't get altered during the upgrade.

```bash
  sudo gitlab-ctl stop sidekiq
  sudo gitlab-ctl stop unicorn
```

Find the previous working version of the package and downgrade to this version:

```bash
  sudo apt-get install gitlab-ce=<version to be installed>
```

For example, if the version is `10.4.0+rnightly.75436.44501791-0`, you would run:

```bash
  sudo apt-get install gitlab-ce=10.4.0+rnightly.75436.44501791-0
```
This will automatically run reconfigure and apply the necessary changes.

Once the reconfigure is done, confirm all the services are up and running.

```bash
  sudo gitlab-ctl status
```

Confirm the correct version is deployed by visiting `https://dev.gitlab.org/help`.

Create a package hold to prevent auto-upgrade:

```bash
  sudo apt-mark hold gitlab-ce
```

and verify the hold is in place.

```bash
  sudo apt-mark showhold
```

Back in the `#announcements` channel, leave a message that the downgrade is completed:

```
Downgrade completed. The package has also been put on hold to prevent automatic upgrades. <link to issue>
```

Once the issue has been resolved, unhold the package and upgrade to the
latest version.

Start by announcing this in `#announcements` channel

```
I will be removing the package hold and manually upgrading package on dev.gitlab.org to the latest nightly. <link to issue>
```

Next, unhold the package:

```bash
  sudo apt-mark unhold gitlab-ce
```

Continue with upgrading:

```bash
  sudo apt-get update
  sudo apt-get install gitlab-ce
```

Once the upgrade is completed, verify that the latest version is installed
by visiting `https://dev.gitlab.org/help`.

Finally, leave a note at the `#announcements` channel

```
Upgrade completed. dev.gitlab.org now runs <version>.
```

#### Maintenance tasks

Requirements:

* Access to the node
* Depending on whether the task requires permanent changes to `/etc/gitlab/gitlab.rb`, access to the [Chef repo](https://dev.gitlab.org/cookbooks/chef-repo). If you do not have access to this repository, make sure
you create [an issue in Infrastructure issue tracker](https://gitlab.com/gitlab-com/infrastructure/issues/new?issue%5Bassignee_id%5D=&issue%5Bmilestone_id%5D=)
and label it `access request`.

Teams responsibility is to make sure that the GitLab instance on this server is operational.
The omnibus-gitlab package on this server is a stock package with required configuration to keep it operational.
Regular omnibus-gitlab commands can be used on this node.
If, for some reason, you need to apply a change to `/etc/gitlab/gitlab.rb`, this change
needs to be introduced in the [dev-gitlab-org role](https://dev.gitlab.org/cookbooks/chef-repo/blob/fa6131d9d06299940a72c51cf60ea62c54fe3461/job-families/dev-gitlab-org.json).

If you do not have access to this repository, but you need to do a hot-patch or configuration
testing, the following steps can be performed:

* Stop chef-client on this node: `sudo service chef-client stop`.
* Make the necessary change to get the instance running again. If that requires change in gitlab.rb file,
change it manually and run reconfigure.
* Reach out to Production team to get help on getting your `gitlab.rb` configuration
change committed to the Chef server.
* After this has been applied, start the chef-client on the node: `sudo service chef-client start`
* Make sure that any change you did is noted in an issue! It is your responsibility to revert the
change on this node once the fix is in place in the package!

#### Improvements

* [Deploy notifications](https://gitlab.com/gitlab-org/omnibus-gitlab/issues/2543)

### Build Machines

GitLab CI runner manager is responsible for creating build machines for package builds.
This node configuration is managed by [cookbook-gitlab-runner](https://gitlab.com/gitlab-cookbooks/cookbook-wrapper-gitlab-runner).
Configuration values are stored in the vault named the same as the node, [see example](https://dev.gitlab.org/cookbooks/chef-repo/blob/bb367e272662da9e9efdfd9adec13769e44a9bc3/job-families/omnibus-builder-runners-manager.json#L18).

Currently, the version of GitLab CI runner is locked. We aim to be close to the current version of runner in order
to get the fixes that we need without getting into issues that could cause a failure. These failures could prevent
the release from going out so be careful with unnecessary changes on these nodes.

For building official packages we use
`build-runners.gitlab.org` and (soon to be deprecated) `omnibus-builder-runners-manager.gitlab.org`.

For building packages on GitLab.com as part of trigger packages pipelines, we use
a manager machine at `build-trigger-runner-manager.gitlab.org`.

Both `build-runners.gitlab.org` and `build-trigger-runner-manager.gitlab.org` are
in GCP project `omnibus-build-runners`. Each of these managers are spawning machines
inside of GCP and are configured with `google` docker machine driver.

`build-runners.gitlab.org` is also configured with the `scaleway` driver,
which boots up machines in a Scaleway account for Raspberry Pi (arm platform) builds.
This same machine is configured to create `package-promotion` machines. These machines
are used only to upload packages so they are scaled down to save on costs.

`omnibus-builder-runners-manager.gitlab.org` is currently being used as a backup
and is configured with `digitalocean` docker machine driver and is booting up machines
inside of Digital Ocean.


#### Maintenance tasks

Requirements:

* Access to the node
* Access to a Chef Vault admin. At minimum, contact the Distribution Lead for help.

When the version of GitLab CI runner needs to be changed:

  * To be performed by a Chef Vault admin
    * In local clone of Chef Repo, they will need to run `bundle exec rake 'edit_role_secrets[<role name for build machine>]'`. This command
  will fetch the secrets from the chef vault and open up your text editor.
    * Change the version of the package listed in the `gitlab-ci-multi-runner` section.
    * After saving the change, there will be a lot of output which also includes deleting of some existing content in the chef vault. This is expected behaviour.
    * Commit.

  * To be performed by any team member:
    * Login to the node and run, `sudo /root/runner_upgrade.sh` to perform the upgrade. This will stop the chef-client service, stop the runner and cleanup the machines,
  run the chef-client to fetch the new version and finally, start gitlab runner again.

When you notice that the builds are pending on our dev.gitlab.org project, it is possible that
the number of failed machines is high. Failed machines prevent the runner manager from
starting up new machines and this can slow down or even block the release.
To resolve this:

  * Login to the [build machine](#build-machines) node
  * Enter the root session: `sudo su`. This is required because `docker-machine` command will list running machines
  for currently active user
  * Run `docker-machine ls`. This will print out the list of machines that are either in `Running`, `Error` or have an empty state.
  * To list only machines in `Error` state, you can use `/root/machines_operations.sh list-failing`
  * To safely clean the machines with `Error` state, run `/root/machines_operations.sh remove-failing`
  * If the machine has an empty state, you can always remove the machine manually or use `docker-machine ls | grep -v 'Running' | awk '{print $1}' | xargs docker-machine rm --force`.
  This line will remove all machines that do not have `Running` state.

### packages.gitlab.com

At this moment, Distribution team is only the user of packages.gitlab.com. Release packages
are served to our users and customers from our CI on `dev.gitlab.org`.

Given that the package server is currently deployed on our own infrastructure,
from an omnibus type package, if Production requires help the team should do a
best effort to help trough any issues.


[issue tracker]: https://gitlab.com/gitlab-org/distribution/team-tasks
