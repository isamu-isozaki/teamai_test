---
layout: markdown_page
title: "Distribution"
---

## On this page

- TOC
{:toc}

## Common links

* [Distribution team issue tracker][issue tracker]
* [Slack chat channel](https://gitlab.slack.com/archives/distribution)

## Mission

Distribution ensures the experience of installing and maintaining GitLab is easy and safe for everyone. It is Distribution team's task to think about the widest variety of installation/update use-cases and provide a solution that will satisfy most needs. Distribution is there to provide the best possible experience for a user that is a novice but also a veteran when it comes to installing and maintaining software.

## Vision

Distribution team vision is shown below, and not limited to:

### Technology

* GitLab has an official installation method on all major platforms and architectures.
* GitLab offers official one click installation method on all major cloud platforms.
* Part of official repositories for any Kubernetes package repository.
* GitLab.com is running using the official installation methods.
* GitLab runs on low resources systems such as Raspberry Pi.
* All GitLab features are installed and configured by default.
* GitLab is able to automatically upgrade itself.
* Installation interface to set up and configure GitLab.
* Any GitLab installation is able to report installation/upgrade errors automatically.
* Setting up GitLab in HA configuration is automated and simple.
* All installation methods are automatically tested before release.
* Most frequently used configuration options are tested using end-to-end integration tests.

### Team

* Team has official certifications for frequently used platforms.
* Each team member is able to work on all team projects.
* Team is able to reach a conclusion independently all the time, consensus most of the time.
* Each team member is a part of a hiring panel aimed to hire better than the best in the team.
* On-boarding and off-boarding is efficient.
* Career development paths are clear.
* Team creates a database of knowledge through documentation, training sessions and
outreach.

## Team responsibility

Distribution team is responsible for:

1. The [installation](/installation/), [update](/update/), and [upgrade](/upgrade/) pages.
1. The omnibus-gitlab installation package.
  * Installation using package is simple, quick, secure and protects the data integrity.
1. A cloud native installation method.
  * Installation using the Helm charts is able to scale easily with the increased demand.
1. Build and own the infrastructure used for creating the various installation methods.
  * Provision and maintain GitLab CI runners used for making above mentioned installation methods.
1. Ensure that GitLab can be installed for self-managed installations and GitLab.com.
1. [Maintaining infrastructure](#infrastructure-and-maintenance) used for work.
1. [Triaging issues](triage.html) in all owned [projects](#projects).
1. Creating [training sessions](training.html).

## Team objectives

Based on team responsibilities, the following objectives apply:

* Installation pages need to be complete, correct, easy, helpful, and attractive.
  Even if team's primary skill is not design and UX, team can maintain the pages
  with the help of teams that have this skill as their primary.
* The omnibus-gitlab installation package and the cloud native installation method
  should allow a beginner to install GitLab quickly, correctly and completely.
  Required configuration should be minimal, and it is
  Distribution team's responsibility to automate as much of this configuration as possible for the user.
* The omnibus-gitlab installation package and the cloud native installation method
  should be sufficiently configurable to allow an advanced user a way of setting up a more complex
  GitLab architecture.
* The above two goals might sound opposing, however they are not. A compromise can be made
  between these two goals without increasing the project maintenance cost for the Distribution team.
  We optimize for the best initial installation experience and then expand to further complexity.
* Distribution team has to verify each change that is introduced in each user facing project.
  This is done by creating feature and end-to-end integration tests. When a feature/fix cannot be tested easily
  with automated tests, confirm the change **manually**. If the person introducing the change
  is a Distribution team member, they are responsible and are required to sign off the change.
  Otherwise, it is the reviewers task to verify and sign off on the change.
* Distribution team welcomes any contribution to any of the projects. Ultimately, it is up to the team
  to decide if the contribution should be accepted. We need to weigh in on how the change affects
  the whole picture, not only what is shown in the diff. This is especially the case when a contribution is changing behaviour.
  If the change is a change in behaviour in one of the upstream components, we need to include team responsible for that component to submit their opinion.
  If we are responsible for certain functionality, we need to consider how the change impacts functionality in all use cases. Then, if the maintenance
  burden increases more than the change is worth or if it changes exiting functionality, we can consider rejecting the contribution.
* Nightly builds are installed on dev.gitlab.org using one of the official artifacts of Distribution team. Purpose of this exercise is to have a
  production level instance using the installation method that most of the rest of the community will be using.
* Triaging issue tracker is a task that allows us to keep on the pulse of the changes we make. By being in contact with users and customers,
  we can maintain visibility into most frequently reported bugs or requested features. Not everything reported will be resolved, however
  _all_ of the reports should be triaged. This also applies to mentions in GitLab CE/EE repositories on issues with `Distribution` label.
* Every Distribution team member is responsible for creating a training session for the rest of the team.
  See the page on [team training](training.html) for details.
* GitLab.com is last on this list, but is first in importance. When team that manages GitLab.com creates an issue, the item should
  be raised up directly to the team Engineering Manager and Product Manager. While these issues are important, we don't necessarily need
  to provide a complete solution right away, but we need to work with the other team on providing a path forward with their request.

### Projects

| Name | Location | Description |
| -------- | -------- |
| Omnibus GitLab | [gitlab-org/omnibus-gitlab](https://gitlab.com/gitlab-org/omnibus-gitlab) | Build Omnibus packages with HA support for LTS versions of all major Linux operating systems such as Ubuntu, Debian, CentOS/RHEL, OpenSUSE, SLES |
| Docker All in one GitLab image | [gitlab-org/omnibus-gitlab/docker](https://gitlab.com/gitlab-org/omnibus-gitlab/tree/master/docker) | Build Docker images for GitLab CE/EE based on the omnibus-gitlab package |
| GitLab Helm Chart | [charts/gitlab](https://gitlab.com/charts/gitlab) | Cloud Native GitLab Helm Charts |
| Docker images for GitLab Helm Chart | [gitlab-org/build/CNG](https://gitlab.com/gitlab-org/build/CNG) | Individual images used by GitLab Helm Charts |
| GitLab Helm Chart operator | [gitlab-org/distribution/gitlab-operator](https://gitlab.com/gitlab-org/distribution/gitlab-operator) | Support project for GitLab Helm Charts, performing various tasks such as zero downtime upgrade |
| Kubernetes Helm Charts index | [charts/charts.gitlab.io](https://gitlab.com/charts/charts.gitlab.io) | Helm charts repository index |
| AWS images | [AWS marketplace](https://aws.amazon.com/marketplace/pp/B071RFCJZK?qid=1493819387811&sr=0-1&ref_=srh_res_product_title) | AWS image based on the omnibus-gitlab package |
| Kubernetes helm charts | [Official Helm Charts](https://github.com/kubernetes/charts) | Application definitions for Kubernetes Helm based on the omnibus-gitlab package |
| GitLab provisioner | [gitlab-org/distribution/gitlab-provisioner](https://gitlab.com/gitlab-org/distribution/gitlab-provisioner) | Creates a GitLab HA installation using Ansible and Terraform |
| GitLab PCF tile | [gitlab.com/gitlab-pivotal](https://gitlab.com/gitlab-pivotal) | One click installation of GitLab in Pivotal Cloud Foundry based on the omnibus-gitlab package |
| GitLab Terraform configuration | [gitlab-terraform](https://gitlab.com/gitlab-terraform) | Terraform configuration for various cloud providers |
| Omnibus GitLab Builder | [GitLab Omnibus Builder](https://gitlab.com/gitlab-org/gitlab-omnibus-builder) | Create environment containing build dependencies for the omnibus-gitlab package |
| Upgrade time metrics | [Upgrade time metrics page on GL Pages](https://gitlab-org.gitlab.io/omnibus-gitlab/upgrade-metrics.html) | Stores the result of calculation of time needed for upgrade between versions in chart form. Backed by Google sheets. Hosted using GL Pages |

## Public by default

All work carried out by the Distribution team is public. Some exceptions apply:

* Work has possible security implications - If during the course of work security concerns are no longer valid, it is expected for this work to become public.
* Work is done with a third party - Only when a third party requests that the work is not public.
* Work has financial implications - Unless financial details can be omitted from the work.
* Work has legal implications - Unless legal details can be omitted from the work.

Some of the team work is carried out on our development server at `dev.gitlab.org`.
[Infrastructure overview document](https://docs.gitlab.com/omnibus/release/README.html#infrastructure) lists the reasons.

Unless your work is related to the security, all other work is carried out in projects on `GitLab.com`.
If you need to submit a sensitive issue, please use confidential issues.

If you are unsure whether something needs to remain private, check with the team Engineering Manager.

## Onboarding and offboarding

In addition to general company on-boarding and off-boarding, Distribution team
has its own process to get new team members up to speed more quickly.

If you are starting with your onboarding, open an issue in [Distribution team issue tracker][issue tracker], select `Team-onboarding` template and assign the issue to yourself.

Going through the steps noted in the issue should be your top priority, higher
than the general company on-boarding issue. This is because items in team on-boarding are specific to your role and it will allow you to get up-to-speed quicker.

Off-boarding should be carried out by the Engineering Manager of the team,
using the appropriate issue template in the same issue tracker.

## Work Resources

General resources available to developers are listed in the
[Engineering handbook](/handbook/engineering/#resources).

In the Distribution team specifically, everyone should have access to the `testground`
project on [Google Cloud Platform](https://console.cloud.google.com/). If you
don't have access, ask the team lead by creating issue in
[Distribution team issue tracker][issue tracker] and label it `Access Request`.

## Infrastructure and maintenance

As part of the team responsibilities, team owns maintenance of infrastructure
used for day to day work.
For list of nodes and description of the maintenance tasks, see the
[infastructure and maintenance](maintenance.html) page.

## How to work with Distribution

Everything that is done in GitLab will end up in the supported installation methods
that are distributed to users. While that sounds like the last link in the chain, it is one of the
most important ones. This means that informing the Distribution team of a change in an
early stage is crucial for releasing your feature. While last minute changes are
inevitable and can happen, we should strive to avoid them.

We expect every team to reach out to the Distribution team before scheduling a feature
in an upcoming release in the following cases:

* The change requires a new or an update on a gem with native extensions.
* The change requires a new or updated external software dependency.
  * Also when the external dependency has its own external dependencies.
* The change adds, modifies, or removes files that should be managed by
omnibus-gitlab. For example:
  * The change introduces new directories in the package.
  * The change introduces new files in previously not defined locations
* The change requires a new configuration file.
* The change requires a change in a previously established configuration.

To sum up the above list:

If you need to do `install`, `update`, `make`, `mkdir`, `mv`, `cp`, `chown`,
`chmod`, do compilation or configuration change in any part of GitLab stack, you
need to reach out to the Distribution team for opinion as early as possible.

This will allow us to schedule appropriately the changes (if any) we have to make
to the packages.

If a change is reported late in the release cycle or not reported at all,
your feature/change might not be shipped within the release.

If you have any doubt whether your change will have an impact on the Distribution team,
don't hesitate to ping us in your issue and we'll gladly help.

[issue tracker]: https://gitlab.com/gitlab-org/distribution/team-tasks
