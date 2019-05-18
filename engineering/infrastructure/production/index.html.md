---
layout: markdown_page
title: "Production Team"
---

## Common Links

- [Public Infrastructure Issue Tracker](https://gitlab.com/gitlab-com/infrastructure/issues/); please use confidential issues for topics that should only be visible to team members at GitLab.
- [Chat channel](https://gitlab.slack.com/archives/production); please use the `#production` chat channel for questions that don't seem appropriate to use the issue tracker or the internal email address for.
- [GitLab Production Calendar](https://calendar.google.com/calendar/embed?src=gitlab.com_si2ach70eb1j65cnu040m3alq0%40group.calendar.google.com&ctz=America/Los_Angeles); add it to your own views by hitting the `+GoogleCalendar` button in the lower right of the screen when viewing the Calendar with the link here.
- [Production On-Call Reports](https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=%E2%9C%93&state=all&label_name[]=oncall%20report)

## On this page
{:.no_toc}

- TOC
{:toc}

## Production Team

The Production SRE team is responsible for all user-facing services. Production SREs ensure that these services are secure, reliable, and fast. This infrastructure includes staging, GitLab.com and dev.GitLab.org; see the [list of environments](/handbook/engineering/infrastructure/environments/).

Production SREs also have a strong focus on building the right toolsets and automations to enable development to ship features as fast and bug free as possible, leveraging the tools provided by GitLab.com itself - we must dogfood.

Another part of the job is building monitoring tools that allow quick troubleshooting as a first step, then turning this into alerts to notify based on symptoms, to then fixing the problem or automating the remediation. We can only scale GitLab.com by being smart and using resources effectively, starting with our own time as the main scarce resource.

## GitLab.com

We want to make GitLab.com ready for mission critical workloads. That readiness means:

1. Speedy ([speed index](/handbook/engineering/performance/#performance-target) below 2 seconds)
1. Available (uptime above 99.95%)
1. Durable (automated backups and restores, monthly manual tests)
1. Secure (prioritize requests of our security team)
1. Deployable (quickly deploy and provide metrics for new versions in all environments)

### Tenets

1. Security: reduce risk to its minimum, and make the minimum explicit.
1. Transparency, clarity and directness: public and explicit by default, we work in the open, we strive to get signal over noise.
1. Efficiency: smart resource usage, we should not fix scalability problems by throwing more resources at it but by understanding where the waste is happening and then working to make it disappear. We should work hard to reduce toil to a minimum by automating all the boring work out of our way.

## Workflow

### Adding work to the Team Backlog and getting it prioritized

Add issues at any time to the [infrastructure issue tracker](https://gitlab.com/gitlab-com/infrastructure/issues).
Let one of the managers for the production team know of the request.  It would be helpful for our prioritization to know the timeline for the issue if your team has commitments related to it.  We do reserve part of our time for interrupt requests, but that does not always mean we can fit in everything that comes to us.

### Team board and Milestones

#### Production Issue Tracker
We have a [production issue tracker](https://gitlab.com/gitlab-com/production/issues).  Issues in this tracker are meant to track incidents and changes to production that need approval.  We can host discussion of proposed changes in linked infrastructure issues.  These issues should have ~incident or ~change and notes describing what happened or what is changing with relevant infrastructure team issues linked for supporting information.

*  All issues affecting customers S1-S4
*  All changes to infrastructure serving production traffic

#### Infrastructure Issue Tracker
We plan our work from the infrastructure [team board](https://gitlab.com/gitlab-com/infrastructure/boards/619904?=) in a [Kanban style workflow](https://kanbanize.com/blog/kanban-for-devops-teams/), though with no swimlanes.

The columns on our board are:

1.  Planning - Issues that we are talking about - to be refined to an actionable state.
1.  Ready - Issues that are "ready to pull"
1.  Waiting - Issues that have been started, but are waiting on an external item (vendor ticket, another team, etc)
1.  In Progress
1.  Completed (aka Closed) - Issue is closed per all notes or criteria in the issue description.

Guiding philosophies:
To get from Planning to Ready, an issue should be:

* Sized in the weight field on a fibonacci scale: 1,2,3,5,8,13,21
* If the issue is a 8 or above, work on breaking it down into smaller issues, making the first issue an Epic
* Have guiding notes or clear criteria for what marks it as done
* Ideally this planning will be done async, but a quick meeting to review an issues guiding notes may be scheduled.

We'll organize our work into 2 week [milestones](https://gitlab.com/gitlab-com/infrastructure/milestones).  These milestones are meant to:

1.  Give us a timebox to gain some measure of velocity over time.
1.  Give us a window of time to focus on a particular team for planned work.  As themes go, it is better to try to focus on one theme for a few time boxes rather than start 3 things and not finish any.
1.  Ideally, as we have more clarity on velocity 50-60% of a milestone's velocity will be scheduled/known work while the remaining work will be room for emergent or toil related work.  
1.  We will hold monthly async planning sessions to pick the particular areas the team will focus on
1.  Issues that fit the theme will be scheduled into milestones as velocity allows.

There will always be a "Current Milestone" and a "Next Milestone".  This way when making or updating issues, we can use quick actions like `\milestone %"Current  Milestone` and `\milestone %"Next Milestone"` to quickly get issues adde.

When a milestone is complete, we'll rename the finished milestone to the YYYY-MM-DD Milestone and update the Current and Next milestones.

We also want to value handing off issues to take advantage of the many timezones our team covers.  An issue may be started by any team member in any timezone, but we can mark an issue with ~Ready_to_Handoff for issues that can go to someone in another timezone.  If we mark an issue with the ~Ready_to_Handoff label, it should have clear notes about where it is being left off and next steps.  Handing off is not required, anyone can own an issue to completion too, but we want to be able communicate and work across the many people on our team were it makes sense.  

The Milestones will run from a Monday to a Friday that is 12 days away.  The Milestone will be named with the Month and End date of the timebox.  For example August Milestone 2 - ending 2018-08-24.


## Why `infrastructure` and `production` queues?

### Premise

Long term, additional teams will perform work on the production environment:

* Release Engineering performs deployments on production
* Security performs scans against the production
* Google may perform work on the underlying production infrastructure

We cannot keep track of **events** in production across a growing number of *functional* queues.

Furthermore, said teams will start to have on-call rotations for both their function (e.g., security) and their services.  For people on-call, having a centralized tracking point to keep track of said events is more effective than perusing various queues. Timely information (in terms of when an event is happening and how long it takes for an on-call person to understand what's happening) about the production environment is critical. The `production` queue centralizes production event information.

### Implementation

Functional queues track team workloads (`infrastructure`, `security`, etc) and are the source of the work that has to get done. Some of this work clearly impacts production (build and deploy new storage nodes); some of it will not (develop a tool to do x, y, z) until is deployed to production.

The `production` queue tracks events in production, namely:

* [changes](https://about.gitlab.com/handbook/engineering/infrastructure/change-management/)
* [incidents](https://about.gitlab.com/handbook/engineering/infrastructure/incident-management/)
* deltas (exceptions) -- still need to do handbook write up

Over time, we will implement hooks into our automation to *automagically* inject change audit data into the `production` queue.

This also leads to a single source of data. Today, for instance, incident reports for the week get transcribed to both the On-call Handoff and Infra Call documents (we also show exceptions in the latter). These meetings serve different purposes but have overlapping data. The input for this data should be queries against the `production` queue versus the manual build in documents.

Additionally, we need to keep track of error budgets, which should also be derived from the `production` queue.

We will also be collapsing the `database` queue into the `infrastructure` queue. The database is a special piece of the infrastructure for sure, but so are the storage nodes, for example.


### Security Related Changes

All direct or indirect changes to authentication and authorization mechanisms used by GitLab Inc. by customers or employees require additional review and approval by a member of at least one of following teams:


* [production team](/handbook/engineering/infrastructure/production/) member
* [security team](/security/)  member
* developer from a different team that is staff level or higher

This process is enforced for the following repositories where the approval is mandatory using
[MR approvals](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html):

* [gitlab-oauth2-proxy](https://gitlab.com/gitlab-cookbooks/gitlab-oauth2-proxy)
* [gitlab_users](https://gitlab.com/gitlab-cookbooks/gitlab_users)

Additional repositories may also require this approval and can be evaluated on a
case-by-case basis.

### Labeling Issues

We use [issue labels](https://gitlab.com/gitlab-com/infrastructure/labels) within the Infrastructure issue tracker to assist in prioritizing and organizing work. Prioritized labels are:

- `~(perceived) data loss`
- `~critical`
- `~SL1` and `~SL2`
- `~unblocks others`
- `~outage`
- `~goal`
- `~blocked`
- `~oncall`

We also use the `~AP1`, `~AP2`, `~AP3` labels as described in [availability & performance priority labels](/handbook/engineering/performance/#performance-labels). Those are mainly used to communicate priority of issues to Product Managers, for scheduling purposes.

Issues labeled `~oncall` are prioritized to be worked on by the current oncall team memers.

#### Goals and Meta Goal

`~goals` are issues that are in a WoW and we agreed as a team that we will do everything in our power to deliver them.  Goal issues should fit in one WoW, that is, they are deliverable in a single week time, if they do not fit in one WoW we are probably talking about a `~meta ~goal`.

We use this kind of issues to indicate a general direction (generally speaking something that will take from 1 to 3 months of work) This means that a `~meta ~goal` should be achievable in one quarter.

`~meta` issues that are not also `~goal` are the tasks that are larger than what fits in a quarter, therefore they need to be sliced into actually deliverable pieces that can also become a goal.

#### Other Labels

We use some other labels to indicate specific conditions and then measure the impact of these conditions within production or the production engineering team. This is specially important from the time investment in specific parts of the production engineering team, to reduce toil or to reduce the chance of a failure by accessing to production more than enough.

Labels that are particularly important for gathering data are:

- `~toil` Repetitive, boring work that should be automated away.
- `~unscheduled` An issue that became an interruption to the team and had to be handled in a WoW. It's unplanned work.
- `~unblocks others` An issue that is allowing some other part of the company to deliver something.
- `~access request` When someone is requesting to get access to some part of the infrastructure.
- `~requires production access` Every time someone with production access has to jump into a console to perform some manual operation like running a script in a rails console, or connecting to Redis or the database directly

### Always Help Others

We should never stop helping and unblocking team members. To this end, data should always be gathered to assist in highlighting areas for automation and the creation of self-service processes. Creating an issue from the request with the proper labels is the first step. The default should be that the person requesting help makes the issue; but we can help with that step too if needed.

If this issue is urgent for whatever reason, we should label them following the instructions above and add them to the ongoing WoW.

### Issue or Outage Hand-off

Ongoing outages, as well as issues that have the `~(perceived) data loss` label and are (therefore) actively being worked on need a hand off to happen as team members cycle in and out of their timezones and availability. The on call log can be used to assist with this. (See link at top to on-call log).

## On-Call Support

To ensure 24x7 coverage of emergency issues, we currently have split on-call rotations between EMEA and AMER regions; team members in [EMEA](https://en.wikipedia.org/wiki/List_of_country_groupings) regions are on-call from 0400-1600 UTC, and team members in [AMER](https://en.wikipedia.org/wiki/List_of_country_groupings) regions are on-call from 1600-0400 UTC. We plan to extend this to include team members from the [APAC](https://en.wikipedia.org/wiki/List_of_country_groupings) region in the future, as well. This forms the basis of a [follow-the-sun](https://en.wikipedia.org/wiki/Follow-the-sun) support model, and has the benefit for our team members of reducing (or eliminating) the stress of responding to emergent issues outside of their normal work hours, as well as increasing communication and collaboration within our [global team](https://about.gitlab.com/team/).

For further details about managing schedules, workflows, and documentation, see the [on-call runbook](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/oncall.md).

## Production Events Logging

There are 2 kind of production events that we track:

- Changes to the production fleet: for this we record things [in the Chef Repo](https://dev.gitlab.org/cookbooks/chef-repo).
  - Deploys will be recorded automagically because of the way we do deploys.
  - General operations can be recorded by creating an empty commit in the repo and pushing it into origin.
- Outages and general production incidents
  - If we are required to act in production manually to perform any operation we should create an issue and consider labeling it as _toil_ to track the cost of such manual work load.
  - If we had a disruption in the service, we must create a blameless post mortem. Refer to the [Outages and Blameless Post Mortems](../#postmortems) section of the Infrastructure page.

## Backups

### Summary of Backup Strategy

- Backups of our databases are taken every 24 hours with continuous incremental data (at 60 sec intervals) streaming into a separate cloud service from the production fleet. These backups are encrypted.
- Backups of our filesystems are taken via Azure snapshots every 24 hours.

For details see the runbooks, in particular regarding details on [Azure snapshots](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/azure-snapshots.md) and [Database backups using WAL-E (encrypted)](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/using-wale-gpg.md)

### R.A.D. - Restore Appreciation Days

Every second day of the month, we have a R.A.D. "party". Two production SREs use this day to test our backup processes by fully restoring not-yet-automated backups to test instances and to verify data integrity. The issues for every individual
R.A.D can be found in the [infrastructure tracker](https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=%E2%9C%93&state=opened&search=restore+OR+backup+appreciation+day).

The ongoing effort to automate all the things backups is tracked in the infrastructure [META issue](https://gitlab.com/gitlab-com/infrastructure/issues/3222).
