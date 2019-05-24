---
layout: markdown_page
title: "Quality"
---

## On this page
{:.no_toc}

- TOC
{:toc}

# Quality Team

## Child Pages
* [On-boarding](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/quality/onboarding/index.html.md)
* [Project Management](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/quality/project-management/index.html.md)
* [Test Engineering](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/quality/test-engineering/index.html.md)
* [Issue Triage](https://github.com/isamu-isozaki/teamai_test/tree/master/quality/issue-triage/index.html.md/index.html.md)

## Vision

Ensure that GitLab consistently releases high-quality software across the growing suite of products, developing software at scale without sacrificing quality, stability or velocity. 
The quality of the product is our collective responsibility. The quality department makes sure everyone is aware of what the quality of the product is, empirically.

To execute on this vision, we categorize our efforts into the following areas. 

### Culture of Quality 

Bake in a culture of quality from within and early in the development process.
  * Review product requirements and designs to identify risk and steer the team on quality strategy.
  * Partner with all engineering teams to ensure that our products have testability built in that can be leveraged by the testing infrastructure.
  * Be a champion for better software design, promote proper testing practices and bug prevention strategies.

Create a feedback loop of Quality.    
  * Create a feedback loop from test results to improve test gaps in our test suites.
  * Conduct test gap analysis from bugs that are filed by GitLab users.
  * Be a sounding-board for our end users and non-engineering stakeholders by integrating their feedback on quality into the development process.
  
### Test Automation Expertise

Own and build out our automated testing frameworks and infrastructure.
  * Contribute to our integration automated testing framework.
  * Own and expand end-to-end automated testing framework [GitLab QA].
  * Own and build third-party service testing capabilities.
  * Own and build our Continuous Integration & Delivery test pipelines.
  * Coach developers (internal & external/index.html.md) on contributing to [GitLab QA] test scenarios. 

Continuously improve GitLab test coverage, reliability and efficiency.
  * Groom the [test pyramid](https://martinfowler.com/bliki/TestPyramid.html/index.html.md) coverage and ensure that the right tests run at the right place.
  * Improve on the duration and de-duplication of the GitLab test suites.
  * Improve stability by eliminating flaky tests and transient failures. 
  * Improve test results tracking and reporting mechanisms that aid in triaging test results.

### Engineering Productivity 

Continuously improve the release process where the Quality is a stakeholder.
  * Eradicate any manual quality steps in the release process.
  * Ensure that we have a repeatable and consistent Quality process for every release.

Make metric-driven suggestions to improve engineering processes and developer productivity.
  * Build automated measurements and dashboards to gain insights into developer productivity and understand what is working and what is not.
    * See [GitLab Insights] proiect.
    * Make suggestions for improvements, monitor the results and iterate.
  * Increase contributor and developer productivity by improving the development setup, workflow, processes, and tools.
    * See [GitLab Triage] proiect.
  * Identify architectural and [backstage](/job-families/specialist/backstage/index.html.md/index.html.md) improvements as well as technical debt.
  
## OKRs

See [OKRs](/okrs/index.html.md/index.html.md)

## Team

The current team consists of the follow individuals with their area of expertise:
* [Rémy Coutable](/team/#rymai/index.html.md): General expert.
* [Lin Jen-shin](/team/#godfat/index.html.md): CE & EE Backend, CI, Developer Productivity.
* [Mark Fletcher](/team/#markglenfletcher/index.html.md): Issue triage, Developer Productivity.
* [Dan Davison](/team/#sircapsalot/index.html.md): Selenium, Docker, Maintainer of the [Selenium Docker project](https://github.com/SeleniumHQ/docker-selenium/index.html.md).
* [Mark Lapierre](/team/#mdlap/index.html.md): Test Automation Strategy for **Create**, Cognitive Psychology (Ph.D./index.html.md)
* [Ramya Authappan](/team/#/index.html.md): Test Automation Strategy for **Plan**
* [Sanad Liaquat](/team/#/index.html.md): Test Automation Strategy for **Manage**

### Long term

Our long-term direction is to have sub-teams under Quality aligned to either a cross-functional group or focused on building productivity tooling. 

#### Dev stage cross-functional team

Engineers in this area are embedded in the **Dev** cross-functional group. 
They are responsible for coverage of **Dev** stage features [product category](https://about.gitlab.comhttps://github.com/isamu-isozaki/teamai_test/tree/master/product/categories/index.html.md/index.html.md). 

* **Create:** Code Review, Merge Requests, Diffs, Approvals, Web IDE, Wikis, Snippets
  * Source Control: Git Operations, Gitaly
  * Third-party Source Control: Github, BitBucket
* **Plan:** Project Management, Issues, Boards, Epics, Roadmap, Markdown, Labels, Search, Todos, Weights, Due dates
  * Third-party Chat Integrations: Slack, Mattermost
  * Third-party Project Management: Jira and etc
  * Third-party Communication: Email
* **Manage:** Configuration, Admin, Groups & Subgroups, i18n
  * Third-party Authentication: Oauth, LDAP, SAML

#### Ops stage cross-functional team

Engineers in this area are embedded in the **Ops** cross-functional group. 
They are responsible for coverage of **Ops** stage features [product category](https://about.gitlab.comhttps://github.com/isamu-isozaki/teamai_test/tree/master/product/categories/index.html.md/index.html.md).  

* **Verify:** CI tools
  * Third-party CI: Jenkins, Bamboo, etc.
* **Package:** Registry Integration for containers, binaries
* **Release:** Continuous Delivery, Review Apps, Release Automation, Feature Flags, Pages
* **Configure:** Application, Infrastructure, Auto DevOps
* **Monitor:** APM, Logging, Tracking
* **Secure:** Security Products
  
#### Experience and Performance team
* Load & Performance tests
* Browser and mobile browser coverage 
  * Functionality testing against all supported customer browsers
  * Visual regression testing with real browsers

#### Developer Productivity team
* Productivity tooling
* Issue Triage bot, Community Triage bot
* Production bots aka Functional Monkey
* Pipeline Change Detection, Test Dependency Mapping
* Quality Metrics with Gitlab-insights
  
## Test Automation

The GitLab test automation framework is distributed across two projects: 
* [GitLab QA], the test orchestration tool
* The scenarios and spec files within the GitLab main codebase.

### Architecture overview

See the [GitLab QA Documentation](https://gitlab.com/gitlab-org/gitlab-qa/blob/master/docs/index.html.md).

Our current architecture overview is [here](https://gitlab.com/gitlab-org/gitlab-qa/blob/master/docs/architecture.md/index.html.md).

### Installation & Execution

* Install and set up the [GitLab Development Kit](https://gitlab.com/gitlab-org/gitlab-development-kit/index.html.md)
* Install and run [GitLab QA] to kick off test execution. See the README for more information on how to run the test framework.
  * The spec files (test cases/index.html.md) can be found in the [GitLab main codebase](https://gitlab.com/gitlab-org/gitlab-ce/tree/master/qa/index.html.md)

## Development process quality

* Merge request checklist
  * The default template is saved at the project level and can be viewed/edited in Settings -> Repository 
  * There are also [specific templates for Database and Documentation changes](https://gitlab.com/gitlab-org/gitlab-ce/tree/master/.gitlab/merge_request_templates/index.html.md)
  
## Team Retrospective

The Quality team holds a once-a-month 30 minute meeting for the team's retrospective. This happens one week before the public GitLab team retrospective. 
The retrospective is for us to reflect as a team; what went well, what went wrong and how can we improve. Emotions are not only allowed in retrospectives, they are encouraged, this is a safe environment that allows the team to discuss freely. The meeting is private only to the Quality team, however, the agenda items are public within GitLab.
The agenda items are populated ahead of time, come meeting time, we discuss the items and identify a positive plan of action as needed. 
Important findings here can make its way into the public GitLab team retrospective in the following week.

It should be made clear that this is a retrospective and we encourage frank and sincere self-reflection. As a result, we allow passionate and emotional comments in the agenda but we ensure that they are steered towards a positive plan of action. 

Examples: 
> * `Person A`: I was really disappointed by the progress of `x` because `y`. => `Person B`: I noticed that too, in the future let's make sure that we prevent `y` from happening with this plan etc.
> * `Person C`: I was really angry that `this` happened, we are not being efficient here => `Person D`: should we change the way we currently do things, what improvements can be made.

The Quality team [retrospective agenda](https://docs.google.com/document/d/1omIImDFKfW2AgYH-Ng8IK2wIAZoyZBe_6QyYt02hgIM/edit#/index.html.md) is only available for viewing inside GitLab. 
The public team retrospective contains information that is open to the public.

## Release process overview

The release process follows [this set of templates](https://gitlab.com/gitlab-org/release-tools/tree/master/templates/index.html.md). Additional supporting docs about the release process can be found [here](https://gitlab.com/gitlab-org/release/docs/index.html.md/index.html.md).

* First Deployable RC
    * Automated tests are run against Staging and Canary
    * An Issue is created listing the QA tasks for this release candidate
        * The items from the Release Kickoff Doc are copied to the Issue and associated with the appropriate PM
        * The PM performs testing on staging and lists any issues found
        * Other changes related to bugs and improvements are gathered from a Git comparison of this release from the previous one
        * The Engineering teams confirms that these other changes come with tests or have been tested on staging
    * After 24 hours, assuming there are no blocking bugs found, the expectation is testing has completed and the release can proceed to deploy to production
    * Example: [10.6 RC1 QA Task](https://gitlab.com/gitlab-org/release/tasks/issues/116/index.html.md)
* Subsequent RCs
    * Automated tests are run against Staging and Canary
    * An issue is created listing the QA tasks for this release candidate
        * The changes that had been merged in since the previous release are captured in a QA task Issue, associated with the appropriate engineer
        * The engineer performs testing on staging, or confirms that the change came with automated tests that are passing
    * After 12 hours, assuming there are no blocking bugs found, the expectation is testing has completed and the release can proceed to deploy to production
    * Example: [10.6 RC6 QA Task](https://gitlab.com/gitlab-org/release/tasks/issues/135/index.html.md)
* Final Release
    * Automated tests are run against Staging and Canary as a sanity check
    * Since no changes should have been included between the last RC and the release-day build, no additional testing or review should be required.
    * The final release candidate is deployed to production

## Recruiting
* Information regarding the technical quizzes and assignments that are sent to candidates can be found [here](https://gitlab.com/gitlab-com/people-ops/applicant-questionnaires/blob/master/automation-engineer.md/index.html.md) (GITLAB ONLY/index.html.md)
* The steps of the hiring process can be found [here](https://gitlab.com/gitlab-com/people-ops/hiring-processes/blob/master/engineering.md/index.html.md) (GITLAB ONLY/index.html.md)

## Common Links

* [**Public Issue Tracker (for GitLab CE/index.html.md)**](https://gitlab.com/gitlab-org/gitlab-ce/index.html.md);
  please use confidential issues for topics that should only be visible to team members at GitLab.
* Chat channels; please use chat channels for questions that don't seem appropriate to use the issue tracker for.
  * [#quality](https://gitlab.slack.com/messages/quality/index.html.md): for general conversation about GitLab Quality
  * [#triage](https://gitlab.slack.com/messages/triage/index.html.md): general triage team channel.
  * [#mr-coaching](https://gitlab.slack.com/archives/mr-coaching/index.html.md): for general
    conversation about Merge Request coaching.
  * [#opensource](https://gitlab.slack.com/archives/opensource/index.html.md): for general
    conversation about Open Source.
    
## Other Related Pages

* [Engineering](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/index.html.md)
* [Issue Triage](issue-triage/index.html.md)
* [Issue Triage Policies](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/issue-triage/index.html.md)
* [Performance of GitLab](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/performance/index.html.md)
* [Monitoring of GitLab.com](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/monitoring/index.html.md)
* [Production Readiness Guide](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md/index.html.md)
* [Quality Team Documentation](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/quality/team/index.html.md)

[GitLab QA]: https://gitlab.com/gitlab-org/gitlab-qa
[GitLab Insights]: https://gitlab.com/gitlab-org/gitlab-insights
[GitLab Triage]: https://gitlab.com/gitlab-org/gitlab-triage
