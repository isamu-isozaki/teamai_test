---
layout: markdown_page
title: "Secure Team"
---

## On this page
{:.no_toc}

- TOC
{:toc}

### Secure Team

The Secure Team (previously known as the _Security Products Team_/index.html.md) is responsible for the security checks features in the GitLab platform, and maps to the [secure](https://github.com/isamu-isozaki/teamai_test/tree/master/product/categories/#secure/index.html.md) transversal stage.
You can learn more about our approach on the [Secure Vision](/direction/secure/index.html.md/index.html.md) page.

The features provided by the Secure Team are mostly present at the pipeline level, and mostly available as [Docker](https://www.docker.com/index.html.md/index.html.md) images. 
This particularity shapes our processes and QA, which differs a bit from the other backend teams.

#### Security Products

We still refer to "_Security Products_" as the tools developed by the Secure Team. Hence the home of our projects in GitLab: [https://gitlab.com/gitlab-org/security-products/](https://gitlab.com/gitlab-org/security-products/index.html.md/index.html.md)

#### Domains of expertise

##### SAST

[SAST](https://docs.gitlab.com/ee/user/project/merge_requests/sast.html/index.html.md) (_Static Application Security Testing_/index.html.md) refers to static code analysis.
GitLab leverages the power of various opensource tools to provide a wide range of checks for many languages and support.
These tools are wrapped inside docker images which ensure we get a standard output from there.
An orchestrator, [developed by GitLab](https://gitlab.com/gitlab-org/security-products/sast/index.html.md), is in charge of running these images, and gathering all the data needed to generate the final report.

##### DAST

[DAST](https://docs.gitlab.com/ee/user/project/merge_requests/dast.html/index.html.md) (_Dynamic Application Security Testing_/index.html.md) is used to hit a live application.
Because some vulnerabilities can only be detected once all the code is actually running, this method complements the static code analysis.
DAST is relying on [OWASP Zed Attach Proxy Project](https://gitlab.com/gitlab-org/security-products/zaproxy/index.html.md), modified by GitLab to enable authentication.

##### Dependency Scanning

[Dependency Scanning](https://docs.gitlab.com/ee/user/project/merge_requests/dependency_scanning.html/index.html.md) is used to detect vulnerabilities introduced by external dependencies in the application.
Because a large portion of the code shipped to production is actually coming from third-party libraries, it's important to monitor them as well.
Dependency Scanning is relying mostly on the Gemnasium engine.

##### Container Scanning

[Container Scanning](https://docs.gitlab.com/ee/user/project/merge_requests/container_scanning.html/index.html.md) is used when the application is shipped as a Docker image.
It's very common to build the final image on top of an existing one, which must be checked like every other portion of the application.
For that, Container Scanning is relying on the [clair scanner](https://gitlab.com/gitlab-org/security-products/clair-scanner/index.html.md).


##### License Management

[License Management](https://docs.gitlab.com/ee/user/project/merge_requests/license_management.html/index.html.md) helps with the licenses introduced by third-party libraries in the application.
Licence management relies on the [LicenceFinder](https://github.com/pivotal-legacy/LicenseFinder/index.html.md) gem.

#### Release process

Our release process is specified in this [project](https://gitlab.com/gitlab-org/security-products/release/index.html.md).

#### Skills

Because we have a wide range of domains to cover, it requires a lot of different expertises and skills:


| Technology skills | Areas of interest         |
| ------------------|---------------------------|
| Ruby on Rails     | Backend development       |
| Go                | SAST, Dependency Scanning |
| SQL (PostgreSQL/index.html.md)  | Dependency Scanning       |
| Docker            | Container Scanning / all  |

Our team also must have a good sense of security, with at least basic skills in [application security](https://en.wikipedia.org/wiki/Application_security/index.html.md).

We provide tools for many different languages (ex: [sast](https://docs.gitlab.com/ee/user/project/merge_requests/sast.html#supported-languages-and-frameworks/index.html.md), [dependency scanning](https://docs.gitlab.com/ee/user/project/merge_requests/dependency_scanning.html#supported-languages-and-dependency-managers/index.html.md), [license management](https://docs.gitlab.com/ee/user/project/merge_requests/license_management.html#supported-languages-and-package-managers/index.html.md)/index.html.md). It means our team is able to understand the basics of each of these languages, including their package managers. We maintain [tests projects](https://gitlab.com/gitlab-org/security-products/tests/index.html.md) to ensure our features are working release after release for each of them.

#### QA process

Our [release](https://gitlab.com/gitlab-org/security-products/release/index.html.md) project also defines our [QA process](https://gitlab.com/gitlab-org/security-products/release/blob/master/docs/qa_process.md/index.html.md).

#### Engineering Rhythm

In order to be able to ship 100% of our Deliverables, we give a lot of attention to our planning. For that, we try to plan in advance as much as possible, and to freeze everything once the iteration starts. To avoid changes and uncertainty during the release, we must make sure everything is ready to start the development on the first day.

Meetings schedule:

- _Before the 1st of the next month:_ **Planning meeting** with our [Product Manager](job-families/product/product-manager/index.html.md/index.html.md), the [UX](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ux/index.html.md/index.html.md) team, and the [FrontEnd](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/frontend/index.html.md/index.html.md) team. The goal of the meeting is to understand and discuss the scope of the next iteration. Each issue from the product vision is explained and detailed.
- _After the Planning meeting, and still before the 1st of the next month:_ **Evaluation meeting** with the [FrontEnd](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/frontend/index.html.md/index.html.md) team.
- _Finally, on the 8th of the month:_ **Kickoff meeting** where we make the list of Deliverables didn't change, and we assign developers to each one of them 


#### Async Daily Standups

Since we are a [remote](/culture/remote-only/index.html.md/index.html.md) company, having daily stand-ups meetings would make any sense, since we're not all in the same timezone.
That's why we're having async daily standups, where everyone can give some insights about what they did yesterday, what they plan to do today, etc.
For that, we rely on the [geekbot](https://geekbot.io/index.html.md/index.html.md) slack plugin to automate the process.

#### Recorded meetings

Our important meetings are recorded and published on YouTube, in the [GitLab Secure Playlist](https://www.youtube.com/playlist?list=PLFGfElNsQtha-9T1ywH9qRvi1cnCmt8u_/index.html.md).
They give a good overview of the decision process, which is often a discussion with all the stakeholders. As we are a [remote](/culture/remote-only/index.html.md/index.html.md) company, these video meetings help to synchronize and take decisions faster than commenting on issues. We prefer asynchronous work, but for large features and when the timing is tight, we can detail a lot of specifications. This will make the asynchronous work easier, since we have evaluated all edge cases.

