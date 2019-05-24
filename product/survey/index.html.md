---
layout: markdown_page
title: Product Survey Outcomes
---

## On this page
{:.no_toc}

- TOC
{:toc}

## September

We got a lot of interesting feedback in this first survey!

Here on top I've summarised reponses. On the bottom we
have addressed every single question/remark that came up.

### Quantitative outcomes

64 responses, 40 from sales

#### What is the best 'selling' feature of GitLab? Why?

1. 25x: CI integrated with SCM
1. 24x: Single application for entire lifecyle
1. 4x: SCM
1. Rest: Approvals, HA, Security

#### What feature / change are (potential/index.html.md) customers most excited about? Why?

Number one and two had the plurality of the replies here.
Almost every feature was mentioned at least once.

1. Security features
1. Issues (incl. portfolio management/index.html.md), CI
1. Kubernetes
1. Almost every other feature in GitLab

#### What should we be working on, that we're not currently (or are planning to/index.html.md)? Why?

There seems to be a lack of awareness on what we're building in Plan, this is
addressed below, many things that were mentioned are in progress or planned for
the near-term future.

1. Issues (incl. portfolio management/index.html.md)
1. SCM / Code review
1. HA
1. Everything else

#### What are we doing product-wise that we shouldn't be doing? Why?

No consensus whatsoever, but some highlights:

- Spend less time on X, where X is currently dominated by other players in the market (JIRA, security tools, AutoDevops/index.html.md)
- Building out more breadth
- Adding features to Core/Starter

### Conclusions and actions

#### There is a lack of insight in what we're building

We now have a separate vision page for each stage in the DevOps lifecycle.
You can find them as `/direction/[name of stage]`:

- [/direction/manage](/direction/manage/index.html.md)
- [/direction/plan](/direction/plan/index.html.md)
- [/direction/create](/direction/create/index.html.md)
- [/direction/verify](/direction/verify/index.html.md)
- [/direction/package](/direction/package/index.html.md)
- [/direction/release](/direction/release/index.html.md)
- [/direction/configure](/direction/configure/index.html.md)
- [/direction/monitor](/direction/monitor/index.html.md)
- [/direction/secure](/direction/secure/index.html.md)

We will take the time to regularly present these in sales meetings,
and other occassions that can be easily shared.

#### It's unclear how we make decisions

On each of the DevOps stage pages linked directly above there is (or shortly will be/index.html.md)
section on how we prioritize and make decisions (given that this is not the same for each team/index.html.md).

We will also be repeating this survey every month, and publishing the results here,
and in a presentation.

We're looking into ways of gaining more insight from shared SalesForce links.
Today, the Create team uses them directly in their RICE scoring,
but looking at all links ever shared has revealed them to be a very noisy signal:
The majority of issues with salesforce links, only have a single link. There is a
handful of outliers that have 10-16 salesforce links, some of which are issues
that are scoped too broadly (e.g. integrate with X/index.html.md), whereas others are already
being worked on (group merge requests/index.html.md).

### Detailed answers to further comments

#### What should we be working on, that we're not currently (or are planning to/index.html.md)? Why?

##### We should work more on issues / portfolio management / requirements management / should make it better than JIRA

We are! You can see our full vision and plans here:

