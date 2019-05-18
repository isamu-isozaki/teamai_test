---
layout: markdown_page
title: "Infrastructure"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Common Links

- [Public Infrastructure Issue Tracker](https://gitlab.com/gitlab-com/infrastructure/issues/) 
- [Public Production Issue Tracker](https://gitlab.com/gitlab-com/production/issues/)
- [Public Gitlab.com Incidents](https://gitlab.com/gitlab-com/production/issues?label_name%5B%5D=incident) that track [GitLab.com incidents](handbook/engineering/infrastructure/incident-management/)
- [Public Gitlab.com Changes](https://gitlab.com/gitlab-com/production/issues?label_name%5B%5D=change) that track [GitLab.com change management](handbook/engineering/infrastructure/change-management/)

- Refer to [on-call labeled issues](https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=oncall) to see issues that the oncall is working on
- Refer to the [production team milestones](https://gitlab.com/gitlab-com/infrastructure/milestones) to see the scheduled work being done by the production team
- Slack channels
  - [#alerts](https://gitlab.slack.com/archives/alerts)
  - [#production](https://gitlab.slack.com/archives/production)
  - [#sre-lounge](https://gitlab.slack.com/archives/sre-lounge)
  - [#database](https://gitlab.slack.com/archives/database)
- Refer to the [runbooks](https://gitlab.com/gitlab-com/runbooks) and contribute back to them
- [On-call Handover Document](https://docs.google.com/document/d/1IrTi06fUMgxqDCDRD4-e7SJNPvxhFML22jf-3pdz_TI)
- [On-call Reports](https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=%E2%9C%93&state=closed&label_name[]=oncall%20report)

## Other Pages
{:.no_toc}

- [Production onboarding](/handbook/engineering/infrastructure/production-onboarding)
- [GitLab.com architecture](/handbook/engineering/infrastructure/production-architecture/)
- [GitLab.com environments](/handbook/engineering/infrastructure/environments/)
- [Monitoring GitLab.com](/handbook/engineering/monitoring/)
- [Performance of GitLab.com](/handbook/engineering/performance)
- [Database Reliability](/handbook/engineering/infrastructure/database/)
- [Production team handbook](/handbook/engineering/infrastructure/production/)
- [Production Readiness Guide](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md)
- [GitLab.com and GitLab Hosted data breach notification policy](/security/#data-breach-notification-policy)
- [On-call Handover](/handbook/engineering/infrastructure/on-call-handover/)

## Vision

**GitLab.com is the Largest Production GitLab Installation on the Planet.**

The Infrastructure Department is the primary responsible party for the **availability**, **reliability**,
**performance**, and **scalability** of all user-facing services (most notably **GitLab.com**). Other departments
and teams contribute greatly to these attributes of our service as well. In these cases it is the responsibility
of the Infrastructure Department to close the feedback loop with monitoring and metrics to drive accountability.

We are a blend of operations gearheads and software crafters that apply sound enginering principles, operational
discipline and mature automation to make GitLab.com ready for mission-critical customer workloads. We strive for
excellence every day by living and breathing [**GitLab's values**](/handbook/values/) as our guiding operating
principles in every decision we make and every action we take.

## Blueprint and OKRs

The [**Infrastructure Blueprint**]( blueprint/) outlines our overall priorities and focus on a quarterly basis.
The blueprint drives Infrastructure's OKRs, which quality and quantify the objectives and key results.

## Design

[**Design**](design/) plays a significant role in how we produce technical solutions to meet the challenges we face
in making GitLab.com ready for mission-critical workloads. 

## Team

An operational environment is a complex and interconnected mesh of components working in unison to deliver a set of
services. Rather than organize the team along siloed functional groups, our team is aligned with the environment's
**lifecycle**, taking into account the two variables that drive change into the environment: time and space. Events
and actions take place in the environment in a time scale (between essentially _now_ and _soon_) and their effect on
people resources is higher the closer said resources are to the environment.

### Structure

Our long-term objective is to become a world-class SRE organization. In order to reach that goal, we are adopting a
**focal** arrangement where the organizational formula is derived from the focus and purpose of the groups arranged
along the time and space variables, and each group contains the appropriate functional resources necessary to manage
the environment, which include systems and database specialties.

The [first iteration](https://about.gitlab.com/handbook/values/#iteration) in this model comprises two groups:

* **Site Availability**, which operates on the _here_ and _now_ and is focused on uptime as its driving force.
* **Site Reliability**, which operates on the _soon_ time horizon and is focused on efficiency, and of course, reliability.

![GitLabInfraOrgStructureV1.png](img/GitLabInfraOrgStructureV2.png)

#### Rotation

Team members in Infrastructure rotate between both groups on a 6-9 month schedule to ensure that all team members level
on the skills necessary to be successful in our long-term vision. The rotation allows each and every one of us to get a
sense of the priority axes across both groups, which will eventually merge under a single SRE umbrella.

#### Long-term Structure

As our processes and automation mature, the quality of our work will stabilize and be more predictable. We will become
adept at maintaining high levels of uptime across the board. **Site Availability** will then merge into
**Site Reliability**, at which point we will have several vertical **Site Reliability** teams that follow the sun.
GitLab.com is a global service, and as such, so must be Infrastructure.

### Site Availability Engineering (SAE)

**Site Availability** is the gatekeeper and primary caretaker of the operational environment, focusing on its uptime and state as it exists in the present.

Over the next 12 to 18 months, we will focus relentlessly on the **availability** of GitLab.com so that it becomes
engrained in everything we do. Thus, the team's priorities are driven, almost exclusively, by availability
considerations, effecting the cultural shift necessary to achieve our uptime goals. This group has the
greatest latitude in making changes to the environment that ensure uptime in the _here_ and _now_, and is the final
authority as it relates to changes in GitLab.com.

Site Availability is the primary owner (but not the only consumer) of the following operational processes and procedures:

* [**delta management**](delta-management/)
* [**change management**](change-management/)
* [**incident management**](incident-management/)

Key metrics related to this group include:

* **Uptime**: of the operational environment at large and of services, subsystems and components.
* **Incidents**: alerts (including false positives), count, length (elapsed time), outages, escalations
* **Deployments**: count, length (elapsed time), “good” vs “bad”
* **Efficiencies**: manual vs automated tasks, (unexpected) interrupts

### Site Reliability Engineering (SRE)

**Site Reliability** is the complementary primary caretaker of the operational environment, focusing on its uptime
through reliability considerations. Whereas **Site Availability** is focused on the _here_ and _now_, **Site Reliability** has a slightly longer time horizon, _soon_. Its guiding principles are efficiency, effectiveness and
frugality. In a sense, this is the team that will outdate both change and delta management. In very colloquial terms,
**Site Reliability** produces well-designed machine parts to replace duct-tape placed in the environment.
