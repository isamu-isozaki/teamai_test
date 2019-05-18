---
layout: markdown_page
title: "Database"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Focus of Database Team

The Database team focuses on improving performance, reliability, and availability of GitLab and GitLab.com. This is done through a variety of different ways such as:

* Making application changes to improve the performance of database queries.
* Adding database monitoring capabilities in GitLab.
* Deploying pgbouncer to reduce the number of database connections that are necessary.
* Adjusting the settings of GitLab.com's PostgreSQL cluster for optimal performance.
* Building, testing, and maintaining a failover system for both GitLab.com and users of GitLab's High Availability features.
* Assisting other developers by answering database related questions and reviewing database related changes.
* Documenting tools, monitoring, and database best practices in order to share as much knowledge as possible.

For further details, see the [current vacancy for a Database Engineer](/job-families/engineering/database-engineer/).

## The First Month

During your first month at GitLab as a database engineer or specialist we expect you to get familiar with GitLab, set up a working environment, and work on a few simple issues. Available issues can be found in the issue boards mentioned below. If there are no issues available or you are not certain what to work on it's best to discuss this with your team members.

## After The First Month

After the first month (depending on how fast you get started this might take less than a month) we expect you to start focusing on work for a specific functional group. Currently the following groups are available:

* Discussion: everything related to issues, merge requests, labels, etc.
* CI/CD: everything related to GitLab CI, Kubernetes, Auto DevOps, etc.
* Platform: everything else.
* Production: everything related to the infrastructure that powers GitLab.com. This team is best suitable for those with a strong infrastructure / operations background.

Once you have chosen a functional group you will be primarily working on the issues related to that group, though you're of course more than welcome to also work on other issues. You will also be expected to help the members of those teams by helping them write better database queries, review merge requests, etc. Of course you don't have to do all of this at once, instead the team will help you ease into this process step by step.

You are free to switch groups at any time, though we prefer for this to be announced in the weekly database meeting so that everybody is aware of this. When doing so you should also inform the team leads of both the old and new team so they are aware of the change.

Note that when focusing on the work of a specific team you do not _report_ to that team's lead or manager, instead you still report to the database team.

## Common Links

To make it easier to find your way around you can find a list of useful or important links below.

### Monitoring & Performance Related Tools

As a database specialist the following tools can be very helpful:

