---
layout: markdown_page
title: "Engineering Workflow"
---

This document explains the workflow for anyone working with issues in GitLab Inc.
For the workflow that applies to everyone please see [PROCESS.md](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md/index.html.md).

## On this page
{:.no_toc}

- TOC
{:toc}


## GitLab Flow

Products at GitLab are built using the [GitLab Flow](https://docs.gitlab.com/ee/workflow/gitlab_flow.html/index.html.md).

## Broken master

If you notice that pipelines for the `master` branch of GitLab [CE] or [EE] are failing (red/index.html.md) or broken (green as a false positive/index.html.md), fixing this takes priority over everything else development related, since everything we do while tests are broken may break existing functionality, or introduce new bugs and security issues.

[CE]: https://gitlab.com/gitlab-org/gitlab-ce/commits/master
[EE]: https://gitlab.com/gitlab-org/gitlab-ee/commits/master

### As a Developer

1. Look for [an issue labelled ~"broken master"][broken-master-issues] that would track the failure
1. If it doesn't exist, [create it][new-issue], ping the relevant people, and post it in `#development` so that other developers are aware of the problem and can help
1. If you have the time, assign it to yourself and start working on it
1. Reply to the automatic "Pipeline failed" notifications in `#development` by mentioning the issue
1. If the problem isn't fixed within a few hours, `@mention` the relevant Engineering Leads and CTO in the issue and on Slack, so that resources can be assigned to fix it as quickly as possible.

[new-issue]: https://gitlab.com/gitlab-org/gitlab-ce/issues/new

### As a Maintainer

It's ok to merge a merge request with a failing pipeline if the following conditions are met:

1. The failure also happens on `master`, and the failing specs are not directly related to functionality touched by the merge request
1. There is [an issue labelled ~"broken master"][broken-master-issues] for it, see the "As a developer" steps above for more details

Before merging, it's a good practice to mention that the failure happens in `master`, and to post a reference to the issue. For instance:

```
Failure in <JOB_URL> happens in `master` and is being worked on in #XYZ, merging.
```

[broken-master-issues]: https://gitlab.com/groups/gitlab-org/-/issues?state=all&label_name[]=broken%20master

## Security Issues

Security issues are managed and prioritized by the security team. If you are assigned to work on a security issue in a milestone, you need to follow these steps:

1. **Do not push code relating to the fix to GitLab.com.** The changes should be kept confidential until the release, and there is no way to make merge requests on GitLab.com confidential at the moment.
1. Instead, work against the equivalent project on [dev.gitlab.org](https://dev.gitlab.org/gitlab/index.html.md). For instance, GitLab
   Community Edition on dev is at [gitlab/gitlabhq](https://dev.gitlab.org/gitlab/gitlabhq/index.html.md).
1. Create your merge request from the most recent security branch. For example, if the current release is 23.5, then use the `security-23-5` branch as the target for your merge request.
1. If no security branch exists, create one from the latest stable branch. For the previous example, you can run (assuming dev is the remote/index.html.md):

    ```sh
    git checkout -b security-23-5 origin/23-5-stable
    git push -u dev HEAD
    ```

1. [Double link](https://github.com/isamu-isozaki/teamai_test/tree/master/communication/#everything-starts-with-an-issue/index.html.md) the issue to the merge request on dev, and the merge request on dev to the issue.
1. Most security issues will need backports to the [previous two monthly releases](https://docs.gitlab.com/ee/policy/maintenance.html#security-releases/index.html.md). For example, if the current release is 23.5, then we would also need MRs to `security-23-4` and `security-23-3`.
   1. **Note**: you do not have to create the backport merge requests until the merge request has been reviewed and is ready to merge, if you would rather wait.
1. Check and add a note in the security issue you're working on listing which GitLab versions does it affects. For example:
     - GitLab CE and EE 8.9.0 - 9.5.10
     - GitLab CE and EE 10.0.0 - 10.1.5
     - GitLab CE and EE 10.2.0 - 10.2.5
   These will be included in the upcoming blog posts.
1. Security patches will eventually be merged into `master` using a [patch set from the most recent stable branch](https://gitlab.com/gitlab-org/release-tools/blob/master/doc/security.md#picking-security-patches-into-master/index.html.md). After the merge requests for the stable branches have been merged, the release manager will ping you if the changes don't apply cleanly to `master` or pass all tests.
1. If an issue exists for the target security patch release, link the merge requests with all the backports and relevant issue to that as well.

If you find a security issue in GitLab, create a **confidential issue** mentioning the relevant security and engineering managers, and post about it in `#security`.

If you accidentally push security commits to GitLab.com, we recommend that you:
1. Delete the relevant branch ASAP
2. Inform a release manager in `#releases`. It may be possible to execute a garbage collection (via the Housekeeping task in the repository settings/index.html.md) to remove the commits.

For more information on how the entire process works for security releases, see the
[documentation on security releases](https://gitlab.com/gitlab-org/release-tools/blob/master/doc/security.md/index.html.md).

## Basics

1. Start working on an issue you’re assigned to. If you’re not assigned to any issue, find the issue with the highest priority you can work on, by relevant label. [You can use this query, which sorts by priority for the started milestones][priority-issues], and filter by the label for your team.
1. If you need to schedule something or prioritize it, apply the appropriate labels (see [Scheduling issues](#scheduling-issues/index.html.md)/index.html.md).
1. If you are working on an issue that touches on areas outside of your expertise, be sure to mention someone in the other group(s/index.html.md) as you soon as you start working on it. This allows others to give you early feedback, which should save you time in the long run.
1. You are responsible for the issues assigned to you. This means it has to ship with the milestone it's associated with. If you are not able to do this, you have to communicate it early to your manager and other stakeholders (e.g. the product manager, other engineers working on dependent issues/index.html.md). In teams, the team is responsible for this (see [Working in Teams](#working-in-teams/index.html.md)/index.html.md). If you are uncertain, err on the side of overcommunication. It's always better to communicate doubts than to wait.
1. You (and your team, if applicable/index.html.md) are responsible for:
  - ensuring that your changes [apply cleanly to GitLab Enterprise Edition][ce-ee-docs].
  - the testing of a new feature or fix, especially right after it has been merged and packaged.
1. Once a release candidate has been deployed to the staging environment, please verify that your changes work as intended. We have seen issues where bugs did not appear in development but showed in production (e.g. due to CE-EE merge issues/index.html.md).

For general guidelines about issues and merge requests, be sure to read the [GitLab Workflow][gitlab-workflow].

[priority-issues]: https://gitlab.com/groups/gitlab-org/issues?scope=all&sort=priority&state=opened&milestone_title=%23started&assignee_id=0
[ce-ee-docs]: https://docs.gitlab.com/ee/development/automatic_ce_ee_merge.html#avoiding-ce-gt-ee-merge-conflicts-beforehand
[gitlab-workflow]: https://github.com/isamu-isozaki/teamai_test/tree/master/communication/#gitlab-workflow

## Working in Teams

For larger issues or issues that contain many different moving parts, you'll be likely working in a team. This team will typically consist of a [backend developer](/job-families/engineering/developer/index.html.md/index.html.md), a [frontend developer](/job-families/engineering/frontend-engineer/index.html.md/index.html.md), a [UX designer](/job-families/engineering/ux-designer/index.html.md/index.html.md) and a [product manager](/job-families/product/product-manager/index.html.md/index.html.md).

1. Teams have a shared responsibility to ship the issue in the planned release.
    1. If the team suspects that they might not be able to ship something in time, the team should escalate / inform others as soon as possible. A good start is informing your manager.
    1. It's generally preferable to ship a smaller iteration of an issue, than ship something a release later.
1. Consider starting a Slack channel for a new team, but remember to write all relevant information in the related issue(s/index.html.md). You don't want to have to read up on two threads, rather than only one, and Slack channels are not open to the greater GitLab community.

## Convention over Configuration

Avoid adding configuration values in the application settings or in
`gitlab.yml`. Only add configuration if it is absolutely necessary. If you
find yourself adding parameters to tune specific features, stop and consider
how this can be avoided. Are they values really necessary? Could constants be
used that work across the board? Could values be determined automatically?
See [Convention over Configuration](https://github.com/isamu-isozaki/teamai_test/tree/master/product#convention-over-configuration/index.html.md) for more discussion.

## Choosing Something to Work On

Start working on things with the highest priority in the current milestone. The priority of items are defined under labels in the repository, but you are able to sort by priority.

After sorting by priority, choose something that you’re able to tackle and falls under your responsibility. That means that if you’re a frontend developer, you work on something with the label `frontend`.

To filter very precisely, you could filter all issues for:

- Milestone: Started
- Assignee: Unassigned
- Label: Your label of choice. For instance `CI/CD`, `Discussion`, `Quality`, `frontend`, or `Platform`
- Sort by priority

[Use this link to quickly set the above parameters][priority-issues]. You'll still need to filter by the label for your own team.

If you’re in doubt about what to work on, ask your lead. They will be able to tell you.

## Triaging and Reviewing Code from the rest of the Community

It's every [developers' responsibilities] to triage and review code contributed by the rest of the community, and work with them to get it ready for production.

Merge requests from the rest of the community should be labeled with the `Community Contribution` label. 

When evaluating a merge request from the community, please ensure that a relevant PM is aware of the pending MR by mentioning them.

This should be to be part of your daily routine. For instance, every morning you could triage new merge requests from the rest of the community that are not yet labeled `Community Contribution` and either review them or ask a relevant person to review it.

Make sure to follow our [Code Review Guidelines](https://docs.gitlab.com/ee/development/code_review.html/index.html.md).

[developers' responsibilities]: /job-families/engineering/developer/#responsibilities

## Workflow Labels

Labels are described in our [Contribution guide][contrib-labels-guide].

[contrib-labels-guide]: https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#workflow-labels

## Working with GitLab.com

GitLab.com is a very large instance of GitLab Enterprise Edition. It runs release candidates for new releases, and sees a lot of issues because of the amount of traffic it gets. There are several internal tools available for developers at GitLab to get data about what's happening in the production system:

### Performance Data

There is extensive [monitoring](https://dashboards.gitlab.com/index.html.md/index.html.md) publicly available for GitLab.com. For more on this and related tools, see the [monitoring handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/monitoring/index.html.md).

More details on [GitLab Profiler](http://redash.gitlab.com/dashboard/gitlab-profiler-statistics/index.html.md) are also found in the [monitoring performance handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/monitoring/index.html.md).

### Error Reporting

- [Sentry](https://sentry.gitlap.com/index.html.md/index.html.md) is our error reporting tool
- [log.gitlab.net](https://log.gitlap.com/index.html.md/index.html.md) has production logs
- [prometheus.gitlab.com](https://prometheus.gitlab.com/alerts/index.html.md) has alerts for the [production team](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/#production-team/index.html.md)

### Feature Flags

If you've built feature flags into your code, be sure to read about [how to use the feature flag to test a feature on GitLab.com](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/#feature-flags/index.html.md).

## Scheduling Issues

GitLab Inc has to be selective in working on particular issues. We have a limited capacity to work on new things. Therefore, we have to schedule issues carefully.

Product Managers are responsible for scheduling all issues in their respective [product areas](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#who-to-talk-to-for-what/index.html.md), including features, bugs, and tech debt. Product managers alone determine the [prioritization](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#prioritization/index.html.md). The UX Lead and Engineering Leads are responsible for allocating people making sure things are done on time. Product Managers are _not_ responsible for these activities, they are not project managers.

Direction issues are the big, prioritized new features for each release. They are limited to a small number per release so that we have plenty of capacity to work on other important issues, bug fixes, etc.

If you want to schedule an `Accepting Merge Requests` issue, please remove the label first.

Any scheduled issue should have a team label assigned, and at least one type label.

### Requesting Something to be Scheduled

To request scheduling an issue, ask the [responsible product manager](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#who-to-talk-to-for-what/index.html.md)

We have many more requests for great features than we have capacity to work on. There is a good chance we’ll not be able to work on something. Make sure the appropriate labels (such as `customer`/index.html.md) are applied so every issue is given the priority it deserves.

### Process Improvement

There is an informal scheduling process discussion in the #scheduling Slack channel. Anyone can join and suggest improvements to our scheduling process.

## Product Development Timeline

[![](gitlab-release-timelines.png/index.html.md)](https://gitlab.com/gitlab-org/gitlab-ce/snippets/1731455/index.html.md)

Teams (Product, UX, Engineering/index.html.md) continually work on issues according to their respective workflows. There is no specified process whereby a particular person should be working on a set of issues in a given time period. However, there are specific deadlines that should inform team workflows and prioritization. Suppose we are talking about milestone `m` that will be shipped in month `M` (on the 22nd/index.html.md). We have the following deadlines:

- By month `M-1, 1st`:
  - Release scope is finalized. In-scope issues marked with milestone `m`.
  - `m` issues are updated with docs starter blurb. Release post (WIP merge request/index.html.md) created with `m` issues and docs starter blurbs.
- On month `M-1, 8th` (or next business day/index.html.md): Kickoff call
- By month `M, 7th`: Completed `m` issues with docs have been merged into master. Un-started or unfinished `m` issues are de-scoped from `m`, with `m` being removed from them.
- On or around `M, 15th`: [team retrospectives](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/management/team-retrospectives/index.html.md) should happen so they can inform the [public retrospective](#retrospective/index.html.md)
- On month `M, 22nd`: Release shipped to production. Release post published.
- On month `M, 22nd`: The next Release has been tentatively planned by Product and has been shared with engineering for discussion.

Refer to [release post due dates](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/blog/release-posts/#due-dates/index.html.md) for additional deadlines.

Note that release timelines are overlapping. For example, when a release is shipped to production on the 22nd, the scope for the following release has already been established earlier in that same month.

An in-scope issue already has a docs starter blurb (written by the PM/index.html.md) by the time engineers start development. Engineers should create and merge in the updated docs as part of completing an issue by the 7th. PMs revise the starter docs blurbs in the release post appropriately before the release post is published.

Refer to [Feature freeze on the 7th for the release on the 22nd](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md#feature-freeze-on-the-7th-for-the-release-on-the-22nd/index.html.md) for further timeline details of code releases, including major/minor version releases, as well as patch releases.

## Updating Issues Throughout Development

Team members use labels to track issues throughout development. This gives visibility to other developers, product managers, and designers, so that they can adjust their plans during a monthly iteration. An issue should follow these stages:

- `In dev`: A developer indicates they are developing an issue by applying the `In dev` label.
- `In review`: A developer indicates the issue is in code review and UX review by removing the `In dev` label, and applying the `In review` label.


## Kickoff

At the beginning of each release, we have a kickoff meeting, publicly livestreamed to YouTube. In the call, the Product Development team (PMs, UX designers, and Engineers/index.html.md) communicate with the rest of the organization which issues are in scope for the upcoming release. The call is structured by [product area](../../product/index.html.md#who-to-talk-to-for-what/index.html.md) with each PM leading their part of the call.

The notes are available in a publicly-accessible [Google doc](https://docs.google.com/document/d/1ElPkZ90A8ey_iOkTvUs_ByMlwKK6NAB2VOK5835wYK0/edit?usp=sharing/index.html.md). Refer to the doc for details on viewing the livestream.

## Retrospective

After each release, we have a retrospective meeting, publicly livestreamed to YouTube. We discuss what went well, what went wrong, and what we can improve for the next release.

In each retrospective we choose a low number (1-3/index.html.md) of high-impact improvements that can be realistically delivered before the next release. A single champion is identified to deliver each improvement. A Champion then follows up on their task to completion. Before the start of the next retrospective, champions are expected to resolve their action items and update the retrospective document on their improvement tasks. And we talk about the status of each improvement at the start of the following retrospective.

The notes are available in a publicly-accessible [Google doc](https://docs.google.com/document/d/1nEkM_7Dj4bT21GJy0Ut3By76FZqCfLBmFQNVThmW2TY/edit?usp=sharing/index.html.md). Refer to the doc for details on viewing the livestream.

## Kickoff and Retrospective Livestream Instructions

Before the meeting starts, remind people who plan to speak to join the Google Hangout earlier, since there is a 50 user limit.

Several minutes before the scheduled meeting time, follow the [livestreaming instructions](../../communication/index.html.md#live-streaming/index.html.md) to start a Google Hangout using the `Now` setting. Paste the Google Hangout invite link in the Google doc.

At the scheduled meeting time, start broadcasting live to YouTube. Begin the meeting.

## Use Group Labels and Group Milestones

When working in GitLab (and in particular, the GitLab.org group/index.html.md), use group labels and group milestones as much as you can. It is easier to plan issues and merge requests at the group level, and exposes ideas across projects more naturally. If you have a project label, you can promote it to a group milestone. This will merge all project labels with the same name into the one group label. The same is true for promoting group milestones.

## Technical debt

We definitely don't want our technical debt to grow faster than our code base. To prevent this from happening we should consider not only the impact of the technical debt but also a contagion. How big and how fast this problem is going to be over time? Is it likely a bad piece of code will be copy-pasted for a future feature? In the end, the amount of resources available is always less than amount of technical debt to address.

To help with prioritization and decision-making process here, we recommend thinking about contagion as an interest rate of the technical debt. There is [a great comment](http://disq.us/p/1ros2o9/index.html.md) from the internet about it:

> You wouldn't pay off your $50k student loan before first paying off your $5k credit card and it's because of the high interest rate. The best debt to pay off first is one that has the highest loan payment to recurring payment reduction ratio, i.e. the one that reduces your overall debt payments the most, and that is usually the loan with the highest interest rate. 

