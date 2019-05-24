---
layout: markdown_page
title: "UX Department Workflow"
---

### On this page

{:.no_toc}

- TOC
{:toc}

## Meet The UX Department

Our UX department is made up of designers and researchers from all around the world. Each of them brings their own unique cultures, experiences, and strengths to GitLab. You can learn about each member of UX by visiting our [team page](/team/index.html.md/index.html.md) and filtering by "UX".

## UX Weekly Call

The UX Department gets together once a week to share and discuss a variety of topics including workflow shortcuts or processes, designs for feedback, UX articles, and conferences. Attendance is optional but participation is encouraged. Each call is recorded and added to the archive.

### Product development timeline

The product development timeline is described in the [engineering workflow](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/workflow/#product-development-timeline/index.html.md) section of the handbook. We will also explain it here.

At GitLab we follow a monthly release cycle, shipping on the 22nd of each month.  We plan and track these monthly releases using [milestones](https://docs.gitlab.com/ee/user/project/milestones/index.html.md/index.html.md).  

There are specific deadlines that inform our workflows and prioritization. Suppose we are talking about milestone `m` that will be shipped in month `M` (on the 22nd/index.html.md). We have the following deadlines:

- By month `M-1, 1st`:
  - Release scope is established. In-scope issues marked with milestone `m`.
  - `m` issues are updated with docs starter blurb. Release post (WIP merge request/index.html.md) created with `m` issues and docs starter blurbs.
- On month `M-1, 8th` (or next business day/index.html.md): Kickoff call
- By month `M, 7th`: Completed `m` issues with docs have been merged into master. Un-started or unfinished `m` issues are de-scoped from `m`, with `m` being removed from them.
- On or around `M, 15th`: [team retrospectives](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/management/team-retrospectives/index.html.md) should happen so they can inform the [public retrospective](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/workflow/#retrospective/index.html.md)
- On month `M, 22nd`: Release shipped to production. Release post published.
- On month `M 22nd`: The next Release has been tentatively planned by Product and has been shared with engineering for discussion.

Our release timelines are overlapping. For example, when a release is shipped to production on the 22nd, the scope for the following release has already been established earlier in that same month. The following visualization illustrates that overlapping concept.

![rolling-planning-visualization.png](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ux/rolling-planning-visualization.png/index.html.md)

### Working with PMs

Every UX Designer is aligned with a PM. The UXer is responsible for the same features their PM oversees. The UX Designer meets with their PMs and other engineers every month to discuss scheduling and prioritization. Once the milestone has been set, the UXer assigns themselves to the issues in their area that need UX. UXers should immediately engage in and facilitate a conversation with the PM and engineers involved with the issue. Communicate early and often.

Understanding which PM is responsible for which area of the product is essential. An excellent resource for this is the [who to talk to for what](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#who-to-talk-to-for-what/index.html.md) and [product categories](https://github.com/isamu-isozaki/teamai_test/tree/master/product/categories/index.html.md/index.html.md) sections of the handbook. The [product section](https://github.com/isamu-isozaki/teamai_test/tree/master/product/index.html.md/index.html.md) of the handbook will give you a deep dive into how product at GitLab thinks and works.

### Milestone Planning

Between the 22nd and 1st of each month, UXers meet with their PMs and other Engineering managers to discuss the priorities for the upcoming milestone. The purpose of these meetings is to ensure that all understand the requirements and to assess whether or not there is the capacity to complete all the issues proposed. The issues set for a particular milestone must be decided by the 1st of each month to give the engineering departments time to plan. There will be occasions where priorities shift, and changes must be made after the 1st. We should remain flexible and understanding of these situations while doing our best to make sure these exceptions do not become the rule.

### Milestone Kickoff

Before working on the next release, we have a company kickoff call to explain what we expect to ship in the next release. This call is led by the product team and highlights significant improvements and features.

The UX Department has its kickoff as part of the [UX weekly call](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ux#ux-weekly-call/index.html.md) directly preceding or following kickoff on the 8th of the month. Using the planning sheet as our guide, each designer walks through the issues they will be working on for that milestone. The kickoff fosters transparency and collaboration across the whole team so it is important that all UXers attend.

### Community Contributions

We want to make it as easy as possible for GitLab users to become GitLab contributors. The UX team should offer support, guidance, and resources to any community member interested in contributing code and/or UX improvements.

Issues that are beneficial to our users, 'nice to have(s/index.html.md),' that we currently do not have the capacity for or want to give priority to are part of our [Backlog (Accepting merge requests/index.html.md)](https://gitlab.com/gitlab-org/gitlab-ce/issues?scope=all&utf8=âœ&state=opened&milestone_title=Backlog%20(Accepting%20merge%20requests/index.html.md)/index.html.md), just as any issue we want to do but is not planned right now. We want to encourage our community to contribute at any stage of an issue we are interested in. If a backlog issue has an additional [UX ready](https://gitlab.com/gitlab-org/gitlab-ce/issues?scope=all&utf8=âœ&state=opened&milestone_title=Backlog%20(Accepting%20merge%20requests/index.html.md)&label_name[]=UX%20ready/index.html.md) label, this issue points to changes that:

* We already agreed on,
* Are well-defined from UX perspective,
* Are likely to get accepted by a maintainer.

As a member of the UX Department, make sure to alert the UX Manager if you are asked to work on one of the issues but donâ€™t have the capacity. The UX manager is responsible for encouraging the community member to suggest a solution, share a design proposal, and keep the conversation going.

For full details on contributing in general, see the [contributing doc](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#label-for-community-contributors/index.html.md).

### UX Designer Workflow

Once assigned to an issue, there is general workflow UX Designers follow. 

Read about [__UX Designer workflows__](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ux/ux-designer/index.html.md)

### UX Research Workflow

There is a general workflow UX Researchers follow.

Read about [__UX Researcher workflows__](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ux/ux-research/index.html.md)

### How we use labels

GitLab uses labels to categorize, prioritize, and track work. The following is a breakdown of the labels most directly related to the UX workflow. An overview of all the workflow label types and uses can be found in the [contributing doc](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#workflow-labels/index.html.md).

* [**UX** label](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=UX/index.html.md): indicates that UX work is required on this issue.
* [**product discovery** label](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=product%20discovery/index.html.md): indicates that the final expected output for this issue could be a doc of requirements, a design artifact, or even a prototype. The issue is intended to be the place for UX, PM, FE, and BE to discuss the problem and potential solutions. The issue is considered done when all involved in the issue feel there is a path forward and the doc, specs, or mockups have been added to a follow-up issue. The implementation of the final solution will be developed in a subsequent milestone. The solution is due on the 7th of the month corresponding to the milestone where the 22nd is the release date. (For example, 10.6 was released on March 22nd, 2018. **product discovery** labeled issues with milestone 10.6 were due on March 7, 2018. [This follows the same due date as the feature freeze for engineering](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md#feature-freeze-on-the-7th-for-the-release-on-the-22nd/index.html.md)./index.html.md) 
* [**UI polish** label](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UI+polish/index.html.md): indicates the issue covers _only_ visual improvement(s/index.html.md) to the existing user interface
* [**UX debt** label](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX+debt/index.html.md): indicates that the issue covers user experience improvement(s/index.html.md) that weren't fully implemented or could be refined after implementation.
* [**Regression** label](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=regression/index.html.md): indicates a bug introduced in the latest release that broke correct behavior (see the [contribution guidelines](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#regression-issues/index.html.md) for more info/index.html.md).
* [**UX ready** label](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=UX%20ready/index.html.md): indicates that all UX work is completed and all feedback has been addressed.

### Milestone Retro

After each release, we have a company retrospective call in which we discuss what went well, what went wrong, and what we can improve for the next release.

To understand the specific challenges faced by the UX Department, we hold an async UX retrospective after every milestone. This retro is done within the planning document. The goal is to evaluate what went well, what didnâ€™t go well, and how we can improve.

### Epics and issues

We use epics and issues to organize, discuss, and execute our day-to-day work. Epics are used to define a larger vision and goal for a feature or area of the product. Issues within the epic drive the actions taken to achieve the desired results. In most cases, PM and the UX Manager are utilizing epics to plan and execute efforts over several milestones. 


[ux-guide]: https://docs.gitlab.com/ee/development/ux_guide/
[ux-label]: https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX
[ux-ready-label]: https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX+ready
[gitlab-design-project-readme]: https://gitlab.com/gitlab-org/gitlab-design/blob/master/README.md
[twitter-sheet]: https://docs.google.com/spreadsheets/d/1GDAUNujD1-eRYxAj4FIYbCyy8ltCwwIWqVTd9-gf4wA/edit