[Portfolio management](https://gitlab.com/groups/gitlab-org/-/roadmap?scope=all&utf8=�&state=opened&label_name[]=Plan&label_name[]=portfolio%20management&layout=QUARTERS/index.html.md)

[Project management (issues, boards, labels, milestones/index.html.md)](https://gitlab.com/groups/gitlab-org/-/roadmap?scope=all&utf8=�&state=opened&label_name[]=Plan&label_name[]=project%20management&layout=QUARTERS/index.html.md)

[Jira integration](https://about.gitlab.com/direction/#jira-integration/index.html.md)

[We are discussing requirements management](https://gitlab.com/gitlab-org/gitlab-ee/issues/7024/index.html.md)

##### HA out of the box should be better for everyone (Cloud Native doesn’t work yet for everyone/index.html.md)

xx

##### We should make further improvements to Geo

Andreas: We are! We are currently working on a roadmap for 2019. For a high-level perspective on what we want to do, see "What to expect from Geo in the near future" in [this recent Geo blog post](https://about.gitlab.com/2018/09/14/how-we-built-gitlab-geo/index.html.md/index.html.md).

##### Notifications need to be better

Andreas: We agree. There is a cross-team effort working towards improving activities/todos/notifications, see [Merge todos into notifications with pinned and unpinned notification sets](https://gitlab.com/gitlab-org/gitlab-ce/issues/48787/index.html.md). There’s also a dedicated Slack channel: [https://gitlab.slack.com/messages/C9CMR2EP4](https://gitlab.slack.com/messages/C9CMR2EP4/index.html.md).

##### Permissions for CI/CD

xx

##### Audit logs

Andreas: We agree, and this is planned for 2019. See the epic on [Auditing and data management improvements](https://gitlab.com/groups/gitlab-org/-/epics/81/index.html.md). We will also cover ideas in an upcoming blog post.

##### Dependency management

Fabio: we started working on it as part of the Secure stage ([dependency scanning](https://docs.gitlab.com/ee/user/project/merge_requests/dependency_scanning.html/index.html.md) and [license management](https://docs.gitlab.com/ee/user/project/merge_requests/license_management.html/index.html.md)/index.html.md), there is also a [proposal](https://gitlab.com/gitlab-org/gitlab-ee/issues/7476/index.html.md) to make dependency management first-class.

##### More dashboards and reports for top-level management

Andreas: Agree. I recently added [Smart dashboards](https://gitlab.com/groups/gitlab-org/-/epics/365/index.html.md) as 2019 vision. Right now it’s still generic, and I’d love to get further input on what we should work on in 2019 besides personal and project.

Fabio: we are introducing [group-level security dashboard](https://gitlab.com/gitlab-org/gitlab-ee/issues/6709/index.html.md) that will include data for Directors and CxO.

[See analytics ideas here](https://about.gitlab.com/direction/#analytics/index.html.md). In particular, we want to have a variety of charts in a [generic dashboard with lots of chart types](https://gitlab.com/groups/gitlab-org/-/epics/313/index.html.md), including those for executive-level / senior leadership consumption.

##### Integrate Gitter

We're working on this, see [our Gitter roadmap](https://gitlab.com/groups/gitlab-org/-/roadmap?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Gitter/index.html.md).

##### Better support for non-developer workflows (designers, writers/index.html.md)

Andreas: Yes! I think we have an enormous potential here, especially for roles that are very close to the development workflow. Read: Designers, Technical writers. I plan to discover how we can support Designers needs better in our product in 2019. There will be a new product category "Product Design Management" planned for 2019.

Fabio: we want to support security teams as first-class users (e.g., default view to security dashboard/index.html.md)

##### Custom roles / permissions

Jeremy: we’re still immensely reluctant to add fully custom roles to GitLab. It adds a lot of complexity to the product, confuses our documentation, and adds an extra layer of configuration that we still don’t feel is worth the maintenance required. The underlying problem (our permissions framework isn’t flexible enough, esp. For rules-heavy enterprises/index.html.md) still demands a solution:

* We’ll continue building out feature-level configuration. This is less risk and we’re able to ship these changes faster.

* We’re considering a feature to make feature-level configuration more flexible, called Policies. This would be an EE feature that lets instances restrict what the various roles can do.

##### Better integration between Salesforce / GitLab / all internal apps

We want this as well. We're reevaluating whether we have capacity to work on this
in Q4.

##### GVFS

We have had conversations with Microsoft about GVFS and are following its development closely. There are a number of [considerations](https://gitlab.com/groups/gitlab-org/-/epics/93#considerations/index.html.md) that prevent using GVFS in most organizations today even if GitLab supported the GVFS protocol. Namely:

* the need to run a custom fork of the Git binary on every client, and

* the need to run a file system driver which only exists for Windows.

Most importantly we have higher priorities which are needed by many customers, namely Gitaly HA which is critical to the Cloud Native project, GitLab.com and the horizontal scalability of GitLab. Related to this is the deduplication of objects across fork networks.

##### More depth to core products: SCM, CI, issues (answered above/index.html.md)

Jason: See answer for "We should build more depth" below.

##### More continuous delivery work

Jason: I was hired as PM for CD, so the organization is taking investment in this seriously, and the work for the 2019 roadmap (and beyond/index.html.md) was just published [here](https://about.gitlab.com/direction/release/index.html.md). Feedback is of course welcome, and we now have a plan in place where we can go after strategic solutions in the space. Improving our CDRA analyst performance is a big part of this and you can see that reflected in the strategic items in the roadmap.

##### Build a training platform, like trailhead for SFDC

This is one for customer success!

##### Better search (global search/index.html.md)

Definitely agree. We want to deliver a global, performant search for GitLab in 2019, including a [command palette](https://gitlab.com/groups/gitlab-org/-/epics/255/index.html.md) for common tasks.

[We want to get Elasticsearch on GitLab.com and then deepen and broaden global search capabilities.](https://about.gitlab.com/direction/#search/index.html.md)

##### Integrate with Trello

We have a very [basic integration with Trello](https://docs.gitlab.com/ee/integration/trello_power_up.html/index.html.md), and would [welcome contributions](https://gitlab.com/gitlab-org/gitlab-ce/issues/44562/index.html.md).

##### Better support for fully offline instances - can’t run Auto DevOps + SAST

Fabio: there any many technical limitations that actually prevent it to be done, but we want to work on this (see [issue](https://gitlab.com/gitlab-org/gitlab-ee/issues/4742/index.html.md)/index.html.md)

##### Dashboard for license management

Fabio: we have a [proposal](https://gitlab.com/gitlab-org/gitlab-ee/issues/7149/index.html.md) to manage licenses at group-level.

##### Proprietary security capabilities, not just open source

Fabio: we already have Gemnasium as part of our security features for dependency scanning, and we are considering adding more but we also don’t want to provide too many integrations since we are a [single application](https://about.gitlab.comhttps://github.com/isamu-isozaki/teamai_test/tree/master/product/single-application/index.html.md)

##### Code analytics

xx

##### Something that is more competitive with artifactory

xx

##### More audit

Andreas: We agree, and this is planned for 2019. See the epic on [Auditing and data management improvements](https://gitlab.com/groups/gitlab-org/-/epics/81/index.html.md). We will also cover ideas in an upcoming blog post. Also see [Audit logs](#heading=h.vlfwmryozqfy/index.html.md) further up.

##### Better support for Windows shops

xx


#### What are we doing product-wise that we shouldn't be doing? Why?

##### Auto Devops is not very good, doesn’t work in practice / complex customer scenarios. We should spend less time on it

Andreas: Note, there is also [Making auto devops easier / better](#heading=h.8jrz4urkzh1u/index.html.md) above.

##### Should be easier to make product prioritize things

Talk directly with the product manager of the related DevOps stage.
If this doesn't work, reach out directly to Job or Mark.

##### We should build more depth

The Create team is working to significantly improve the depth of support for code reviews and approvals for complex real world situations where there are large changes, multiple rounds of review and more.

Andreas: On the Manage team, we are planning the same. While we are extending our range of [product categories in 2019](https://gitlab.com/gitlab-com/www-gitlab-com/merge_requests/14277/diffs/index.html.md), improving the experience and details of our product is a major part of our plans moving forward.

Jason: We are focusing on this this year for [release](https://about.gitlab.com/direction/release/index.html.md)/[verify](https://about.gitlab.com/direction/verify/index.html.md); both have the below theme for the coming year to try to focus on how we solve problems in deeper ways not just be adding more breadth.

❤� **More Complete (Minimally Lovable/index.html.md) Features to Solve Complex Problems**

V1 feature iterations are how we build software, but at the same time we need to continue to curate those features that have proven their value into complete, lovable features that exceed our users expectations. We will achieve this by growing individual features, solving scalability challenges that larger customers see, and providing intelligent connections between individual features. Doing this lets us solve deeper, more subtle problem sets and - by being focused on real problems our users face - we'll leave the competition behind.

##### Our MVCs are not features, should make a more narrow definition

We're working with product marketing on making it easier to provide context.
In addition, our new vision pages should go a long into doing this.

##### We take on too much breadth, risk competitors being better at our core

Jason: This seems to be mostly answerable using the "We should build more depth" answers above.

##### We should spend more time on onboarding / training

Agreed. We're just starting a Growth team that will look at ways we can
do this most effectively.

##### Teach new features to support

Jason: We also have a responsibility to teach our users, which we do through the release post primarily I think. I bet that support is reading these - if they are finding it lacking, then our users probably are too, and we could work together to ensure both support and our customers (at least who follow the release posts/index.html.md) are both properly up to speed.

##### We should not add anything to Core/Starter

Our biggest competitor should be ourselves. If we fail to improve Core or Starter, customers are more likely to pay for a competitor than chose GitLab. The community is a valuable asset to the company and an exclusive focus on Premium and Ultimate will alienate them.

##### Our security features are not worthy to replace BlackDuck, Veracode, etc. We should add more reports and information to be able to replace them

Fabio: considering that we entered this area in late 2018, we are quickly ramping up and we constantly iterate every release to improve our security features. The fact we are already compared to market leaders is a good indicator we are going in the right direction!

Product survey Q&A.md
Displaying Product survey Q&A.md.