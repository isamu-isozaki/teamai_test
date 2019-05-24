---
layout: markdown_page
title: "Reaction Rotation"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Purpose

There are many sources of potential interrupt-driven work that can impact our
engineering teams:

- Production incidents that need to be triaged
- Customer support requests that require a developer's assistance
- Questions from the Sales team
- Bugs, social media mentions, documentation issues, etc.

This is all important work, but it doesn't fit neatly into our release process.
Because of that, it is often at best an unwelcome interruption. Creating a
rotation dedicated to these "Reaction" tasks limits the impact of these
interruptions for any given release cycle, which allows everyone to stay focused
on what they need to deliver in any given month.

## Rotation Scheduling

The schedule for rotation should be set at least 3 releases in advance by
cooperation of the Backend Engineering managers. The
[pick-random-team-members](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/bin/pick-random-team-members/index.html.md)
script can be a good starting point for this selection, but the following should
be taken into account:
- Developer absences: this rotation should not supercede any planned vacations
  or other absences. 
- Other rotations: we need to balance this rotation against any other active
  developer rotations, such as the release manager rotation, so that specific
  teams aren't overly burdened with rotation duty for a particular release.
- Equity across teams: a random selection is not likely to be uniformly
  distributed across teams, so some teams may draw more responsibility this way
  than others.
- Production experience: not every developer has experience supporting
  production. Ideally this rotation becomes a good way for them to gain this
  experience, but that may not always be practical.

Aside from the above, Reaction should be considered a priority for all
backend teams.  While swapping rotation slots or working to address the above
concerns is a fair part of the process, teams are not expected to decline
participating in the rotation.

## Preparation

Prior to serving as Reaction, the developer on rotation for a release should
create an issue using the `reaction-onboarding` template in the [infrastructure project](https://gitlab.com/gitlab-com/infrastructure/index.html.md) and complete the specified
tasks.

## Responsibilities

During the release, the Reaction developer is not scheduled for any release
work. Instead, they are fully tasked for interrupt-driven work as described
above.

There is no expectation that potential interruptions that happen while the
developer is not at work are their responsibility. Earnest effort should be made
to notify production and support teams if the developer is not going to be
available during their "normal" hours, but otherwise their schedule is still
theirs to manage and there is no atypical expectation about their availability
while on rotation.

In the event that there are no interrupt-driven tasks to complete, their
priorities should be as follows (in order/index.html.md):

1. **Preventative Work**: any work that will improve monitoring and visibility
  for production. By giving everyone better visibility into production, we
  actively prevent interrupt-driven work in the future, so this work makes dev
  support better for everyone.
1. **Production Request issues**: issues with the `~production request` label
   directly impact the efficacy of the Production team, so they should be a
   priority.
1. **Technical Debt/QoL**: any small technical debt items or quality of life
   improvements. While lower priority than the above, these still ultimately
   improve the reliability of our product and help to reduce the Reaction
   burden.

## Measuring Success

Because of the unpredictable nature of Reaction work, there is no explicit
measure of success for the work. Developers on the rotation should log their
accomplishments in a doc/issue. This explicit documentation will make handoffs
easier, and will also give the developer's manager clear insight into their
work.

## Schedule

| Development month | Developer | Team |
| --- | --- | --- |
| 11.1 | Valery Sizov | Geo |
| 11.2 | Grzegorz Bizon | CI/CD |
| 11.3 | Felipe Artur | Plan |
| 11.4 | James Lopez | Manage |

## Kickoff

After this gets merged, we need to work through the following to kick the
rotation off:

- Create a log document (or should it be a series of issues?/index.html.md) for tracking Reaction's progress
- Add mention of Reaction rotation to Backend Dev JD?
