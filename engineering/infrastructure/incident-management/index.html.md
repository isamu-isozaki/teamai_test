---
layout: markdown_page
title: "Incident Management"
---

## On this page
{:.no_toc}

- TOC
{:toc}

# Incidents

Incidents are **anomalous conditions** that result in **service degradation** or **outage** and require intervention (human or automated/index.html.md) to restore service to full operational status in the shortest amount of time possible. The primary goal of incident management is to organize chaos into swift incident resolution. To that end, incident management requires well defined roles for all resources involved, control points to manage the flow of both resolution path and information, active and effective communication to notify the appropriate stakeholders about the status of an incident and its resolution, and post-mortem, root-cause analysis and introspective analysis procedures.

## Incident Severities

Incident severities encapsulate the impact of an incident and scope the resources allocated to handle it. Detailed definitions must be provided for each severity, and these definitions must be reevaluated as new circumstances become known. Incident management uses our standarized severity definitions, which can be found under [`CONTRIBUTION.MD`](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#severity-impact-guidance/index.html.md).

* Sev1 and Sev2 incidents cannot be considered closed until GitLab.com has been fully operational, onine, stable and performant for 30 minutes after the incident was resolved.
* When a closed Sev2 or Sev3 incident is followed by another Sev2 or Sev3 incident within 3 hours, the latter incidents are automatically upgraded to Sev2 incidents.

### Alert Severities

* Alerts severities do not necessarily determine incident severities. A single incident can trigger a number of alerts at various severities, but the determination of the incident's severity is driven by the above definitions.
* Over time, we aim to automate the determination of an incident's severity through service-level monitoring that can aggregate individual alerts against specific SLAs.

## Roles

| **Role** | **Definition and Examples** |
| -------- | ------------------------|
| `IMOC`   | **Incident Manager** |
|          | The **Incident Manager** is the tactical leader of the incident response team, and it must not be the person doing the technical work resolving the incident. The IMOC assembles the Incident Team, evaluates data (technical and otherwise/index.html.md) coming from team members, evaluates technical direction of incident resolution and coordinates troubleshooting efforts, and is responsible for documentation and debriefs after the incident.|
| `CMOC`   | **Communications Manager** |
|          | The **Communications Manager** is the communications leader of the incident response team. The focus of the Incident Team is on resolving the incident as quickly as possible. However, there is a critical need to disseminate information to appropriate stakeholders, including employees, eStaff, and end users. For Sev1 (and possibly Sev2/index.html.md) incidents, this is a dedicated role. Otherwise, IMOC can handle communications.|
| `OCIT`   | **On-Call + Incident Team** |
|          | The Incident Team is primarily composed of the on-call person. However, the Incident Manager can call in additional resources as necessary.|

These definitions imply several on-call rotations for the different roles. The IMOC should be a technical person with a good understanding of GitLab.com's architecture. The CMOC is not required to be technical. The IMOC and the CMOC work in tandem to manage the incident and timely communication.

## Communication Channels

Information is a key asset during any incident. Properly managing the flow of information to its intended destination is critical in keeping interested stakeholders apprised of developments in a timely fashion. The awareness that an incident is in progress is critical in helping stakeholders plan for said changes.

This flow is determined by:

* the type of information,
* its intended audience, 
* and timing sensitivity.

Furthermore, avoiding information overload is necessary to keep every stakeholder’s focus.

To that end, we will have:

* a dedicated incident bridge (zoom call/index.html.md) for all incidents.
* a dedicated `#incident` channel, since `#production` contains sizeable amounts of information and it takes effort to filter out non-relevant items. This is particularly important for the incident team, which must be focused on technical information to resolve the incident. While `#incident` is an open channel and anyone is free to join, we will encourage people to use other channels to communicate with the IMOC.
* periodic updates intended to the various audiences at place (CMOC handles this/index.html.md):
  * End-users (Twitter/index.html.md)
  * eStaff
  * Support staff
  * Employees at large
* [a dedicated repo for issues related to Production](https://gitlab.com/gitlab-com/production/index.html.md) separate from the queue that holds Infrastructures’s workload: namely, issues for incidents and changes.


