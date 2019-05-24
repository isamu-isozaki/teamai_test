---
layout: markdown_page
title: "Infrastructure"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Common Links

- [Public Infrastructure Issue Tracker](https://gitlab.com/gitlab-com/infrastructure/issues/index.html.md/index.html.md) 
- [Public Production Issue Tracker](https://gitlab.com/gitlab-com/production/issues/index.html.md/index.html.md)
- [Public Gitlab.com Incidents](https://gitlab.com/gitlab-com/production/issues?label_name%5B%5D=incident/index.html.md) that track [GitLab.com incidents](handbook/engineering/infrastructure/incident-management/index.html.md/index.html.md)
- [Public Gitlab.com Changes](https://gitlab.com/gitlab-com/production/issues?label_name%5B%5D=change/index.html.md) that track [GitLab.com change management](handbook/engineering/infrastructure/change-management/index.html.md/index.html.md)

- Refer to [on-call labeled issues](https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=oncall/index.html.md) to see issues that the oncall is working on
- Refer to the [production team milestones](https://gitlab.com/gitlab-com/infrastructure/milestones/index.html.md) to see the scheduled work being done by the production team
- Slack channels
  - [#alerts](https://gitlab.slack.com/archives/alerts/index.html.md)
  - [#production](https://gitlab.slack.com/archives/production/index.html.md)
  - [#sre-lounge](https://gitlab.slack.com/archives/sre-lounge/index.html.md)
  - [#database](https://gitlab.slack.com/archives/database/index.html.md)
- Refer to the [runbooks](https://gitlab.com/gitlab-com/runbooks/index.html.md) and contribute back to them
- [On-call Handover Document](https://docs.google.com/document/d/1IrTi06fUMgxqDCDRD4-e7SJNPvxhFML22jf-3pdz_TI/index.html.md)
- [On-call Reports](https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=%E2%9C%93&state=closed&label_name[]=oncall%20report/index.html.md)

## Other Pages
{:.no_toc}

- [Production onboarding](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/production-onboarding/index.html.md)
- [GitLab.com architecture](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/production-architecture/index.html.md/index.html.md)
- [GitLab.com environments](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/environments/index.html.md/index.html.md)
- [Monitoring GitLab.com](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/monitoring/index.html.md/index.html.md)
- [Performance of GitLab.com](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/performance/index.html.md)
- [Database Reliability](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/database/index.html.md/index.html.md)
- [Production team handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/production/index.html.md/index.html.md)
- [Production Readiness Guide](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md/index.html.md)
- [GitLab.com and GitLab Hosted data breach notification policy](/security/#data-breach-notification-policy/index.html.md)
- [On-call Handover](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/on-call-handover/index.html.md/index.html.md)

## Vision

**GitLab.com is the Largest Production GitLab Installation on the Planet.**

The Infrastructure Department is the primary responsible party for the **availability**, **reliability**,
**performance**, and **scalability** of all user-facing services (most notably **GitLab.com**/index.html.md). Other departments
and teams contribute greatly to these attributes of our service as well. In these cases it is the responsibility
of the Infrastructure Department to close the feedback loop with monitoring and metrics to drive accountability.

We are a blend of operations gearheads and software crafters that apply sound enginering principles, operational
discipline and mature automation to make GitLab.com ready for mission-critical customer workloads. We strive for
excellence every day by living and breathing [**GitLab's values**](https://github.com/isamu-isozaki/teamai_test/tree/master/values/index.html.md/index.html.md) as our guiding operating
principles in every decision we make and every action we take.

## Blueprint and OKRs

The [**Infrastructure Blueprint**]( blueprint/index.html.md/index.html.md) outlines our overall priorities and focus on a quarterly basis.
The blueprint drives Infrastructure's OKRs, which quality and quantify the objectives and key results.

## Design

[**Design**](design/index.html.md/index.html.md) plays a significant role in how we produce technical solutions to meet the challenges we face
in making GitLab.com ready for mission-critical workloads. 

## Team

An operational environment is a complex and interconnected mesh of components working in unison to deliver a set of
services. Rather than organize the team along siloed functional groups, our team is aligned with the environment's
**lifecycle**, taking into account the two variables that drive change into the environment: time and space. Events
and actions take place in the environment in a time scale (between essentially _now_ and _soon_/index.html.md) and their effect on
people resources is higher the closer said resources are to the environment.

### Structure

Our long-term objective is to become a world-class SRE organization. In order to reach that goal, we are adopting a
**focal** arrangement where the organizational formula is derived from the focus and purpose of the groups arranged
along the time and space variables, and each group contains the appropriate functional resources necessary to manage
the environment, which include systems and database specialties.

The [first iteration](https://about.gitlab.comhttps://github.com/isamu-isozaki/teamai_test/tree/master/values/#iteration/index.html.md) in this model comprises two groups:

* **Site Availability**, which operates on the _here_ and _now_ and is focused on uptime as its driving force.
* **Site Reliability**, which operates on the _soon_ time horizon and is focused on efficiency, and of course, reliability.

![GitLabInfraOrgStructureV1.png](img/GitLabInfraOrgStructureV2.png/index.html.md)

#### Rotation

Team members in Infrastructure rotate between both groups on a 6-9 month schedule to ensure that all team members level
on the skills necessary to be successful in our long-term vision. The rotation allows each and every one of us to get a
sense of the priority axes across both groups, which will eventually merge under a single SRE umbrella.

#### Long-term Structure

As our processes and automation mature, the quality of our work will stabilize and be more predictable. We will become
adept at maintaining high levels of uptime across the board. **Site Availability** will then merge into
**Site Reliability**, at which point we will have several vertical **Site Reliability** teams that follow the sun.
GitLab.com is a global service, and as such, so must be Infrastructure.

### Site Availability Engineering (SAE/index.html.md)

**Site Availability** is the gatekeeper and primary caretaker of the operational environment, focusing on its uptime and state as it exists in the present.

Over the next 12 to 18 months, we will focus relentlessly on the **availability** of GitLab.com so that it becomes
engrained in everything we do. Thus, the team's priorities are driven, almost exclusively, by availability
considerations, effecting the cultural shift necessary to achieve our uptime goals. This group has the
greatest latitude in making changes to the environment that ensure uptime in the _here_ and _now_, and is the final
authority as it relates to changes in GitLab.com.

Site Availability is the primary owner (but not the only consumer/index.html.md) of the following operational processes and procedures:

* [**delta management**](delta-management/index.html.md/index.html.md)
* [**change management**](change-management/index.html.md/index.html.md)
* [**incident management**](incident-management/index.html.md/index.html.md)

Key metrics related to this group include:

* **Uptime**: of the operational environment at large and of services, subsystems and components.
* **Incidents**: alerts (including false positives/index.html.md), count, length (elapsed time/index.html.md), outages, escalations
* **Deployments**: count, length (elapsed time/index.html.md), â€œgoodâ€ vs â€œbadâ€
* **Efficiencies**: manual vs automated tasks, (unexpected/index.html.md) interrupts

### Site Reliability Engineering (SRE/index.html.md)

**Site Reliability** is the complementary primary caretaker of the operational environment, focusing on its uptime
through reliability considerations. Whereas **Site Availability** is focused on the _here_ and _now_, **Site Reliability** has a slightly longer time horizon, _soon_. Its guiding principles are efficiency, effectiveness and
frugality. In a sense, this is the team that will outdate both change and delta management. In very colloquial terms,
**Site Reliability** produces well-designed machine parts to replace duct-tape placed in the environment.
