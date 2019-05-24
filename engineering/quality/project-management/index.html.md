---
layout: markdown_page
title: "Project Management"
---

## On this page
{:.no_toc}

- TOC
{:toc}

# Quality Team's Project Management


## Projects

The Quality team currently works cross-functionally and our task ownership spans multiple projects. 

* **GitLab.org**
  * [Gitlab QA](https://gitlab.com/gitlab-org/gitlab-qa/index.html.md/index.html.md)
  * [GitLab-Insights](https://gitlab.com/gitlab-org/gitlab-insights/index.html.md/index.html.md)
  * [GitLab-Triage](https://gitlab.com/gitlab-org/gitlab-triage/index.html.md)
  * [GitLab CE Tests](https://gitlab.com/gitlab-org/gitlab-ce/index.html.md/index.html.md)
  * [GitLab EE Tests](https://gitlab.com/gitlab-org/gitlab-ee/index.html.md/index.html.md)
  * **Quality Group**
    * [Quality team's task](https://gitlab.com/gitlab-org/quality/team-tasks/boards/index.html.md/index.html.md)
    * [Triage-Ops](https://gitlab.com/gitlab-org/quality/triage-ops/index.html.md/index.html.md)
    * [Nightly tests](https://gitlab.com/gitlab-org/quality/nightly/index.html.md)
    * [Staging tests](https://gitlab.com/gitlab-org/quality/staging/index.html.md)
    * Canary tests (future/index.html.md)
    * Production tests (future/index.html.md)
    * [Known QA failures](https://gitlab.com/groups/gitlab-org/quality/-/issues?scope=all&utf8=%E2%9C%93&state=all&label_name[]=bug/index.html.md)
    
## Project Management

Our team's [Quality: Development board (top level board/index.html.md)](https://gitlab.com/groups/gitlab-org/-/boards/425899/index.html.md) can span 10k+ issues and it's not easy to work on that level. 
As a result, it's only meant to capture the current workload of the team. The board shows who currently owns what in the entire GitLab.org space. 

The board is meant to be read-only. We don't manage the project on that level.

We have sub-boards at the project level that are used for project management, triaging and scheduling issues.

Each project has 3 boards each for a given dimension of the project management component: `Development`, `Prioritization`, and `Scheduling`

### Development

This board shows the current ownership of workload / issues with assignees as the dimension. 

![Development.png](Development.png/index.html.md)

### Prioritization

This board is for prioritization with priorities as the dimension (`~P1` `~P2` `~P3` `~P4`/index.html.md). 

Most important is left most and gradually moves to least urgent.

![Priorities.png](Priorities.png/index.html.md) 
 
### Scheduling

This board is for scheduling with milestones as the dimension. 

Earliest milestone is left most and gradually moves into later milestones.

![Milestones.png](Milestones.png/index.html.md)

## How to use the boards

Each project planning, scheduling and triaging process will happen in the projects' boards. 

The boards are using a consistent configuration and is the same across all of our projects. This means that anyone on the team can work using the same set of tools everywhere.

Think of all these projects as different class of objects with stable interface methods that is consistent and cross-compatible. 

This also ensures that the data rolled up to the top level board is consistent. 

### Board Overview

![Mermaid.png](Mermaid.png/index.html.md)

### Board Links

* **[GitLab.org top Level board](https://gitlab.com/groups/gitlab-org/-/boards/425899/index.html.md)**
   * [GitLab-QA](https://gitlab.com/gitlab-org/gitlab-qa/index.html.md/index.html.md)
     * [`Development`](https://gitlab.com/gitlab-org/gitlab-qa/boards/2922/index.html.md)
     * [`Priorities`](https://gitlab.com/gitlab-org/gitlab-qa/boards/787592/index.html.md)
     * [`Scheduling`](https://gitlab.com/gitlab-org/gitlab-qa/boards/787593/index.html.md)
  * [GitLab-Insights](https://gitlab.com/gitlab-org/gitlab-insights/index.html.md/index.html.md)
     * [`Development`](https://gitlab.com/gitlab-org/gitlab-insights/boards/443349/index.html.md)
     * [`Priorities`](https://gitlab.com/gitlab-org/gitlab-insights/boards/787583/index.html.md)
     * [`Scheduling`](https://gitlab.com/gitlab-org/gitlab-insights/boards/787576/index.html.md)
  * [GitLab-Triage](https://gitlab.com/gitlab-org/gitlab-triage/index.html.md/index.html.md)
     * [`Development`](https://gitlab.com/gitlab-org/gitlab-triage/boards/316854/index.html.md)
     * [`Priorities`](https://gitlab.com/gitlab-org/gitlab-triage/boards/788523/index.html.md)
     * [`Scheduling`](https://gitlab.com/gitlab-org/gitlab-triage/boards/788524/index.html.md)
  * [GitLab CE](https://gitlab.com/gitlab-org/gitlab-ce/index.html.md/index.html.md): GitLab CE issues with `~Quality`
    * [`Quality: Development`](https://gitlab.com/gitlab-org/gitlab-ce/boards/793776/index.html.md)
    * [`Quality: Priorities`](https://gitlab.com/gitlab-org/gitlab-ce/boards/793777/index.html.md)
    * [`Quality: Scheduling`](https://gitlab.com/gitlab-org/gitlab-ce/boards/793779/index.html.md)
  * [GitLab EE](https://gitlab.com/gitlab-org/gitlab-ee/index.html.md/index.html.md): GitLab EE issues with `~Quality` 
    * [`Quality: Development`](https://gitlab.com/gitlab-org/gitlab-ee/boards/793784/index.html.md)
    * [`Quality: Priorities`](https://gitlab.com/gitlab-org/gitlab-ee/boards/793788/index.html.md)
    * [`Quality: Scheduling`](https://gitlab.com/gitlab-org/gitlab-ee/boards/793791/index.html.md)
  * **[Quality group](https://gitlab.com/gitlab-org/quality/index.html.md)**
    * [Triage-Ops](https://gitlab.com/gitlab-org/quality/triage-ops/index.html.md/index.html.md): GitLab-Triage setup for CE/EE and etc.
      * [`Development`](https://gitlab.com/gitlab-org/quality/triage-ops/boards/701857/index.html.md)
      * [`Priorities`](https://gitlab.com/gitlab-org/quality/triage-ops/boards/793763/index.html.md)
      * [`Scheduling`](https://gitlab.com/gitlab-org/quality/triage-ops/boards/793764/index.html.md)
    * [Quality Task](https://gitlab.com/gitlab-org/quality/team-tasks/index.html.md) Roadmap and initiative planning
      * [`Roadmaps`](https://gitlab.com/gitlab-org/quality/team-tasks/boards/548459/index.html.md)
      * [`Initiatives`](https://gitlab.com/gitlab-org/quality/team-tasks/boards/793708/index.html.md)
    * [Nightlies](https://gitlab.com/gitlab-org/quality/nightly/index.html.md)
      * Use the [default board](https://gitlab.com/gitlab-org/quality/nightly/boards/index.html.md)
    * [Staging](https://gitlab.com/gitlab-org/quality/staging/index.html.md)
      * Use the [default board](https://gitlab.com/gitlab-org/quality/staging/boards/index.html.md)
