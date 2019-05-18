---
layout: markdown_page
title: "Technical Writing workflow"
---

## On this page
{:.no_toc}

* Will be replaced with the ToC, excluding the "On this page" header
{:toc}

This document explains the workflow of the Technical Writing team. Consider it
an extension of the [Engineering workflow](/handbook/engineering/workflow/)
which you should be familiar with.
For the workflow that applies to everyone please see
[PROCESS.md](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md).

## Process

In order to avoid situations where a feature slips through without documentation,
there must be a clear, defined process.

A checklist is present in the MR template to make sure that documentation is
part of the MR, but sometimes there are some legitimate reasons to defer
documentation from the initial MR which then makes it easy to get lost.

Two things you need to remember:

1. For every release cycle, every issue that introduces a new feature and requires
   new documentation to be added or changed, **must have** the `Documentation` label
   assigned along with one of the
   [priority labels](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#workflow-labels).
1. If the implementation MR for some reason cannot have docs, only merge the MR if
   there is a _new_ issue created that is tracking the docs needed. The new issue
   should have the appropriate milestone, assignee and at least both the
   `Documentation` and `Deliverable` labels, which is important so that the issue
   is shown in the [Documentation issue board][board]. Make sure to link back to the
   implementation MR and the initial issue for a reference. This will save time
   from searching information needed to write the docs.

The [GitLab.org group issue board][board] can then be used to schedule what
issues to work on.

## Priority and scheduling

There are various types of issues you are called to work on:

- Documenting and reviewing the new features for the current release
- Working on the [Documentation Backlog](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Documentation)
- Enhancing the [docs website](https://gitlab.com/gitlab-com/gitlab-docs/issues)

Below is the current priority of scheduling issues:

1. Documentation for the current release (consult the [board])
1. Documentation issues with the [customer label](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Documentation&label_name[]=customer)
1. Everything else

## Workflow labels

Labels are described in our [Contribution guide][contrib-labels-guide].

[contrib-labels-guide]: https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#workflow-labels

## Product development timeline

The documentation should be ready by the 8th for the kickoff call and the link
added to the [release post](/handbook/marketing/blog/release-posts/) of the
upcoming release. For more information on the product development timeline, see the
[Engineering handbook](/handbook/engineering/workflow/#product-development-timeline).

[board]: https://gitlab.com/groups/gitlab-org/-/boards/375110?milestone_title=%23started&=&label_name[]=Documentation
