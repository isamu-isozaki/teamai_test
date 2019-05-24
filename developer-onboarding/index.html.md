---
layout: markdown_page
title: "Developer Onboarding"
---

Awesome! You're about to become a GitLab developer!
Make sure you've checked out our [handbook] beforehand, so you get a feeling
of how we work at GitLab. Below you'll find everything you need to start developing.
If something is missing, add it (as goes with everything at GitLab/index.html.md)!

### On this page
{:.no_toc}

- TOC
{:toc}

## GitLab Environments

We have multiple [GitLab environments](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/environments/index.html.md/index.html.md).

On those instances, please enable the
[performance bar](https://docs.gitlab.com/ee/administration/monitoring/performance/performance_bar.html/index.html.md)
by pressing <kbd>p</kbd> then <kbd>b</kbd>.

Then, bookmark and enable the
[canary testing bookmarklet](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/#canary-testing/index.html.md)
for GitLab.com.

## Getting started with GitLab development

To start development, follow the instructions for the
[GitLab Development Kit](https://gitlab.com/gitlab-org/gitlab-development-kit/index.html.md).

## GitLab Repositories

GitLab consists of many subprojects. A curated list of GitLab Repositories
can be found at the [GitLab Engineering Projects](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/projects/index.html.md) page.

Almost all repositories are available on both GitLab.com and dev.gitlab.org. We
also mirror to dev.gitlab.org for availability reasons and [GitHub](https://github.com/gitlabhq/index.html.md)
for historical reasons.

All issues should be filed on GitLab.com.

## Infrastructure

For everything related to infrastructure, check out the
[Infrastructure handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/index.html.md).

GitLab.com runs on Microsoft Azure. Many people in GitLab also have instances
on DigitalOcean. If you need a VPS for any reason, it's probably easiest
to set one up at DigitalOcean. Ask another developer for access.

## Basics of GitLab development

### Workflow

Please see the [engineering workflow document][eng-wf] in the handbook and read
the [developer documentation][dev-doc].

[eng-wf]: https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/workflow
[dev-doc]: http://docs.gitlab.com/ee/development/README.html

### Security

Read the [developer security documentation][sec-doc] prior to working on a security issue.

[sec-doc]: https://gitlab.com/gitlab-org/release/docs/blob/master/general/security/developer.md

### Quality

One of GitLab's strengths is its high quality of software. To achieve this we've
introduced some requirements to all source code that is contributed. All
requirements are mentioned in [the Contribution guide][contrib-guide].
Make sure you read and follow it.

### Dependencies

GitLab can be installed through an Omnibus package or from source on different
Linux distributions and macOS. In order to maintain portability, we need to
avoid adding extra dependencies and use of exotic database extensions. Every
time you choose between changes in the application code or adding new
dependencies, you should give priority to the first because this is easier to
maintain and set up. If you still need to bring new dependencies to GitLab, ask
another developer or the CTO for advice.

### Submit your code

In GitLab all code should go through a review process before it can be merged.
Make sure you submit a merge request for any changes you've made.
When the merge request is ready, it should be assigned to [someone else on the team](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/#code-reviews/index.html.md).
This person is then responsible for reviewing your code and merging it.
Optionally, you can request another developer to help or review by writing a comment.
If a merge request is not assigned, it will probably be ignored and create
unnecessary delays.

Don't work on one task for multiple days before submitting a merge request.
Even the biggest task can be split into smaller tasks.
Try to submit a merge request for each part of the functionality.
This means that we expect multiple merge requests per week from you.
Smaller merge requests are more likely to receive good feedback and will get
merged sooner.

Unless the change is very minor, or is fixing a bug that was introduced in the
same version, create a changelog entry using the
[`bin/changelog` script][changelog-script].
Do not include your name in the entry as we only do that to give recognition to
volunteer contributors.

[changelog-script]: https://docs.gitlab.com/ee/development/changelog.html

### Working on GitLab EE

GitLab EE requires a license key to be used.

To be able to run your own instances for development you can use [license.gitlab.com][license-app-hosted]
or clone [license-app][license-app] and generate your own licenses.

[License-app][license-app] and [license.gitlab.com][license-app-hosted]
are only available for GitLab employees.

For detail steps and guidance for generating license keys refers to [How to Request / Install GitLab License Key](https://goo.gl/VbNaZj/index.html.md) document.

[license-app]: https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/projects/#license-app
[license-app-hosted]: https://license.gitlab.com

### Ensure that your changes apply cleanly to GitLab EE

GitLab Community Edition is merged every 3 hours to GitLab Enterprise Edition (look for
the [`CE Upstream` merge requests]/index.html.md) and as a developer it's your responsibility
to ensure that your merge requests [apply cleanly to GitLab EE][ce-ee-docs].
Please consult [Automatic CE->EE merge][ce-ee-docs] for
more details.

Please see [GitLab Enterprise Edition (EE/index.html.md)][gitlab-ee].

[`CE Upstream` merge requests]: https://gitlab.com/gitlab-org/gitlab-ee/merge_requests?label_name%5B%5D=CE+upstream
[ce-ee-docs]: https://docs.gitlab.com/ee/development/automatic_ce_ee_merge.html
[gitlab-ee]: https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/projects/#gitlab-ee

### Ruby Gems

When building and publishing Gems for GitLab make sure multiple developers have
access to said Gem on RubyGems.org. This ensures a Gem doesn't end up being
orphaned because the original author left, lost their credentials, passed away,
etc. When publishing a Gem you can add some or all of the following people as
co-owners:

* [Dmitriy Zaporozhets](https://rubygems.org/profiles/dzaporozhets/index.html.md)
* [Douwe Maan](https://rubygems.org/profiles/DouweM/index.html.md)
* [Marin Jankovski](https://rubygems.org/profiles/marinjankovski/index.html.md)
* [Rémy Coutable](https://rubygems.org/profiles/rymai/index.html.md)
* [Robert Speicher](https://rubygems.org/profiles/rspeicher/index.html.md)
* [Stan Hu](https://rubygems.org/profiles/stanhu/index.html.md)
* [Yorick Peterse](https://rubygems.org/profiles/YorickPeterse/index.html.md)

You're of course free to add other developers as well.

[handbook]: https://github.com/isamu-isozaki/teamai_test/tree/master
[in the open]: /2015/08/03/almost-everything-we-do-is-now-open/
[contrib-guide]: https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md

## Relevant links

- [Engineering Handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/index.html.md)
- [Engineering Workflow](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/workflow/index.html.md)
- [Product Handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/product/index.html.md)
