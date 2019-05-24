---
layout: markdown_page
title: "Engineering"
---

## Communication<a name="reach-engineering"></a>

- [**Public Issue Tracker (for GitLab CE/index.html.md)**](https://gitlab.com/gitlab-org/gitlab-ce/index.html.md); please use confidential issues for topics that should only be visible to team members at GitLab.
- [**Chat channel**](https://gitlab.slack.com/?redir=%2Farchives%2Fdevelopment/index.html.md); please use the `#development`, `#vpe`, `#frontend`, `#infrastructure`, `#ci-cd`, and `#support` chat channels for questions that don't seem appropriate to use the issue tracker or the internal email address for.
- VPE Office Hours: Each week [Eric Johnson](https://gitlab.com/edjdev/index.html.md) holds open office hours on Zoom for questions, feedback, and handbook changes. It's typically Thursdays at 9am PST for 1 hour, but see his calendar for current times.

## On this page
{:.no_toc}

- TOC
{:toc}

## Other Related Pages

- [Developer onboarding](https://github.com/isamu-isozaki/teamai_test/tree/master/developer-onboarding/index.html.md)
- [Engineering Career Development](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/career-development/index.html.md)
- [Engineering Management](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/management/index.html.md)
- [Engineering Workflow](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/workflow/index.html.md)
- [Frequently Used Projects](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/projects/index.html.md)
- [Issue Triage Policies](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/issue-triage/index.html.md)
- [Critical Security Release Process](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/critical-release-process/index.html.md)
- [Emergency Meeting Protocol](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/emergency-meeting-protocol/index.html.md)
- [Performance of GitLab](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/performance/index.html.md)
- [Monitoring of GitLab.com](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/monitoring/index.html.md)
- [Production Readiness Guide](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md/index.html.md)
- [Contributing to Golang projects](/courses/dev-101/index.html.md)
- [VPE Eric J's README](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/erics-readme/index.html.md)

## The Importance of Velocity

* The rate at which GitLab delivers new value to users in the form of features is a competitive advantage for the project and the company.
* As an open source project, people are welcome to fork us. However, in order to ensure that the community remain intact, and the bulk of energy is directed toward one verion of GitLab it is important to move fast so that any fork is quickly out of date.
* Companies tend to slow down as they grow. It takes deliberate effort to prevent this, so it must always be top of mind.
* Once you slow down, it is incredibly painful to speed back up again.

## Velocity over predictability

We optimize for shipping a high volume of user/customer value with each release. We do want to ship multiple major features in every monthly release of GitLab. However, we do not strive for predictability over velocity. As such, we eschew heavyweight processes like detailed story point estimation by the whole team in favor of lightweight measurements of throughput like the number of merge requests that were included or rough estimates by single team members.

There is variance in how much time an issue will take versus what you estimated. This variance causes unpredictability. If you want close to 100% predictability you have to take two measures:

1. Invest more time in estimation to reduce that variance. The time spend estimating things could otherwise be used to create features.
1. Leave a reserve of time with unscheduled work so you can accommodate the variance. According to [Parkinson's law](https://en.wikipedia.org/wiki/Parkinson%27s_law/index.html.md) the work expands so as to fill the time available for its completion. This means that we're not adhering to our [iteration value](https://github.com/isamu-isozaki/teamai_test/tree/master/values/#iteration/index.html.md) and that for the next cycle our estimates for comparable features will be larger.

Both measures reduce the overall velocity of shipping features.
The way to prevent this is to accept that we don't want perfect predictability.
Just like our [OKRs](/okrs/index.html.md/index.html.md) are so ambitious that we expect to reach about 70% of the goal this is fine for shipping [planned features](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#ambitious-planning/index.html.md) too.

_Note:_ This does not mean we place zero value on predictability. We just optimize for velocity first.

## GitLab Repositories

GitLab consists of many subprojects. A curated list of GitLab Repositories can be found at the [GitLab Engineering Projects](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/projects/index.html.md) page.

When adding a repository please follow these steps:
1. Ensure that the project is under the [gitlab-org](https://gitlab.com/gitlab-org/index.html.md) namespace for anything related to the application or under the [gitlab-com](https://gitlab.com/gitlab-com/index.html.md) namespace for anything strictly company related.
1. [Add the project to the list of GitLab Repositories](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/doc/projects.md/index.html.md)
1. Add an MIT license to the repository. It is easiest to simply copy-paste the [MIT License](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/LICENSE/index.html.md) verbatim from the `gitlab-ce` repo.
1. Add a section titled "Developer Certificate of Origin and License" to `CONTRIBUTING.md` in the repository. It is easiest to simply copy-paste the [DCO + License section](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#developer-certificate-of-origin-license/index.html.md) verbatim from the `gitlab-ce` repo.
1. Add any further relevant details to the Contribution Guide. See [Contribution Example](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md/index.html.md).
1. Add a link to `CONTRIBUTING.md` from the project's `README.md`

## Engineering Departments & Teams

* [Dev Backend](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/dev-backend/index.html.md/index.html.md)
  * [Create](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/dev-backend/create/index.html.md/index.html.md)
  * [Distribution](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/dev-backend/distribution/index.html.md/index.html.md)
  * [Geo](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/dev-backend/geo/index.html.md/index.html.md)
  * [Gitaly](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/dev-backend/gitaly/index.html.md/index.html.md)
  * [Gitter](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/dev-backend/gitter/index.html.md/index.html.md)
  * [Manage](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/dev-backend/manage/index.html.md/index.html.md)
  * [Plan](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/dev-backend/plan/index.html.md/index.html.md)
* [Frontend](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/frontend/index.html.md/index.html.md)
* [Infrastructure](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/index.html.md/index.html.md)
  * [Database](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/database/index.html.md/index.html.md)
  * [Production](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/production/index.html.md/index.html.md)
* [Ops Backend](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ops-backend/index.html.md/index.html.md)
  * [CI/CD](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ops-backend/ci-cd/index.html.md/index.html.md)
  * [Monitoring](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ops-backend/monitoring/index.html.md/index.html.md)
  * [Secure](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ops-backend/secure/index.html.md/index.html.md)
* [Quality](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/quality/index.html.md/index.html.md)
* [Security](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/security/index.html.md/index.html.md)
* [Support](https://github.com/isamu-isozaki/teamai_test/tree/master/support/index.html.md/index.html.md)
* [UX](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ux/index.html.md)

## Starting new teams

Our product offering is growing rapidly. Occasionally we start new teams. Backend teams should map to our [product categories](https://github.com/isamu-isozaki/teamai_test/tree/master/product/categories/index.html.md/index.html.md). Backend teams also map 1:1 to [product managers](https://github.com/isamu-isozaki/teamai_test/tree/master/product/index.html.md/index.html.md).

A dedicated team needs certain skills and a minimum size to be successful. But that doesn't block us from taking on new work. This is how we iterate our team size and structure as a feature set grows:

1. **Existing Team:** The existing PM schedules issues for most appropriate existing engineering team
  * If there is a second PM for this new feature, they work through the first PM to preserve the 1:1 interface
1. **Shared Manager Team:** Dedicated engineer(s/index.html.md) are identifed on existing teams and given a specialty
  * The manager must do double-duty
    * Their title can reflect both specialties of their engineers _e.g._ Engineering Manager, Distribution & Packaging
    * Even if temporary, managing two teams is a valuable career opportunity for a manager looking to develop director-level skills
  * Each specialty can have its own process, for example: Capitalized team label, Planning meetings, Standups
1. **New Dedicated Team:**
  * Engineering Manager
  * Senior/Staff Engineer
  * Two approved fulltime vacancies
  * A dedicated PM

## Team Page Template

```markdown
## Vision

...

## Mission

...

## Team Members

The following people are permanent members of the [Blank] Team:

<%= direct_team(manager_role: 'Engineering Manager, [Blank]'/index.html.md) %>

## Stable Counterparts

The following members of other functional teams are our stable counterparts:

<%= stable_counterparts(role_regexp: /[,&] Blank/, direct_manager_role: 'Engineering Manager, [Blank]'/index.html.md) %>

## Common Links

 * Issue Tracker
 * Slack Channel
 * ...

 ## How to work with us

 ...

```


## Collaboration

To maintain our rapid cadence of shipping a new release every month, we must keep the barrier low to getting things done. Since our team is distributed around the world and therefore working at different times, we need to work in parallel and asynchronously as much as possible.

That also means that if you are implementing a new feature, you should feel empowered to work on the entire stack if it is most efficient for you to do so.

## Code Quality and Standards

We need to maintain code quality and standards. It's very important that you are familiar with the [Development Guides] in general, and the ones that relates to your group in particular:

- [UX Guides](https://docs.gitlab.com/ee/development/ux_guide/index.html/index.html.md)
- [Backend Guides](https://docs.gitlab.com/ee/development/README.html#backend-howtos/index.html.md)
- [Frontend Guides](https://docs.gitlab.com/ee/development/fe_guide/index.html/index.html.md)
- [Database Guides](https://docs.gitlab.com/ee/development/README.html#databases/index.html.md)

It is important to remember that quality is everyone's responsibility.  Everything you merge to master should be production ready.  Familiarize yourself with the [definition of done].

[Development Guides]: https://docs.gitlab.com/ee/development/README.html
[definition of done]: https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#definition-of-done

## Error Budgets

In Q3 of 2018 we are trying [SRE](https://en.wikipedia.org/wiki/Site_Reliability_Engineering/index.html.md)-like error budgets in [OKRs](/okrs/2018-q3/index.html.md/index.html.md) to incentivize risk management help and make GitLab.com ready for mission critical customer workloads.

Each backend and frontend development team will be responsible for preserving 100 points (or percent/index.html.md) of their budget this quarter. The severity of issues caused will subtract from their budget accordingly:

* ~S1: -30 points
* ~S2: -15 points
* ~S3: -6 points
* ~S4: -3 point

The Infrastructure team will perform attribution as part of the post-mortem process and record the results in the OKRs page.

## Engineering Led Initiatives

Engineering is the primary advocate for the performance, availability, and security of the GitLab project. Everyone in the engineering function should participate in the Product Management [prioritization process](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#product-process/index.html.md) to ensure that our project stays ahead in these areas. The following list should provide some guidelines around the initiatives that each engineering team should advocate for during their release planning:

- Review fixes from our support team. These issues are tagged with the `support-fix` label.  You can filter on open MRs [here](https://gitlab.com/gitlab-org/gitlab-ce/merge_requests?label_name%5B%5D=support-fix/index.html.md).
- Working on high priority issues as a result of [issue triaging](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/issue-triage/index.html.md/index.html.md). This is our commitment to the community and we need to include some capacity to review MRs or work on defects raised by the community.
- Improvements to the performance and scalability of a feature.  Again, the Product team should be involved in the definition of these issues but Engineering may lead here by clearly defining the recommended improvements.
- Improvements to our toolchain in order to boost efficiency.

## Rails by default, VueJS where it counts

Part of our engineering culture is to keep shipping so users and customers see significant new value added to GitLab.com or their self-managed instance. To support rapid development, we focus on Rails page views by default. When an area of the application sees significant usage, we typically rewrite those screens as a [VueJS](https://vuejs.org/index.html.md/index.html.md) single page app backed by our API, in order to maintain the best qualitative experience and quantitative performance.

## Demos

The idea that [working software is the primary measure of progress](http://agilemanifesto.org/principles.html/index.html.md) is one of the principles of agile software development. Demoing gets more eyes on the project to uncover bugs and reveal ambiguities in the product requirements. It's also a transparent and lightweight way to provide status to the rest of the organization. Developers should demo at least once a week with product managers present. Demo meetings should be kept to 30 minutes or less. The emphasis should be on the product requirements or acceptance criteria and less on the implementation details.

## Canary Testing

GitLab makes use of a 'Canary' environment, a series of servers to test the GitLab code base on prior to production deployment. The Canary environment contains code functional elements like web and git servers while sharing data elements such as sidekiq, database, and file storage with production. This allows UX code and most application logic code to be user tested under real world scenarios before being deployed.

The Canary environment is available for usage by enabling a cookie attribute of `gitlab_canary` when accessing `gitlab.com`. All engineers are encouraged to enable this flag and perform normal daily activities in order to spot issues and problems before deployment to the production environment. In order to facilitate the enabling of the canary cookie, a short javascript snipped is provided below to bookmark that toggles between states.

```javascript
javascript:void((function(d/index.html.md){document.cookie='gitlab_canary=' + (document.cookie.indexOf('gitlab_canary=true'/index.html.md) >= 0 ?  'false' : 'true'/index.html.md) + ';domain=.gitlab.com;path=/;expires=' + new Date(Date.now(/index.html.md) + 31536000000/index.html.md).toUTCString(/index.html.md); location.reload(/index.html.md);}/index.html.md)(document/index.html.md)/index.html.md);
```

## Code Reviews

Code reviews are mandatory for every merge request, you should get familiar and follow our [Code Review Guidelines](https://docs.gitlab.com/ee/development/code_review.html/index.html.md).

These guidelines also describe who would need to review, approve and merge your merge request.

### Reviewer

All GitLab developers can, and are encouraged to, perform code review on merge requests of colleagues and community contributors. If you want to review merge requests, you can wait until someone assigns you one, but you are also more than welcome to browse the list of open merge requests and leave any feedback or questions you may have.

To let other developers know that you are interested in performing code reviews, you can add this to your [team page entry](/team/index.html.md/index.html.md) by editing [`data/team.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/team.yml/index.html.md).

You can find someone to review your own merge requests by looking on the [team page](/team/index.html.md/index.html.md), or on the list of [GitLab Engineering Projects](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/projects/index.html.md/index.html.md), both of which are fed by `data/team.yml`.

You can also help community contributors get their merge requests ready, by becoming a [Merge Request Coach](/roles/merge-request-coach/index.html.md/index.html.md).

Note that while all developers can review all merge requests, the ability to _accept_ merge requests is restricted to maintainers.

### Maintainer

Maintainers are GitLab developers who are experts at code review, know the GitLab product and code base very well, and are empowered to accept merge requests in one or several [GitLab Engineering Projects](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/projects/index.html.md/index.html.md).

Every project has at least one maintainer, but most have multiple, and some projects (like GitLab CE and GitLab EE/index.html.md) have separate maintainers for frontend and backend.

Great developers are often also great reviewers, but code review is a skill in and of itself, and not every developer, no matter their seniority, will have had the same opportunities to hone that skill. It's also important to note that a big part of being a good maintainer comes from knowing the existing product and code base extremely well, which lets them spot inconsistencies, edge cases, or non-obvious interactions with other features that would otherwise be missed easily.

To protect and ensure the quality of the code base and the product as a whole, people become maintainers only once they have convincingly demonstrated that their reviewing skills are at a comparable level to those of existing maintainers.

As with regular reviewers, maintainers can be found on the [team page](/team/index.html.md/index.html.md), or on the list of [GitLab Engineering Projects](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/projects/index.html.md/index.html.md).

#### How to become a maintainer

As a reviewer, a great way to improve your reviewing skills is to participate in MRs. Add your review notes, pass them on to maintainers, and follow the conversation until the MR is closed. If a comment doesn't make sense to you, ask the commenter to explain further. If you missed something in your review, figure out why you didn't see it, and note it down for next time.

Reviewers need to make the case for their own maintainership status.

When:
 - the MR's they've reviewed consistently make it through maintainer review without significant additionally required changes;
 - the MR's they've written consistently make it through reviewer and maintainer review without significant required changes;
they can:

* create an MR to add the maintainership to their team page entry
* explain in the MR body why they are ready to take on that responsibility
* use specific examples of recent "maintainer-level" reviews that they have performed
* assign the MR to your manager and to the existing maintainers of the relevant product (GitLab CE, GitLab EE, etc/index.html.md) and area (backend, frontend, etc/index.html.md)

The MR's should not reflect only small changes to the code base, but also architectural ones and ones that create a full feature.

If the existing maintainers do not have significant objections, and if at least half of them agree that the reviewer is indeed ready, we've got ourselves a new maintainer!

The existing maintainers will also raise any areas for growth on the merge request. If there are many gaps, the reviewer will need to address these before asking for reconsideration.

If you'd like to work towards becoming a maintainer, discuss it in your regular 1:1 meetings with your manager. They will help you to identify areas to work on before following the process above.

## Resources for Development
{: #resources}

When using any of the resources listed below, some rules apply:

* Consider the cost and whether anything can be done to reduce the cost.
* You can boot up as many machines as you need.
* It is your responsibility to clean up after yourself; if a machine is not used, remove it.
* If you observe any resource that is running for long periods of time, ask the person responsible whether the machine is still in use.
* Prepend your username to any resource you start. Eg. if your name is Jane Doe, name the resource `janedoe-machine-for-testing`.

### Google Cloud Platform (GCP/index.html.md)

Every team member has access to a common project on [Google Cloud Platform](https://console.cloud.google.com/index.html.md/index.html.md). Please see the secure note with the name "Google Cloud Platform" in the shared vault in 1password for the credentials or further details on how to gain access.

Once in the console, you can spin up VM instances, Kubernetes clusters, etc. Please remove any resources that you are not using, since the company is [billed monthly](https://cloud.google.com/pricing/index.html.md/index.html.md). If you are unable to create a resource due to quota limits, file an issue on the [Infrastructure issue tracker](https://gitlab.com/gitlab-com/infrastructure/index.html.md).

### Digital Ocean (DO/index.html.md)

Every team member has access to the [dev-resources project](https://gitlab.com/gitlab-com/dev-resources/index.html.md/index.html.md) which allows everyone to create and delete machines on demand.

### Amazon Web Services (AWS/index.html.md)

In general, most team members do not have access to AWS accounts. In case you need an AWS resource, file an issue on the [Infrastructure issue tracker](https://gitlab.com/gitlab-com/infrastructure/index.html.md). Please supply the details on what type of access you need.

## DevOps Slack Channels

There are primarily two Slack channels which developers may be called upon to assist the production team
when something appears to be amiss with GitLab.com:

1. `#backend`: For backend-related issues (e.g. error 500s, high database load, etc./index.html.md)
2. `#frontend`: For frontend-related issues (e.g. JavaScript errors, buttons not working, etc./index.html.md)

Treat questions or requests from production team for immediate urgency with high priority.

## Reaction Rotation

See [the Reaction description](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/reaction/index.html.md/index.html.md).

## Release Managers

See [the Release Management description](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/release-management/index.html.md/index.html.md).
