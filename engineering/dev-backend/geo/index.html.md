---
layout: markdown_page
title: "Geo and Disaster Recovery"
description: "Summary of how the Geo Team operates"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## The Geo Team

[Geo](/features/gitlab-geo/) is a [Premium](/pricing/) feature, built to help speed up the development of distributed teams by providing one or more read-only mirrors of a primary GitLab instance. This mirror (a Geo secondary node) reduces the time to clone or fetch large repositories and projects, can be used to run automated tests, or can be part of a Disaster Recovery solution. 

## Goals and Priorities

The goal of the Geo Team is to provide an easily configurable read-only mirror of a GitLab installation that is complete, accurate, verifiable and efficient.

In the longer term, our goal is to be able to promote any secondary node to a primary node state to support a Disaster Recovery situation.

We are also considering what a read-write mirror would involve and where this would fit on our roadmap.  

To that end, our priorities are:

1. [Hashed Storage GA](https://gitlab.com/groups/gitlab-org/-/epics/75), alleviating challenges from the [legacy storage solution](https://docs.gitlab.com/ee/administration/repository_storage_types.html).
2. To [deploy Geo in another GCP region](https://gitlab.com/gitlab-com/gl-infra/infrastructure/issues/4741), providing gitlab.com with resilience. (This also promotes our value of [collaboration](https://about.gitlab.com/handbook/values/#collaboration) through dogfooding.)  
3. Reduce the effort required to install, configure and maintain Geo secondary nodes.
4. Clear up any bugs concerning the accuracy of the replicated data, or the reporting on the state of a secondary node.
5. Ensure that Geo runs efficiently.

## Geo's Relationship to Disaster Recovery

Disaster Recovery (DR) is a set of policies, tools and procedures put in place to be able to recover from a disaster. 

Geo provides data redundancy. The customer will have a redundant copy of data in a separate location. If anything were to happen to their primary instance, a secondary instance still retains a copy of the data. 

However, data redundancy is one part of a complete DR strategy. 

High Availability (HA) is also a step towards Disaster Recovery. At the moment Geo does not provide true HA because if the primary instance is not available, certain actions are not possible.

## Common Links

Documentation
- [Geo](https://docs.gitlab.com/ee/gitlab-geo/)
- [Disaster Recovery](https://docs.gitlab.com/ee/administration/geo/disaster_recovery/index.html)
- [Planned Failover](https://docs.gitlab.com/ee/administration/geo/disaster_recovery/planned_failover.html)
- [Background Verification](https://docs.gitlab.com/ee/administration/geo/disaster_recovery/background_verification.html)

Other Resources
- Issues relating to Geo are mostly to be found on the
[gitlab-ee issue tracker](https://gitlab.com/gitlab-org/gitlab-ee/issues/?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Geo)
- [Chat channel](https://gitlab.slack.com/archives/g_geo); please use the `#g_geo`
chat channel for questions that don't seem appropriate to use the issue tracker
for.

## Geo Terminology

| Term  |  Definition |  
|---|---|
| Geo |  The product name given to the feature that provides the ability to create one or more read-only mirrors for the main/primary instance |
| Primary  | The main, primary instance where read-write operations are allowed |
| Secondary  | An instance that synchronizes with the Primary node where only read-only operations are permitted |

## Planning and Demos

### Discussions

Discussions are documented [separately](https://docs.google.com/document/d/18vGk6dQs7L0oGQOb_bNiFa5JhwLq5WBS7oNxQy09ml8/edit#heading=h.p295wb40mdh4).

### Planning

We use issue boards to focus on each milestone and a [planning board](https://gitlab.com/groups/gitlab-org/-/boards/796972?&label_name[]=Geo) to look further ahead.  

[Here](https://gitlab.com/groups/gitlab-org/-/epics?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Geo) you can find the Epics for Geo. 

### Demos

The demos are recorded and should be stored in Google Drive under "GitLab Videos --> [Geo Demos](https://drive.google.com/drive/u/0/folders/1Ot2ElWwEh9vdPx1K8VO5ZMBkxlmRAXm4)". If you recorded the demo, please make sure the recording ends up in that folder.
