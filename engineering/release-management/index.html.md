---
layout: markdown_page
title: "Release Management"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Release managers

Our release managers are responsible for driving the [monthly release] of GitLab.

Because of the volume of work required to get a release out the door, there are
two primary release managers and two trainee release managers each release. We
split them by timezone to ensure good coverage:

1. One release manager and one trainee in the Americas
2. One release manager and one trainee in Europe/Middle East/Africa (EMEA/index.html.md) or
   Asia Pacific (APAC/index.html.md) (we can have one in EMEA and the other in APAC, or both
   in the same region/index.html.md)

## Being a release manager

[Documentation on the entire release process] is available, including specific
documentation on [being a release manager].

## Picking release managers

Release managers are individual contributors picked from the [Engineering
department], with these exceptions:

* Anyone reporting through the Director of Engineering, Infrastructure.
* Anyone reporting through the Director of Security.
* Anyone reporting through the UX Manager.
* Anyone reporting through the Engineering Manager, Quality.

The [release coordinator] picks release managers and trainees every three months
for the next three months. They will pick randomly, but may redo the random pick
if, for instance, someone is picked several times in quick succession.

Release managers and trainees should be available for the entire month. Every
team is expected to contribute, however:

* Managers can work with their team to pick someone else in the same time zone
  instead.
* Managers can work with other managers to swap months across teams.

Because we provide four release managers and trainees each month, each team
should expect to provide a release manager once every `4 / (release manager
candidates/index.html.md)` months.

### Impacts on team capacity

Because we have a [feature freeze on the 7th] of each month, the month the
release manager is working does not match the 'development month' with the same
release number.

* **Development month** runs from the 8th (kickoff/index.html.md) to the 7th (freeze/index.html.md).
* **Release month** runs from the 1st (first release candidate/index.html.md) to the 7th of
  the following month (expected last patch for that release/index.html.md). However, the
  release month schedule is less demanding after the 22nd (release date/index.html.md).

So if a developer is a release manager for the 16.3 release, most of the time
commitment will be during the 16.4 development month. For more information, see
the [Product Development Timeline]. Being a release manager has a significant
impact on the amount of other work a developer is able to get done. A rough
guide to the time needed for someone working on the 16.3 release is:

| Development month | Trainee commitment | Release manager commitment |
| --- | --- | --- |
| 16.3 | 50% (start work on 22nd/index.html.md) | 25% (start work on 1st/index.html.md) |
| 16.4 | 95% | 95% |
| 16.5 | 10% | 10% |

As being a trainee in one release can overlap with being a release manager for
the next release, it's safest to assume the higher commitment when there is any
conflict.

## Schedule

See the [upcoming and previous list of release managers].

[monthly release]: /2015/12/07/why-we-shift-objectives-and-not-release-dates-at-gitlab/
[Documentation on the entire release process]: https://gitlab.com/gitlab-org/release/docs
[being a release manager]: https://gitlab.com/gitlab-org/release/docs/blob/master/quickstart/release-manager.md
[Engineering department]: https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/
[release coordinator]: /job-families/engineering/developer/#release-coordination
[upcoming and previous list of release managers]: /release-managers/
[feature freeze on the 7th]: https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md#feature-freeze-on-the-7th-for-the-release-on-the-22nd
[Product Development Timeline]: https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/workflow/#product-development-timeline