* [Private Grafana](https://dashboards.gitlab.net/): for both application and system level performance data.
* [Performance Bar](https://docs.gitlab.com/ee/administration/monitoring/performance/performance_bar.html): type `pb` in GitLab and a bar with performance metrics will show up at the top of the page. This tool is especially useful for viewing the queries executed and their timings.
* [Sherlock](https://docs.gitlab.com/ee/development/profiling.html#sherlock): a tool similar to the performance bar but meant for development environments. Sherlock is able to show backtraces and the output of `EXPLAIN ANALYZE` for executed queries. Enable by starting Rails with `env ENABLE_SHERLOCK=1 bundle exec rails s`.
* <https://explain.depesz.com/> for visualizing the output of `EXPLAIN ANALYZE`.

### Dashboards

The following (private) Grafana dashboard are important / useful for database specialists:

* [PostgresSQL Overview](https://dashboards.gitlab.net/dashboard/db/postgresql-overview)
* [PostgresSQL Tuple Statistics](https://dashboards.gitlab.net/dashboard/db/postgresql-tuple-statistics)
* [Transaction Overview](https://dashboards.gitlab.net/dashboard/db/transaction-overview?orgId=1)
* [Rails Controllers](https://dashboards.gitlab.net/dashboard/db/rails-controllers?orgId=1)

### Documentation

Basically everything under <https://docs.gitlab.com/ee/development/README.html#databases>, but the following guides in particular are important:

* [What requires downtime?](https://docs.gitlab.com/ee/development/what_requires_downtime.html)
* [Adding database indexes](https://docs.gitlab.com/ee/development/adding_database_indexes.html)
* [Post Deployment Migrations](https://docs.gitlab.com/ee/development/post_deployment_migrations.html)
* [Background Migrations](https://docs.gitlab.com/ee/development/background_migrations.html)
* [SQL Migration Style Guide](https://docs.gitlab.com/ee/development/migration_style_guide.html)
* [SQL Query Guidelines](https://docs.gitlab.com/ee/development/sql.html)
* [Infrastructure runbooks and documentation](https://gitlab.com/gitlab-com/runbooks#postgresql)

For various other development related guides refer to <https://docs.gitlab.com/ee/development/README.html>.

### Slack Channels

We recommend you join at least the following Slack channels:

* [#database](https://gitlab.slack.com/messages/database)
* [#development](https://gitlab.slack.com/messages/development)
* [#performance](https://gitlab.slack.com/messages/performance)
* [#production](https://gitlab.slack.com/messages/production)

Don't try to keep up with everything as some of these channels can see a lot of activity, instead just idle there in case somebody needs you. The most important channel is `#database`.

We also recommend turning off `@here` and `@channel` mentions for `#production` and `#development` to reduce the amount of unwanted notifications.

## Important Groups

Make sure you are a member of the group <https://gitlab.com/gl-database>. This makes it easier to assign merge request approvers or mention all database specialists at once.

## Workflow

There are four main repositories database engineers work in:

* <https://gitlab.com/gitlab-org/gitlab-ce>
* <https://gitlab.com/gitlab-org/gitlab-ee>
* <https://gitlab.com/gitlab-com/infrastructure>
* <https://gitlab.com/gitlab-com/database>

We also primarily use the following labels:

* "database": for anything database related.
* Performance labels "P1-4" and severity labels "S1-4" for estimating the priority of an issue. See [Availability and Performance Priority Labels](/handbook/engineering/performance/#performance-labels) and [CONTRIBUTING.md](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#bug-priority-labels) for more information. In short: P1 is the most important, P4 the least.
* "performance": for performance related issues and merge requests.
* "OKR-DB": issues to be completed in the current OKR.

### Issue Boards

To make it easier to work we have the following issue boards:

* [GitLab.org OKR Issue Board][okr-issue-board]: this board lists all the issues we should complete in the current OKR.
* [GitLab.com OKR Issue Board][okr-infra-issue-board]: this board lists all the infrastructure issues that we should complete in the current OKR.
* [GitLab.org Database Issue Board][db-issue-board]: this board lists all database related issues (regardless of the OKR they belong to).

### Creating Issues

Always make sure an issue exists for the work you are about to perform. As a rule of thumb: work does not exist unless there is an issue for it. Issues are not only used to describe the work to do, but also to track progress. Make sure you update your issues on a regular basis with your findings, statistics, progress, etc. It's better to share too much information on the work being done than to share too little.

### Assigning Issues

We recommend you only assign issues to yourself if you are actively working on them. If you are simply _interested_ in an issue it's best left unassigned until you are working on it. This way you don't end up with an issue list that is thousands of issues long with no progress being made.

### Ask!

Don't sit around doing nothing if you can't find anything to work on! Instead just ask what should be done in the `#database` channel if no AP1/2/3 issues are available.

### Weekly Goals

For planning we use so called "Weekly Goals". Weekly goals are written in an issue that's created for the next work week / sprint. These work weeks range from Monday to Friday. These issues are assigned to all database specialists. Some examples of these issues:

* <https://gitlab.com/gitlab-com/database/issues/85>
* <https://gitlab.com/gitlab-com/infrastructure/issues/2459>

The work to be done is planned with the database team. When planning try to plan enough for 4 or so days, but make sure you don't plan too much. It's better to plan less and achieve everything than to plan a lot and achieve very little.

We also use these issues to document what we're working on and to communicate status.

The format of the issue bodies is fairly straightforward: for every database specialist there is a checklist referring to other issues (perhaps with some brief info) to perform, which are checked off as work is completed. Checklists can be created using the following Markdown:

```markdown
* [ ] This is an item on my checklist
* [x] This item is marked as done
```

An overview of existing issues can be found at <https://gitlab.com/gitlab-com/database/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Weekly+Goals>.

To make it easier to create these issues you can use the issue template "Database Goals".

## Notification Settings

To prevent yourself from getting buried in unread notifications it's best to adjust the default notification settings of your GitLab account. We recommend the following:

* Set the "Global notification level" setting in <https://gitlab.com/profile/notifications> to "Disabled".
* Make sure "Receive notifications about your own activity" is unchecked.
* Disable notifications for the "gl-infra" group if you are a member, unless you are interested in getting notifications whenever somebody mentions `@gl-infra` (which can happen quite a lot).

Using this setup you will _not_ get any Email notifications. TODOs are still created but _only_ if somebody mentions your username or a group you are a member of.

## Slack Notifications

We recommend turning off Slack notification popups as these can be quite invasive, especially when multiple notifications are displayed at once. Turning off the sound notifications can also greatly help as you won't be distracted every time somebody sends you a message or mentions your username.

[okr-issue-board]: https://gitlab.com/groups/gitlab-org/-/boards/414134
[okr-infra-issue-board]: https://gitlab.com/groups/gitlab-com/-/boards/539339
[db-issue-board]: https://gitlab.com/groups/gitlab-org/-/boards/414142
