---
layout: markdown_page
title: Issue Escalations
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

Escalating GitLab issues correctly is an important part of providing quick and accurate customer support. The support team uses the processes and escalation points described on this page when dealing with GitLab issues.

## Issue Prioritization

In general, the Product team  will prioritize all issues
(not just customer requests/index.html.md) as described elsewhere in the handbook, specifically for
[the product managers](https://github.com/isamu-isozaki/teamai_test/tree/master/product/product-areas/#prioritization/index.html.md), and for [engineering](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/workflow/index.html.md). From those pages, generally, it goes in order of:

1. Regressions
1. Bugs
1. Product Direction / Vision
1. New Feature Proposal

The Support Team plays a role in communicating the **impact to customers** of regressions, bugs, and feature
requests. By using issue templates and then using the appropriate labels on those issues, the team can
communicate _within the support team_ about which customer-affecting issues are high priority, and also show
this to the team at large. By then participating in the scheduling effort for each release, the Support Team
represents the voice of the customer in product development.

### Make important issues visible to the Product team

The best way to get attention by the Product team is to know how Product chooses issues to prioritize and
to ship in the next release. These are the criteria that allow a good communication about priorities between the
Support team and the Product team:

1. Consider labeling an issue as ~SP1 only if:
   - It is a relevant ~bug
   - You really think this is something that should be done in the next release
   - The issue is critical for the relationship with a customer (use also ~customer or ~"customer+" labels in this case/index.html.md)
1. Label the issue with the proper [team label](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#team-labels/index.html.md),
   this is the first label PMs filter for when they want to schedule issues
1. Label the issue as ~regression, ~bug, ~"feature proposal" or ~"enhancement"

If the PM will find only a few issues marked as ~SP1 while planning, it is easier they can be included in the scheduling.
Having a lot of results can make it difficult to figure out what should be done to help the Support team.

When contributing to the issue, it is valuable to add the most detailed description possible (removing sensitive details in case/index.html.md),
it is easy to figure out the scenario without jumping into the Zendesk ticket. Providing a link to the ticket is a good practice, anyway.

The Support team can directly ping the PM in the #product Slack channel (see
[who to talk to](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#who-to-talk-to-for-what/index.html.md)/index.html.md)
in case this may help the communication.

When writing in issues, be specific: do not simply `cc` as this does not
indicate what action is required.
For example: "@PM please provide feedback on this issue. Are we interested in
fixing/implementing this? How critical do you think it is?"

### General notes on making issues

#### Use templates

When reporting a bug/regression or feature proposal. For example, `gitlab-ce` project has 'Bug' and 'Feature Proposal'
templates.

#### Use labels

Always. Use either `~bug` or `~feature proposal` and
also add `~customer`. For certain premium subscribers, you may need to use
`~customer+`. If there are one or more component labels that are appropriate,
such as `~ldap`, add those, too. Add [Support Priority labels](#support-priority-labels/index.html.md) ( `~SP1`, `~SP2`, `~SP3`/index.html.md) to indicate perceived priority inside the Support Team.

#### Maintain confidentiality

If an image, log output, etc. is required for the issue, try to produce your own test image. If you are unable
to reproduce the issue and you wish to use the image provided by the customer make sure you _obtain
permission_ from the customer since the image may (inadvertently/index.html.md) include sensitive information like names,
group names, user names, or code.

#### Information gathering

For the *Application and environment information* section of issue templates, use:

+ Omnibus: `sudo gitlab-rake gitlab:check`
+ Source: `sudo -u git -H bundle exec rake gitlab:check RAILS_ENV=production SANITIZE=true`
________________________
+ Omnibus: `sudo gitlab-rake gitlab:env:info`
+ Source: `sudo -u git -H bundle exec rake gitlab:env:info RAILS_ENV=production`

### Regressions

We aim to fix [regressions](https://docs.gitlab.com/ee/university/glossary/#regression/index.html.md) in patch releases, when possible. However, not all regressions are created equal - we will work to patch the high-impact ones first.

For all regressions, add the `~regression` label and the milestone the regression was introduced in.
For high-impact regressions, also add `~"Next Patch Release"` and ping the relevant lead, along with any experts on the subject area.

### Bugs and Feature Proposals

By default, add an appropriate [support priority label](#support-priority-labels/index.html.md) to bugs and feature proposals. The labels are `~SP1`, `~SP2`, and `~SP3`, where `SP1` is the highest priority.
These labels are applied in addition to the `~bug`, `~feature proposal` and `~customer` labels. Use
priority labels in accordance with the urgency / impact matrix below.

The reasoning behind adding an `~SP` label to _every_ of these issues is that each issue _should_ have had
someone consider the urgency and impact, and this is best done at time of creating the issue since that is
when the information and context is "fresh" in your memory. It is OK to change the assessment and label at a
later date upon reflection (for example, during the support-internal scheduling meeting/index.html.md). When an issues are
allowed to be filed _without_  an `~SP` label it will be unclear whether an issue lacks the label due to lack
of urgency / impact, or due to missing a step in the process.

> **Note about feature proposals:** GitLab has limited development resources.
  Additionally, we must think about how widely applicable a feature may be to
  other users. Requests that are very specific to one company's workflow are
  likely to be rejected. Even if a feature seems widely applicable, we may
  leave the feature proposal dormant for some time and see if other users
  and customers chime in that they are also interested. Features that garner
  interest from multiple organizations will be considered more rapidly. Of
  course, there are always exceptions to these 'rules'. This note is meant to
  set the expectation that feature proposals may not be implemented quickly.

### Support Priority labels

Use the following as a guideline to determine which Support Priority label to use (if any/index.html.md) for bugs and feature proposals.

- **Urgency:** _For example: Does this break all GitLab functionally or just a small part?_
  - U1 - A large part, or a fundamental part
  - U2
  - U3 - Only a small part
- **Impact:** _For example: How many users does this impact?_
  - I1 - Many users
  - I2
  - I3 - Limited number of users

| **Urgency \ Impact**          | **I1 - High** | **I2 - Medium**  | **I3 - Low**   |
|-------------------------------|---------------|------------------|----------------|
| **U1 - High**                 | `SP1`         | `SP1`            | `SP2`          |
| **U2 - Medium**               | `SP1`         | `SP2`            | `SP3`          |
| **U3 - Low**                  | `SP2`         | `SP3`            | `SP3`          |

### Escalating from the Support Team to the Development Team

On the last Tuesday of each month, the Support Team reviews the `SP` labeled issues (especially `SP1` and
`SP2`/index.html.md), discusses priorities, and chooses the top few to present to the Product team
for potential deliverables in the next release.

After the support team prioritizes it, we ping the relevant product manager for the express purpose of
scheduling. Having the Product team comment in the issues directly follows our core value of being transparent and will help customers understand the
context around why / when their issues are being resolved, and it provides direct feedback from
customers to the Development and Product teams.

Working this way, it is possible that a customer reported issue is not picked up for a while (scheduling
first, then time to work on a fix, then schedule for release, etc./index.html.md). However, the idea is that this is OK
because most truly urgent issues will in fact be regressions that don’t have this
scheduling problem. If a bug isn't a regression, that means it has existed for more than a month when the customer notes it, and thus we've gone at least a full month without someone reporting the issue as urgent.

**Note**
- Issues are not scheduled for a particular release unless Product adds them to a release milestone
*and* they are assigned to a developer. We aim to be realistic about scheduled deliverables and will
avoid scheduling issues that cannot be delivered in a given release.
- Safety valve: If something is "truly urgent", pinging leads in the issues when they are created is the best
way to go, so it can be made Next Patch Release. This will often be preceded by loud debate and concurrence on
chat.

## Functional escalation points

| Service/Product  | Escalation Types                 | Escalation Point                                        | Assignment      |
|------------------|--------------------------------|-----------------------------------------------------------|------------------
| GitLab CE        | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/gitlab-ce/issues/new        |
| GitLab EE        | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/gitlab-ee/issues/new        |
| GitHost.io       | Bug reports, Feature proposals | https://gitlab.com/gitlab-com/githost/issues/new          | Maintainer of GitHost.io
| Omnibus GitLab   | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/omnibus-gitlab/issues/new   | Omnibus GitLab specialist
| GitLab Runner    | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/gitlab-runner/new  | GitLab CI specialist
| GitLab Workhorse | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/gitlab-workhorse/issues/new | Maintainer of gitlab-workhorse


**See the [GitLab team page](/team/index.html.md/index.html.md) for assignments**


## Operational escalation points


| Service/Product       | Escalation Type                                                                                  | Escalation Point                                         |  Assignment      |
|-----------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------|----------------------- |
| GitLab Infrastructure | Anything related to the **running of GitLab.com**, performance, something breaks                | https://gitlab.com/gitlab-com/infrastructure/issues/new | Production Lead/Senior Production Engineer
| GitLab.com Support Engineers| Anything related to the **use of GitLab.com**, operations that can't be performed with admin access  | https://gitlab.com/gitlab-com/support/services/services-meta/new | Use `~"SE Escalation"` label |
| GitLab Support        | Any and all questions in relation to providing customer service for GitLab users and customers. | https://gitlab.com/gitlab-com/support/support-team-meta/issues/new        | Support Team Lead/Senior Support Engineer

**See the [GitLab team page](/team/index.html.md/index.html.md) for assignments**

### Notes

#### GitHost.io

+ GitHost [project](https://dev.gitlab.org/gitlab/GitHost/index.html.md)
+ GitHost [service](http://githost.io/index.html.md)

#### Omnibus GitLab

+ Related to Omnibus GitLab packaging only.
+ GitLab [omnibus release packages](https://packages.gitlab.com/gitlab/index.html.md)

#### GitLab Runner

- Information on [GitLab Runner](https://gitlab.com/gitlab-org/gitlab-runner#features/index.html.md)
- [Runner documentation](http://docs.gitlab.com/ee/ci/runners/README.html/index.html.md)

#### GitLab Workhorse

- Information on [GitLab Workhorse](/2016/04/12/a-brief-history-of-gitlab-workhorse/index.html.md/index.html.md)
- **Description**  *"Gitlab-workhorse is a smart reverse proxy for GitLab. It handles "large" HTTP requests such as file downloads, file uploads, Git push/pull and Git archive downloads."*

#### GitLab Infrastructure

- Reach the infra team on [Slack](https://gitlab.slack.com/archives/infrastructure/index.html.md)
- Old blog post on [infrastructure](/2016/04/29/look-into-gitlab-infrastructure/index.html.md/index.html.md)
