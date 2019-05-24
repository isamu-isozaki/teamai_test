---
layout: markdown_page
title: "Change Management"
---

## On this page
{:.no_toc}

- TOC
{:toc}

# Changes

Changes are any **modification to the operational environment** and are classified into two types:

* **Service changes** are regular, routine changes executed through well-tested, automated procedures performed with minimal human interaction that may cause predictable and limited performance degradation and no downtime. As such, service changes do not require review or approval except on their very first iteration.
* **Maintenance changes** are possibly complex changes that require manual intervention beyond initiating the change and that will cause downtime or significant performance degradation by the nature of the change. These changes require strict scheduling, careful planning and review, and approval by the Director of Infrastructure for execution.

**Deployments** are a special change metatype depending on their scope and the effect they may have on the environment, as defined above. As we make progress towards CI/CD, we aim to turn all deployments into simple service changes.

## Trust

**GitLab.com** is the premier GitLab instance on the planet, and a **production** instance in every sense of the word. Change Management's primary goal is to **safeguard the integrity of the GitLab.com environment through increased predictability** by providing a framework to drive all changes towards becoming service changes and to help us achieve an **optimal change speed**.

Change Management is underpinned by **trust**: we trust ourselves to act responsibly in the operational environment to maintain its integrity and, by extension, its availability and performance.

To that end, we are not instituting a blanket policy for changes. Rather, we are developing the foundation of what a service change is (risk evalation, automatic auditing and communication, pre-flight checks, defensive coding, post-change validation/index.html.md) and will help teams with adoption. 

Change Management helps us prioritize our resources towards changes that need to be made more resilient through defensive automation. Priorities are driven by two factors:

* changes that cause ~S1 or ~S2 incidents
* changes driven by services that are below a TBD error budget

In these situations, we will focus on developing the necessary automation and safeguards to help teams and services move towards safe service changes in a timely fashion. Until then, all changes that fall under the two abovementioned categories are treated as maintenance changes.

### Change Severities

Change severities encapsulate the risk associated with a change in the environment. Said risk entails the potential effects if the change fails and becomes an incident. Change management uses our standarized severity definition, which can be found under out which can be found under [`CONTRIBUTION.MD`](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#severity-impact-guidance/index.html.md).

* In order to minimize the number of variables at play, no changes are executed during an active incident.
* ~S1 and ~S2 changes are always serialized and executed exclusively (i.e., never concurrently/index.html.md).
* ~S3 and ~S4 changes are allowed to take place concurrently as long as there is awareness of said concurrency.
* The Infrastructure on-call resource has veto power over any and all changes.

## Change Plans

All changes should have change plans. While this is optional for service changes, it is mandatory for maintenance changes. **Change Plans** provide detailed descriptios of proposed changes and include the following information:

* Change Type
* Change Team Members
* Change Severity
* Detailed steps for the change. Each step must include:
  * pre-conditions for execution of the step,
  * execution commands for the step,
  * post-execution validation for the step

With change plans, we develop a solid library of change procedures. Even more importantly, they provide detailed blueprints for implentation of defensive automation. Ideally, the planner and the executor should be different individuals.

## Change Reviews

Maintenance changes require change reviews. The reviews are intended to bring to bear the **collective** experience of the team while providing a forum for pointing out potential risks for any given change. A minimun quorun of three reviewers is required to approve a ~S1 or ~S2 maintenance change.

## Roles

| **Role** | **Definition and Examples** |
| -------- | ------------------------|
| `EMOC`   | **Event Manager** |
|          | The **Event Manager** is the tactical leader of the change team. For **service changes**, the EMOC is the person executing the change. For **maintenance changes**, the EMOC is the person in the IMOC rotation. ~S1 and ~S2 changes require an EMOC.|
| `CMOC`   | **Communications Manager** |
|          | The **Communications Manager** is the communications leader of the change team. The focus of the Change Team is executing the change as safely and quickly as possible. For ~S1 and ~S2 **maintenance changes**, a CMOC communicates with the appropriate stakeholders. Othersiwe, EMOC can handle communication.|
| `CT`   | **Change Team** |
|          | The Change Team is primarily composed of technical staff perfoming the change.|



## Communication Channels

Information is a key asset during any change.  Properly managing the flow of information to its intended destination is critical in keeping interested stakeholders apprised of developments in a timely fashion. The awareness that a change is happening is critical in helping stakeholders plan for said changes.

This flow is determined by:

* the type of information,
* its intended audience, 
* and timing sensitivity.
 
For instance, a large end-user may choose to avoid doing a software release during a maintenance window to avoid any chance that issues may affect their release.

Furthermore, avoiding information overload is necessary to keep every stakeholder’s focus.

To that end, we will have:

* a dedicated change bridge (zoom call/index.html.md) for S1 and S2 changes.
* a dedicated `#change` channel, since `#production` contains sizeable amounts of information and it takes effort to filter out non-relevant items. This is particularly important for the change team, which must be focused on technical information to perform the change. While `#change` is an open channel and anyone is free to join, we will encourage people to use other channels to communicate with the EMOC.
* periodic updates intended to the various audiences at place (CMOC handles this/index.html.md):
  * End-users (Twitter/index.html.md)
  * eStaff
  * Support staff
  * Employees at large
* [a dedicated repo for issues related to Production](https://gitlab.com/gitlab-com/production/index.html.md) separate from the queue that holds Infrastructures’s workload: namely, issues for incidents and changes. This is useful because there may be other teams, over time, that need to do work in the production environment.


