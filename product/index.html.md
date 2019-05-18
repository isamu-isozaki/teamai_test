---
layout: markdown_page
title: Product
---

The document below talks about _how_ we do product at GitLab, not about _what_.
For the _what_, see [Product Direction](/direction/).

## Where to reach product managers
{:.no_toc}

- [**Public Issue Tracker (for GitLab CE)**](https://gitlab.com/gitlab-org/gitlab-ce/issues); please use confidential issues for topics that should only be visible to team members at GitLab.
- [**Chat channel**](https://gitlab.slack.com/archives/product); please use the `#product` chat channel for questions that don't seem appropriate for the issue tracker.

## On this page
{:.no_toc}

- TOC
{:toc}

## Other pages related to Product
{:.no_toc}

* [Product Categories](/handbook/product/categories/)
* [Release posts](/handbook/marketing/blog/release-posts/)
* [Making Gifs](/handbook/product/making-gifs/)
* [Data analysis](/handbook/product/data-analysis/)
* [Technical Writing](/handbook/product/technical-writing/)
* [Markdown Guide](/handbook/product/technical-writing/markdown-guide/)
* [Demo](/handbook/marketing/product-marketing/demo/)

## Who to talk to for what

### Who

Please see the [Product Categories](/handbook/product/categories/) to know which product manager handles which category.

### How

If you have any product-related questions, comments, input, or otherwise, the
product manager is the primary person you should talk to, _if creating an issue
does not suffice_. Otherwise, [read this section on how to create an
issue](/handbook/product/#how-to-submit-a-new-issue).

This includes, but is not limited to, features, bugs, and other changes that need
to be prioritized, changed, discussed, or need more attention.

Product managers will reach out to stakeholders when making or communicating any
decision. The pressure of balancing priorities while ensuring we build excellent
software is on the product managers and they need all the input they can get to
achieve this.

Paid features fall under their respective PMs, not under one PM in particular.
For instance, Service Desk falls under Victor, because it's part of our Issues.

See our [product categories](/handbook/product/categories/) for how to map our product to product managers.

### Technical Writing

The Technical Writing team is responsible for:

* [docs.gitlab.com](https://gitlab.com/gitlab-com/gitlab-docs)
* CE docs
* EE docs
* Written technical tutorials which are in CE or EE docs
  (video tutorials will come later).

We are there to assist developers in their documentation writing process by
providing copy editing and reviewing services and are not responsible for
writing the first draft of documentation for new or updated features.

We maintain and improve the overall health of documentation
by creating topic index pages, improving organization, creating tutorials, etc.

We manage our documentation tasks for CE and EE on the following issues boards
which track labels beginning with `docs-`:

* [CE Documentation Issue Board](https://gitlab.com/gitlab-org/gitlab-ce/boards/106589)
* [EE Documentation Issue Board](https://gitlab.com/gitlab-org/gitlab-ee/boards/266349)

### Planning horizon

1. [Mission](/strategy/#mission): generation
1. [Strategy](/strategy/#sequence-): lustrum
1. [Vision](/direction/product-vision/): year
1. [Milestones](/direction/#future-releases): quarter (we have issues assigned to specific release milestone for a rolling 3 months)
1. [Release](https://gitlab.com/gitlab-org/release-tools/blob/master/templates/monthly.md.erb): month (we try to not change the release that is started)

Inspired by:

- First part of [Dear PMs, It's Time to Rethink Agile at Enterprise Startups](http://firstround.com/review/dear-pms-its-time-to-rethink-agile-at-enterprise-startups/)
- [The Nearsighted Roadmap](https://medium.com/@jobv/the-nearsighted-roadmap-57fa57b5906a)

## How to work as/with product

At GitLab, the PMs lead their specialization. That is, the Platform PM decides
what the platform team works on, for which release, and makes sure
this furthers our goals. This includes bugs, features, and architectural changes.

The PM can't be expected to parse every single bug or issue that comes by, so
they have to rely heavily on the input of the various stakeholders. To be
able to achieve this, both the PM and the stakeholders have to actively work
together. It's a two-way street.

In general terms, if you require something to happen with the product or if you
need engineering staff for a particular change, you approach a PM.
Preferably through creating an issue (the GitLab way), and mentioning them there.

In the same vein, PMs are required to ask for feedback from the stakeholder of
particular changes. If a change will affect GitLab.com and its maintenance, a
PM should proactively reach out to infrastructure engineers to help with the
scope, design, and decisions regarding this change.

It is then up to the PM to weigh all these inputs and decide on a
[prioritization](#prioritization). It is to be expected that they are the best equipped to make this
prioritization, while also keeping in mind all goals of GitLab.

### Examples: A customer has a feature request

If you hear a feature request from a customer, you should follow the normal
procedure: create an issue and label it correctly. Let's say the customer
requests an enhancement to Issues. You know by reading above that you'll have to
label this with `Discussion` and you can mention or reach out to Victor to
expedite this if warranted.

A salesperson for an organization asking for a paid-tier feature request shall
work with the product manager to arrange conversations to further explore the
feature request and desired outcome. The process will be:

* Sales schedules 1 hour zoom meeting with product manager, customer and themselves. Call recorded if customer gives permission.
* Product Manager prepares any additional questions they would like answered, beyond what is below.
  * What version of GitLab are you currently using? CE / Starter / Premium?
  * How are you currently doing source code management? GitLab merge requests or another tool? How about CI/CD?
  * How are you currently doing issue management? How are you using HP ALM? Agile/Kanban? What do your sprint/iterations look like? 1 week? 1 month? 2 months?
  * What is the integration like between issue management and source code management?
  * How do teams manage multiple repos? Does a team typically work on one repo at a time? Or do they work on multiple repos at the same time?
* Sales sends questions to customer prior to meeting.
* Meeting is created in Salesforce.com
* Sales creates a Google document for notes from call with customer.  Google Doc shared with product manager and sales manager
* Sales and product manager schedule 15 minute pre-meeting to share what we know about the customer thus far, so as to not waste time asking questions we already know the answer to. Notes from this pre-meeting are added to the Google document.
* Sales adds a link to the Google document under the account object as a note.

### Example: Many support requests come in about a bug with CI

Same as before, make sure an issue is made and make your case with Mark that
this is becoming a problem and needs to be fixed. Mark will make sure that this
is fixed or resolved in some other way.

### Example: I think creating new files is slow

Everything in GitLab should be fast and creating files falls under the
repository, so you create an issue and make James aware of it by mentioning it.

James in turn will investigate whether this is a general problem or one specific
to GitLab.com, in collaboration with infrastructure and others and schedule any
necessary changes for an upcoming release.

## How to share feedback

Whenever you're sharing feedback on an issue (e.g. "Customer X wants this"), whether from a customer or directly from you,
please make sure to do the following:

- Link to the source if possible
- Provide context: if a customer wants this feature, include _why_ they are interested in this. If you don't know,
make sure to ask or bring the relevant PM in contact with the customer
- Include any further useful context (e.g. what kind of software is this customer building, or how big are they)
- Be as specific as possible

If a customer expresses interest by simply mentioning an issue number or e.g. "an integration with X",
that is not sufficient information. Make sure to ask them:

- why do you want this?
- what parts of this issue / integration are important to you and why?
- have you tried workarounds?
- how important is this to you?

The product manager is responsible for figuring all of this out, but being one step ahead of them
will speed things up.

## Product Process

Introducing changes requires a number of steps, with some overlap, that should be
completed in order:

### Prioritization: Ahead of kickoff

1. Proper discovery has been done and requirements for the change are defined
2. Engineering has been involved in the discovery process (FE, BE, UX, as needed)
3. Technical architecture has been drafted and is agreed upon
4. Scoping and splitting up into actionable issues has happened

#### Ambitious Planning

Here at GitLab, we are an [ambitious](#be-ambitious) company and this means we
aim for big things with every release. The reality of taking chances and
planning aspirationally means that we won't always be able to deliver everything
that we wanted to try in every release, and similar to our [OKRs](/handbook/ceo/#three-levels-of-performance),
we believe this is a good thing. We don't want to shy away from challenging
ourselves and always want to keep a sense of urgency, and aiming for more helps
us do that. Also see [the importance of velocity](/handbook/engineering/#the-importance-of-velocity)

### Kickoff meeting

#### Preparation

1. Relevant issues are added to the [Kickoff doc](https://docs.google.com/document/d/1ElPkZ90A8ey_iOkTvUs_ByMlwKK6NAB2VOK5835wYK0/edit?usp=sharing)
   1. Product managers should add any issue that is marked ~direction and ~Deliverable for the upcoming milestone (no ~Stretch issues)
   1. Issues should report the tier they will be included in
2. Issue descriptions are updated to include an introduction to the underlying
   problem, use cases, and a complete proposal. It should be easy to
   understand the problem from reading the issue title and description without
   digging through comments.

#### Meeting

1. We start the meeting by reminding anyone who may be watching the video/stream about how we [plan ambitiously](#ambitious-planning).
2. Introduce the issues of your product category by explaining the problem and proposal of listed items.
3. Share your screen to guide through the individual issues. If there is a UX design or mockup available, show it.

### Execution

1. Design
1. Backend development
1. Frontend development
1. QA and feature assurance
1. Deploy

### QA RCs on staging and elsewhere

After the feature freeze, it's expected of each product manager to test their own features and perform quality assurance
to the best of their ability and follow up where necessary.

Product managers can use the staging environment once the release managers have deployed a release candidate to staging.
Release managers should post in the #product channel in Slack that a new release candidate is available. Product managers
can also use other environments as needed, such as GitLab provisioned on Kubernetes with GKE.

## Communication

- [**Public Issue Tracker (for GitLab Community Edition)**](https://gitlab.com/gitlab-org/gitlab-ce/issues)
and [**for GitLab Enterprise Edition**](https://gitlab.com/gitlab-org/gitlab-ee/issues) - please use
confidential issues for topics that should only be visible to team members at GitLab.
- [**Chat channel**](https://gitlab.slack.com/archives/product) - please use the
`#product` chat channels for questions that don't seem appropriate for the
issue tracker or more generic chat channels.

## Goals of Product

Everyone at GitLab is involved with the product. It's the reason why we are
working together.

With every release of GitLab, we want to achieve each of the following goals.

1. Improve GitLab's existing tools.
1. Achieve [our vision](/direction/#vision) of a complete toolset.
1. Make our product more interesting for our customers through Products and
EE exclusive features.

## Scope of responsibilities

The product team is responsible for iteration on most of GitLab's products and
projects:

- GitLab CE and EE
- GitLab.com
- about.gitlab.com
- customers.gitlab.com
- version.gitlab.com
- license.gitlab.com

This includes the entire stack and all its facets. The product team needs to
weigh and prioritize not only bugs, features, regressions, performance, but also
architectural changes and other changes required for ensuring GitLab's excellence.

## Product at GitLab

GitLab is designed and developed in a unique way.

The direction for the GitLab product is spelled out on the
[Direction page](/direction). This document provides lessons and heuristics on
how to design changes and new features. Our iterative process is demonstrated in
a [blog post](/2017/01/04/behind-the-scenes-how-we-built-review-apps/).

Much of our product philosophies are inspired by the [Ruby on Rails doctrine](http://rubyonrails.org/doctrine/) of ['Rails is omakase'](http://david.heinemeierhansson.com/2012/rails-is-omakase.html). I highly suggest reading these.

### TL;DR

1. [Minimally Viable Change](#the-minimally-viable-change): Work in iterations
by implementing only the minimally viable change.
1. [Convention over Configuration](#convention-over-configuration): Avoid
configuration and make it work out of the box.
1. [Be Ambitious](#be-ambitious): do things no one else is doing.
1. [Do not mess with Flow](#simplicity): _frictionless_ from planning to monitoring. Avoid adding clicks.
1. [Embrace the single application](#single-application): unlock the unique
benefits of a single application in early iterations.

### Product Principles

#### The Minimally Viable Change

Reduce every change proposal to its absolutely minimally viable form.
This allows us to ship almost anything within a single release,
get immediate feedback and avoid deep investments in ideas that might
not work. Other advantages:

- This helps avoid the sunk-cost fallacy in situations where we might
decide to drop a change, as we almost never spend more than a few weeks working
on something.
- It prevents over-engineering.
- It forces everyone involved to look for the simplest solution to a problem,
which is often the best solution.
- It forces working towards an 80/20 solution; while competing products might cater
to the last 20% of the market, a minimally viable solution is _good enough_ for 80%.
- A bigger change is harder to review.
- A bigger change is harder to roll back.
- The bigger the change, the larger the risk of a conflict with someone else's contribution
- The bigger the change, the longer it takes before everyone can benefit from the change.
- Further changes or enhancements to the change are driven by feedback from
actual users. This is a much more informative mechanism than the intuition
of a product person (though note that this doesn't mean we should just build
whatever feedback tells us).

The minimally viable change [should not be a broken feature](http://blog.crisp.se/2016/01/25/henrikkniberg/making-sense-of-mvp).

![mvc.png](/handbook/product/mvc.png)

Virtually every new feature must be maintained forever (the standard for sunsetting a
feature is very high). Creating a new feature means that GitLab has to continually manage the technical
costs of maintenance of that feature. Making small changes with quick feedback loops reduces the risk
of introducing a new feature where the value doesn't justify the long-term costs.

A new feature also adds a tax on the user experience due to additional complexity in the product.
Make sure that the benefits gained by users from the new feature more than cover the tax incurred,
accounting for how frequently the new feature is used by users. In particular, the new feature
should satisfy this inequality:

`(benefits * frequency) / (tax * (1-frequency)) > 1`

Despite its minimal form, the change
* always requires documentation
* has to have its usage tracked from day 1 if the feature has a meaningful impact.

[![xkcd.com](https://imgs.xkcd.com/comics/optimization.png)](https://xkcd.com/1691/)

#### Convention over Configuration

Prefer choices that are well thought out and based on current best practices.
Avoid unnecessary configuration. Avoid configuration to support fragile workflows.

For example, when considering whether to add a checkbox or two radio boxes, think
carefully about what users really want. Most of the time, you'll find you really only need
one solution, so remove the other option. When two possible choices really are
necessary, the best or most common one should be the default, and the other one
should be available. If the non-default choices are significantly less common,
then consider taking them out of the main workflow for making decisions, by
putting them behind an Advanced configuration tab, for example.

Every configuration option in GitLab multiplies its complexity, which means
the application is harder to use, harder to develop, and
less friendly to users.

Requests for configuration can be a proxy for trying to support a fragile
workflow. Rather than enabling bad habits and incurring product debt, effort
should be spent helping customers adopt best practices.

Making features configurable is _easy_ and _lazy_.
It's a natural reaction to propose a big change to be configurable,
as you worry it'll negatively affect certain users. However,
by making a feature configurable, you've now created two problems.

[![xkcd.com](https://imgs.xkcd.com/comics/standards.png)](https://xkcd.com/927/)

Work on solutions that work for everyone, and that replace all
previous solutions.

Sometimes configuration is inevitable or preferable. GitLab should
work perfectly right out of the box for most users. Your configuration
must not make that experience worse and should always _get out of the
way of the user_.

##### Encouraging behavior

Convention also implies that we're encouraging our customers to do things
in a certain way. A very concrete example of this is the ability to disable
pipelines. We believe that our integrated solution will give a superior user
experience and we're motivated to encourage this behavior. For this reason, adding a
configuration to allow disabling this permanently (be that in a template or
instance-wide), is something that should be avoided.

Encourage favorable behaviors by limiting configuration.

##### Default to ON

In addition to encouraging behavior by limiting the ability to toggle features,
new features, when introduced, should default to turning things ON (if they are
configurable at all).

##### Deciding on configurations

Avoiding configurations is not always possible. When we have no choice,
the secondary priority is to configure something in the GitLab
interface. A configuration should only appear in a file (`gitlab.rb` or
`gitlab.yml`) as a last resort.

##### Configuration in file

There are two major configuration files available in GitLab. Adding configurations
to either should be avoided as much as possible.

- [`gitlab.yml`](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/config/gitlab.yml.example)
is the configuration file used by the Rails application. This is where the domain is configured. Other configurations should be moved to the UI as much as possible and no new configurations should be added here.
- [`gitlab.rb`](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/files/gitlab-config-template/gitlab.rb.template)
is the configuration file for Omnibus-GitLab. It acts not only as
an abstraction of the configuration of `gitlab.yml` for GitLab-Rails, but also
as the source for _all configurations_ for services included and managed within
the Omnibus-GitLab. Newly introduced services probably need to be configured
here.

When you have to add a new configuration, make sure that the features and
services are on by default.
Only add a configuration line to either of these configuration files if the
feature or service cannot be fully disabled from the admin UI.

[Convention over configuration is also listed in the CONTRIBUTING file in GitLab's repositories.](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#contribution-acceptance-criteria)

#### Be Ambitious

Many crazy, over-ambitious ideas sound like they are impossible just
because no one else is doing them.

Since we have amazing engineers and a culture of shipping minimally
viable changes, we are able to do a lot more 'impossible' things than others.

That's why we're shipping merge conflict resolution, why we shipped built-in CI
before anyone else, why we built a better static pages solution, and why
we're able to compete.

[![xkcd.com](https://imgs.xkcd.com/comics/squirrel_plan.png)](https://xkcd.com/1503/)

#### Simplicity

Doing something simple in GitLab should BE simple and require no
human cpu-cycles to do so. Things that are simple now should still
be simple two years from now, ten years from now, and onwards.

This sounds obvious, but messing with flow is easily done. In most
cases, flow is disrupted by adding another action, or another click.

For instance: You want users to be made aware of the rules of a project.
Your proposal is a little popup that shows the rules before they create an
issue. This means that every time that someone creates an issue they need
to click once before resuming their normal action. This is unacceptable.
A better solution is to add a link to the issue that points the user to this.

[![xkcd.com](https://imgs.xkcd.com/comics/app.png)](https://xkcd.com/1174/)

It's very hard to maintain flow with a lot of configurations and options.
In cases where you want to enforce a certain behaviour, the most obvious step
may be to add another step or action. This can be avoided by making the action
work in parallel (like a link in the issue), encouraging rather than enforcing
certain behaviours.

Also, we don't want users to be able to construct workflows that break GitLab or
make it work in unpredictable ways.

#### Discoverability Without Being Annoying

Feature discoverability is important for allowing new and existing users to access
old and new features, thereby increasing the value for them. It also allows GitLab
to get as much feedback as possible, as fast as possible, in order to quickly
iterate.

However, UI that purports to increase discoverability, but that is not carefully
designed and implemented, may actually _harm_ the overall experience by constantly shoving
unwanted images and text in the face of the user. The end result is that the user
loses trust in GitLab, and they no longer take the time to carefully parse text and
other UI elements in the future. Even worse, they might leave GitLab because of this
degraded experience. The following are a few illustrative examples and best practices.

##### Empty states

- Empty states are the simplest paradigm for feature discoverability. They should always be considered.
- Typically, any empty list view should be replaced with an empty state design, similar to below.
- Empty state designs should provide an immediate call to action, thus improving discoverability.
- Once the UI area is no longer "empty", that design is no longer present and there is no harm to the user experience at all.

![pipelines_empty_state.png](/handbook/product/pipelines_empty_state.png)

##### Banners

- Banners draw attention to the user by introducing a feature to them in a nearby context.
- Benefits
  - Attractive graphics to draw attention.
  - Brief explanatory text.
  - A call to action for the user to start using the feature.
- Downsides
  - They invade the user's current flow and intended actions.
  - They are visually disruptive.
- To offset the downsides
  - There should only be one banner on the page at a time.
  - They should carry minimal information and not overwhelm the page.

Think of this: Your co-worker is hard at work in front of their computer, and you
suddenly tap their shoulder or yell at them to tell them about some new cool widget.
You better have a good reason for that: that widget better be awesome.

- Banners need to be dismissible permanently so that a user _never_ sees it again,
_ever_, after they have dismissed it.
- We have only one chance to introduce a feature to a user with a banner.
- Once they have chosen to dismiss it, it should never appear again because we do
not want to betray their trust when they click dismiss.
- Trust is incrementally earned with delightful experiences. If a banner
re-appears after dismissal, trust is destroyed.

Back to the analogy: Your co-worker said they don't care about that new cool widget. Never,
ever, _ever_, bring it up again. They told you they don't care, and you need to respect
that.

- Banner dismissal must be associated with the user in the system database, and
it must persist, even across version upgrades.
- If a user accesses GitLab with different clients, the dismissal state must be
consistent and the user has zero chance of seeing that banner again.
- A corollary is that banners should only be shown when a user is logged in.

![pipelines_empty_state.png](/handbook/product/banner_customize_experience.png)

##### Navigation

Leveraging navigation is an effective design paradigm to introduce a user to a new
feature or area of GitLab.

- See example design below: There is a subtle pulsating blue dot to draw a user's attention.
- This plants a seed in the user's mind that they can go and investigate that feature at a later time.
- If at the current moment they don't want to be disturbed, they can just ignore it because it is only
a slight visual disturbance (as compared to a banner which takes up more screen real estate).

- The pulsating blue dot UI element should be dismissible, with the same dismissibility
requirements as banners, for the same trust reasons discussed above.
- If dismissed once, it stays dismissed forever, for that user, across all clients that the user can
access GitLab with.

- In the same way that a page should not have more than one banner, the navigation should
_not_ have more than one call to action (the blue dot in this case).
- We do not want to overload the user with too much noise.

Back to the analogy. We're not going to bother our co-worker with 5 different cool new widgets at the same time.

- GitLab should only ever show at most one blue dot. This should be implemented by
GitLab having a prioritized list of blue dots stored in the backend.
- It should show the highest priority blue dot that has not already been dismissed.

![tooltip_boards.png](/handbook/product/tooltip_boards.png)

#### Single application

GitLab is a single application, rather than a set of loosely connected
components. This is a big advantage, [read why here](/handbook/product/single-application).

Consider opportunities to take advantage of this unique attribute in early
iterations. Integrating features with different parts of the application can
increase the adoption of early iterations. Other advantages:

- A minimal viable feature that is well integrated can be more useful than a
sophisticated feature that is not integrated.

Although not every feature needs to be integrated with other parts of the
application, you should consider if there are unique or powerful benefits for
integrating the feature more deeply in the second or third iteration.

#### Flow One

Shipping only MVCs can result in a large set of loosely connected pieces that
don't necessarily combine into a single, great user experience.

An obvious solution to this would be to plan out the future in detail,
creating a long-term roadmap. However, this is unwanted as it can restrict
your flexibility and ability to respond to changing needs or feedback.

Flow One offers an alternative. You draw out a workflow consisting of
MVCs (that can be shipped individually). The workflow should only cover a
specific, narrow use-case, and nothing more.

This means you:

- avoid creating an inflexible, long-term plan
- can more easily construct a full feature/ capability, which is more easily marketed
- can provide context to each individual change ("we need this as part of X")
- can continue to ship MVCs
- work concurrently on several items, non of which are blocking

Flow One should cover the first iteration of a particular workflow.
After this, individual MVCs can be introduced to expand the use-cases
or loosen the assumptions (e.g. from a feature that can only be used
if you're using feature branches, to one that works for other git strategies).

### Breadth over depth

See our thoughts on breadth over depth [on our strategy page](/strategy/#breadth-over-depth).

### Prioritization

As this document and the [direction page](/direction) shows,
there are a million things we want to do.
So, how do we prioritize them and schedule things properly?
Roughly speaking, we balance the following priorities:

1. Security fixes and data-loss prevention
1. Regression fixes (things that worked before including major performance regressions)
1. New features, technical debt, community contributions, and all other improvements

Issues like security come in [different severity levels](https://about.gitlab.com/handbook/engineering/security/#labels-and-confidentiality).
Lower severity means a lower priority, at ~S4/~P4 their priority is no different then other feature proposal.

Any new feature will have to meet the following requirements:

1. It is [technically viable](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#contribution-acceptance-criteria)
1. The technical complexity is acceptable. We want to preserve our ability to make
changes quickly in the future so we try to avoid complex code, complex data structures, and optional settings.
1. It is orthogonal to other features (prevents overlap with current and future features).
1. The requirements are clear.
1. It can be achieved within the scheduled milestone. Larger issues should be
split up, so that individual steps can be achieved within a single milestone.

New features are prioritized based on several factors:

- Is it a top project from the [OKRs](/okrs/)?
- Does it bring our [vision](/direction/#vision) closer to reality?
- Does it help make our community safer though [moderation tools](https://gitlab.com/gitlab-org/gitlab-ce/issues/19313)?
- Is this something requested by many of our customers?
- Does it help generate revenue for us through our [paid tiers](/handbook/product/#paid-tiers)? (i.e what is the impact on IACV?)
- Is it something we need ourselves?
- Has it been much requested on the issue tracker?
- Does it benefit a large portion of our users?

Every release of GitLab has to be better than the last. This means that
bugs, regressions, security issues, and necessary performance and architecture changes always take up
whatever capacity they require to ensure GitLab remains stable, secure and fast.

We hope to realize our [vision](/direction/#vision),
while making sure we're building things that our customers want. In practice this means
that we aim to ship features that align with our vision,
but also solve problems our customers have. These features bring the product forward,
and build value for the largest group of people possible. For example, issue relationships is a highly
requested feature that also fits neatly within our vision. Everyone will benefit from this.

In practice, it is not possible to always ship things that only fall within our vision.
Other changes are prioritized and scheduled based on demand. An example would be a specific
form of authentication that is only used in particular organizations. This is not a big
win to all our customers, but if it's not too much work, it can be a very big win to a subset of
customers. Demand can also come internally, such as things that'll help GitLab achieve goals
within a team or specifically drive business goals such as specific EE features.

We take all priorities in account when planning and scheduling larger initiatives across the
teams (such as: "we're integrating CI, so everyone has to contribute to this in some way").
Still, most changes are scheduled at a team-level, like: "make issues faster", or
"add a new way to schedule pipelines".

#### Example

To make it clear with an example, the CI/CD team might ask:

* What else is needed for the idea-to-production vision? Are there other APIs needed
for ChatOps integration? Can we trigger manual actions via API? (e.g. [Environment-specific variables](https://gitlab.com/gitlab-org/gitlab-ce/issues/20367),
and [show deployment activity](https://gitlab.com/gitlab-org/gitlab-ce/issues/19992))
* What moves us towards automatic deploys of `gitlab-ce`?
* What moves the [CI/CD vision](/direction#ci--cd) forward?
* Can we polish the existing feature set? (e.g. [#21126](https://gitlab.com/gitlab-org/gitlab-ce/issues/21126), [#18178](https://gitlab.com/gitlab-org/gitlab-ce/issues/18178), [Show builds in context of pipeline](https://gitlab.com/gitlab-org/gitlab-ce/issues/20863), [#5983](https://gitlab.com/gitlab-org/gitlab-ce/issues/5983), [#3976](https://gitlab.com/gitlab-org/gitlab-ce/issues/3976))
* Can we speed up CI/CD pipelines? (e.g. sticky runners, [automatic parallelization](https://gitlab.com/gitlab-org/gitlab-ce/issues/21480))
* What can we do to make customers happy? ([list](https://gitlab.com/gitlab-org/gitlab-ce/issues?scope=all&state=opened&utf8=✓&label_name%5B%5D=CI&label_name%5B%5D=customer))
* What can we do to ship EE features for CI? (e.g. [gitlab-ee#933](https://gitlab.com/gitlab-org/gitlab-ee/issues/933))

#### Milestones

We schedule an issue by assigning it a milestone; for more on this see
[Planning a Future Release](#planning-future-release).

### Naming features

Naming new features or renaming existing features is notoriously hard and sensitive to many opinions.

#### Factors in picking a name

- It should clearly express what the feature is, in order to avoid the [AWS naming situation](https://www.expeditedssl.com/aws-in-plain-english).
- It should follow [usability heuristics](http://www.designprinciplesftw.com/collections/10-usability-heuristics-for-user-interface-design) when in doubt.
- It should be common in the industry.
- It should not overlap with any other existing concepts in GitLab.
- It should have as few words as possible (so people won't use a shortened name).
- If you remove words from the name, it is still unique (helps to give it as few words as possible).

#### Process

- It's highly recommended to start discussing this as early as possible.
- Seek a broad range of opinions and consider the arguments carefully.
- The PM responsible for the area involved should make the final decision and not delay the naming.
- Naming should definitely not be a blocker for a feature being released.
- Reaching consensus is not the goal and not a requirement for establishing a name.

#### Renaming

The bar for renaming existing features is extremely high, especially for long-time features with a lot of usage.
Some valid but not exclusive reasons are:

- New branding opportunities
- Reducing confusion as we introduce new adjacent features
- Reducing confusion as we re-factor existing features

### No enforced workflows

Enforced workflows should be avoided in GitLab. For example, there are three issue
states (`Open`, `In Progress` (as of 10.2), and `Closed`), and any issue should be
allowed to transition from one state to any other state
without workflow restrictions. (Roles and permissions is a separate concern.)

- Enforced workflows restrict GitLab to a smaller number of use cases, thus reducing the value of GitLab.
- Enforced workflows require overhead to maintain in the product. Each new feature
must account for any existing enforced workflows.
- We should trust our users to use GitLab responsibly, giving them freedom, instead
of imposing enforced workflows that we think made sense at the time of design and implementation.

[A comment on Hacker News](https://news.ycombinator.com/item?id=16056678) perfectly details what can go wrong when enforcing workflows:

"The down side for the true end-users, those who actually use the software day-to-day,
is that most business processes are awful. If your experience is the hellish existence
that I see strolled about on threads where JIRA comes up ...:

1. Your admin(s) set it up once and hasn't bothered to iterate on those workflows.
1. The business mapped their autonomy stripping processes onto JIRA intentionally.
I'd guess that most of your work experience is similar. Process stifled nonsense."

But that comment also specifies the advantage:

  "JIRA's most powerful feature is that it affords for mapping businesses processes onto software.
  This is incredibly compelling to enterprise customers. Software that enforces workflows, procedures
  and requirements can be an incredible lever and JIRA's price point makes build vs buy decisions an absolute no-brainer."

We should ensure that GitLab makes it easy to help with enterprise workflows:

- When starting a branch with an issue (number) we link it to the branch.
- When merging an MR you automatically close the issue(s) it fixes.
- In GitLab CI you can define your deployment stage progression (staging, pre-production, production) including manual approval.
- We run quality and security tools automatically and provide dashboards to check status instead of making it a step in the process.
- We limit the impact of mistakes with incremental rollout and automatic rollback.

### Performance

Fast applications are better applications. Everything from the core user experience,
to building integrations and using the API is better if every query is quick, and
every page loads fast. When you're building new features, performance has to be top of mind.

We must strive to make every single page fast. That means it's not acceptable for new
pages to add to performance debt. When they ship, they should be fast.

You must account for all cases, from someone with a single object, to thousands of objects.

Read the handbook page relating to [performance of GitLab.com](/handbook/engineering/performance), and note the Speed Index target shown there
(read it thoroughly if you need a detailed overview of performance). Then:

- Make sure that new pages and interactions meet the Speed Index target.
- Existing pages should never be significantly slowed down by the introduction of new features
or changes.
- Pages that load very slowly (even if only under certain conditions) should be sped up by
prioritizing work on their performance, or changes that would lead to improved page load speeds
(such as pagination, showing less data, etc).
- Any page that takes more than 4 seconds to load (speed index) should be considered too slow.
- Use the [availability & performance priority labels](/handbook/engineering/performance/#performance-labels)
to communicate and prioritize issues relating to performance.

Of course, you must prioritize improvements according to their impact (per the [availability & performance priority labels](/handbook/engineering/performance/#performance-labels)).
Pages that are visited often should be prioritized over pages that rarely have any visitors.
However, if page load time approaches 4 seconds or more, they are considered no longer
usable and should be fixed at the earliest opportunity.

### Alpha, Beta, GA

Occasionally we need to test large, complex features before we are confident
that we'll be able to scale, support and maintain them as they are.
In this case we have the option to release them as Alpha or Beta versions.

In general, we should avoid releasing Alpha or Beta versions of features.
A minimally viable change should be _viable_ and therefore should not need a
pre-release. That said, if there is a situation where we have no valid alternative,
the definitions of each stage is below.

It's never acceptable to make changes that risk any damage to existing production
data accessed by our users.

#### Alpha

- not ready for production use
- unstable and can cause performance and stability issues
- the configuration and dependencies are likely to change
- features and functions may be removed
- data loss can occur (be that through bugs or updates)

#### Closed Beta

Similar to Beta, but only available to selected users.

- not ready for production use
- unstable and can cause performance and stability issues
- configuration and dependencies unlikely to change
- features and functions unlikely to change
- data loss less likely

#### Beta

- not ready for production use
- unstable and can cause performance and stability issues
- configuration and dependencies unlikely to change
- features and functions unlikely to change
- data loss not likely

#### Generally Available (GA)

Passed the [Production Readiness Review](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md) for GitLab.com, which means that it is:

- ready for production use at any scale
- fully documented and supported

### Discouraging, deprecating and removing features

Deprecating features (changes) follows a particular pattern.
Use the language `Discouraged (maintained)`, `Deprecated (not maintained)` or `Removed` to
specify the state of a feature that is going to be or is removed.

Features that are discouraged, deprecated or removed should be:

1. Labelled accordingly in the documentation
1. Labelled accordingly in the application

Features that are Deprecated or Removed should be removed from marketing pages.

#### Discouraged (maintained)

- planned to be removed at some point in the future, but will be deprecated publicly ahead of time
- maintained: bugs and regressions are still fixed
- still available with new installations, but documentation mentions
that use is discouraged (with alternatives if relevant)

#### Deprecated (no longer maintained)

- may be removed at any point in the future
- no longer maintained: bugs and regressions are no longer fixed
- still available with new installations, but documentation mentions
deprecated state

#### Removed

- no longer available in the latest version of the product

### No artificial limits in Core

Per [GitLab Stewardship](/stewardship/#promises), we will not introduce _artificial_ limits in Core. Artificial means
arbitrarily setting a small number (such as: 1) as a limit on a given GitLab object category,
that would incur _no additional_ effort or cost had we chosen a larger number. The additional
effort includes product, design, and engineering effort to create the feature in the first place,
and to maintain it over time.

For example, GitLab Core has the [issue board feature](https://docs.gitlab.com/ee/user/project/issue_board.html) in every project.
In GitLab EE, each project supports [multiple boards](https://docs.gitlab.com/ee/user/project/issue_board.html#multiple-issue-boards).
This _does not_ mean that Core has an artificial limit of one board per project, because there is additional effort
to manage multiple boards such as supporting the navigation interface, and all the associated engineering work.

### Data-driven work

Using data to learn from our users is important. Our users are spread across GitLab.com
and self-managed instances, so we have to focus our efforts on learning and
providing benefit to both when we decide to collect more data, or build and use
additional analytics tools. If we do this, we can help make the rest of the
company successful as well. This means that we should:

- Build and use tools that work for both GitLab.com and self-managed.
- Start from a question, and build / collect what we need to answer that question. This avoids wasting time with data we don’t need.
- Use and improve existing tools we have inside of GitLab before leaning towards off-the-shelf products.
- Our customers, sales team and customer success teams all benefit greatly from similar insights into their usage as the product team does. Make things that help all of these people.

### Working with (customer) feature proposals

When someone requests a particular feature, it is the duty of the PM to investigate
and understand the need for this change. This means you focus on what is the problem
that the proposed solution tries to solve. Doing this often allows you to find that:

1. An existing solution already exists within GitLab
1. Or: a better or more elegant solution exists

Do not take a feature request and just implement it.
It is your job to find the underlying use case and address that in an elegant way that is orthogonal to existing functionality.

This prevents us from building an overly complex application.

Take this into consideration even when getting feedback or requests from colleagues.
As a PM you are ultimately responsible for the quality of the solutions you ship,
make sure they're the (first iteration of the) best possible solution.

### Security Paradigm

Security is now part of [SDLC](https://en.wikipedia.org/wiki/Software_development_process).

You can read more about our approach in the [Secure Vision](/direction/secure/) page.

If you are interested in advanced technical details, you can find more in the
[Secure Team engineering](https://about.gitlab.com/handbook/engineering/ops-backend/secure/) page.

### Statistics and performance data

Traditionally, applications only reveal valuable information about usage and
performance to administrators. However, most GitLab instances only have a handful of
admins and they might not sign in very often. This means interesting data is rarely
seen, even though it can help to motivate teams to learn from other teams,
identify issues or simply make people in the organisation aware of adoption.

To this end, performance data and usage statistics should be available to all users
by default. It's equally important that this can be optionally restricted to admins-only,
as laws in some countries require this, such as Germany.

Not all instance-data is available to all users in GitLab yet.
[This issue](https://gitlab.com/gitlab-org/gitlab-ce/issues/41416) and the epic above should solve this.

## How to work as a PM

If you follow the guidelines above, you won't be writing long, detailed
specs for a part of the product for next year. So how should you be
spending your time?

Invest the majority of your time (say 70%) in deeply understanding the problem.
Then spend 10% of your time writing the spec _for the first iteration only_ and
handling comments, and use the remaining 20% to work on promoting it.

A problem you understand well should always have a (seemingly) simple or obvious
solution. Reduce it to its simplest form (see above) and only ship that.

Once you've shipped your solution, both you and the community will
have a much better idea of what can be improved and what should be prioritized
for future iterations.

As a PM, you're the person that has to kick-off new initiatives. You're not
responsible for shipping something on time, but you _are_ responsible for taking
action and setting the direction. Be active everywhere, over-communicate, and
sell the things you think are important to the rest of the team and community.

As a PM, you need to set the bar for engineering. That is, to push engineering and
the rest of the company. You almost want engineering to complain about the pace
that product is setting. Our default instinct will be to slow down, but we can't
give in to that.

As a PM you don't own the product; ask other people for feedback and give
team members and the community the space to suggest and create things without your
direct intervention. It's your job to make sure things are decided and
planned, not come up with every idea or change.

### Planning and roadmaps

As a PM, you must plan for the near term (more detailed) as well as for the
long term (more broad). This will enable you to efficiently communicate both
internally and externally how the team is planning to deliver on the [product vision](https://about.gitlab.com/direction/product-vision/).

#### Near-term

In order to plan effectively around releases, as a PM you should have a detailed
3-month roadmap at all times. The issues contained in this near-term roadmap
are the ones you should be spending the most energy on (fleshing them out,
adding detail, discussing, etc). These issues will go through a refinement period where
Product, Engineering, UX and other parties will discuss the proposal until a
proper MVC proposal is reached (see [Contents of an MVP](https://about.gitlab.com/handbook/product/#content-of-an-mvp)
for more detail). Most of the communication may happen within the issue
comments, but some may happen offline (such as via Slack). Ensure that any
relevant information that arise as part of an offline conversation is added to
the issue title and issue description. As a PM you must ensure that issues
have enough detail added to them before they become actionable as part of
an iteration.

The near-term roadmap will also help planning for capacity with engineering
and UX in order to commit to the contents of the next release.

#### Long-term

For longer term, you need to create and maintain a vision for your
category and areas of responsibilities. This lives either on the [direction page][/direction]
or is linked from there, e.g. `/direction/create`.

Your long-term vision should be more concrete for things that are closer in time,
and vice versa. The format of the [2018 vision](https://about.gitlab.com/direction/product-vision/)
is a great way to structure your vision. You're free to do otherwise,
just make sure it's easily consumable from the website.

The purpose of this page or addition to the direction page is to make it clear in
what greater context individual changes fall. E.g. you might deliver a feature that
allows admins to track username changes. That is not very interesting and hard to sell -
but if it's clear that this is part of a greater push to improve auditing in GitLab,
this becomes an enticing part of a greater whole.

To further communicate the plans we have, you should present your vision to
anyone that is interested in listening, record it, publish it on YouTube and
add that to the top of your vision. This will make it much easier to consume
the content.

It's okay if your vision changes over time. Ideally, what you'll change are minor
things: links, issues, smaller features. Large, strategic initiatives are unlikely to
change frequently - when they do, it's probably worth talking about (i.e. redoing the video).

#### Special consideration

The roadmap should also delimit which items will be delivered prior to the
next [summit](https://about.gitlab.com/culture/summits/), as well as prior to
the end of the current calendar year. These delimitations will help determine
both the internal and external communication for both product and marketing.

### Important dates PMs should keep in mind

- **1st** - Scope/capacity for the upcoming release has been agreed on between
  product/engineering/UX (released the month following, not the current month)
- **7th** - Code freeze for the current release goes into effect. After this
  date you should not commit to any last minute requests (issues that are
  critical, such as security vulnerabilities, are generally handled directly
  by engineering). Also, update the [Kickoff document](https://docs.google.com/document/d/1ElPkZ90A8ey_iOkTvUs_ByMlwKK6NAB2VOK5835wYK0/edit)
  to explicitly declare which items did and did not get merged for the current
  release. Notify your manager of anything that did not make it, [if you haven't already](https://about.gitlab.com/handbook/product/#shifting-commitment-mid-iteration).
- **8th** - Kickoff call for upcoming release (published the month
  following). This is a live-streamed call where PMs communicate the features
  their teams will focus on for the upcoming release. The kickoff does not have
  to include every single issue included in the iteration; it should focus on
  major work/features as defined by the `direction` label. i.e. all items
  mentioned at the Kickoff should have the `direction` label, and all
  `direction` items that are marked as `Deliverable` for the upcoming release
  should be mentioned. Issues such as documentation or minor fixes need not be
  mentioned. Same applies to exploration issues.
- **14th** (6th working day before the 22nd) - All relevant items in your area have been added to the [release post draft]
  (https://about.gitlab.com/handbook/marketing/blog/release-posts/) for the
  current release.
- **15th** - [Team retrospective](https://about.gitlab.com/handbook/engineering/management/team-retrospectives)
- **22nd** - New release and blog post are published. Also, by now you should
  have a draft on the issues that will be included in the next kickoff
  (released 2 months later). Start capacity and technical discussions with
  engineering/UX.

(current release = published this month, upcoming release = published next month)

### Dogfood everything

The best way to understand what pains users experience is to go through what we
ask them to do to set up or use GitLab. As a PM, you should go through
every feature, at the minimum the ones you are responsible for. All of them. That
includes features that are not in GitLab's UI directly but require server
configuration. If you, as a PM, can't understand the documentation, or if you
struggle to install something, would anyone else bother to do it too? Going
through this is not only beneficial for understanding what the pain points are,
it will also tell you what can be enhanced, such as a better flow or better
documentation.

As a Product function, it is our responsibility to ensure that the entire
company is dogfooding.

#### Example: configuring GitLab

Most of GitLab is configured through the file `gitlab.rb`. It's tempting to
add a new parameter in this file - it's easy, fast to do, and won't require
adding a new UI element to allow the configuration of this new setting. However,
changing this file requires you to reconfigure GitLab. To do that, you have to
login to your server and type in commands to reconfigure your instance,
possibly multiple times if you have more than one server.

This is not something that we can ask our customers to do. Only by using your
own product and features will you realize that some practices should be avoided
as much as possible.

### Product Workflow

Almost everything that we do is documented in issues.

#### How to submit a new issue

1. If you have time, the first thing you should do is search both CE and EE
projects to see if a similar issue already exists. We shouldn't create
duplicates if we can avoid them.
1. Identify if the issue is about GitLab Community Edition (CE) or GitLab
Enterprise Edition (EE), although this can easily be changed later.
1. You should clearly state what the current pain point is, what we are trying
to solve, what the benefits will be, what it should do, how to accomplish that
and the next steps.
1. The body of the issue should be written in a clear way, without ambiguity.
1. The initial issue should be about the problem we are solving.  If a separate [product discovery issue](#product-discovery-issues) is needed for additional research and design work, it will be created by a PM or UX person.
1. If the body contains too many paragraphs, it can surely be rewritten to be shorter.
1. Do not use acronyms or abbreviations. Everyone should be able to jump on the
issue and participate without needing a glossary.
1. Choose labels which are relevant to the issue. If you are unsure about what
certain labels are for, check the labels pages ([CE](https://gitlab.com/gitlab-org/gitlab-ce/labels)
or [EE](https://gitlab.com/gitlab-org/gitlab-ee/labels)), and read the
descriptions. The [contributing doc](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md)
provides a breakdown of the label types and how to choose the right label.
1. Unless you know what you are doing, do not
    - assign someone to the issue
    - assign a milestone
    - set a due date
    - add weight - weight represents the technical complexity and should be
    defined by our developers
1. Mention the different stakeholders in the body of your issue. In most product
related issues, we usually mention the product manager, the design, frontend, and backend managers as appropriate.
Some teams have [experts](/team/structure/#expert) or [liaisons](/job-families/liaison) that can be mentioned instead of the managers.
Mentioning the people in the body of the issue will trigger the notification mechanisms
chosen by the people who are mentioned - therefore there is no need to notify
people in another channel after the issue has been created (Slack, email).

#### How to use epics

Issues related to the same feature should be bundled together into an
into an [epic](https://docs.gitlab.com/ee/user/group/epics/).

##### Epics for a single iteration

Big features may include multiple issues even if we are just targeting an MVC.
In this case, we should use an epic to collect all of them in one single place.
This epic should have a start and an end date, and it should not span more than
3 releases, otherwise we run the risk of having epics drag on indefinitely. When
these issues are finished and closed, we should have successfully achieved the
epic's goal. A good example of this kind of epic is the first iteration on a new
feature.

##### Epics for a long-term plan

We can use epics also to track many issues related to a specific topic, even if
we don't have a specific timeline to ship them in. These
epics should be marked as ~meta and they may not have a specific start or end
date. This is useful to have an overview of the future. A good example of this
kind of epic is to collect all the changes for a post-MVC of a given feature,
in order to bring it to be feature complete.

#### Product Discovery Issues

When a product discovery step is needed to design a feature, PMs should
create a separate issue (linked to the epic and implementation issue) for that
research and design work to occur.  We should not repurpose or otherwise reuse
the existing implementation issue; doing so creates a risk of the issue being
closed when the design work is complete and thereby losing track of the actual
delivery of the item.

It's also important to ensure that product discovery issue is really even
needed.  It's possible in many situations to simply use the initial ticket for
any design discussions - this will ensure all of the back and forth is in one
place, avoiding the risk of losing track of parts of the discussion.  If you
find you are creating a issue simply to reserve time or people on the roadmap,
consider trying to secure the capacity in another way.

In certain cases a product discovery issue can be worked ahead of time, but a
best-practice for good product development is to plan for and do this sort of
research and development work within the milestone, including engineering and other
stakeholders directly. Doing product discovery ahead of time, without the full
group is generally not an effective approach..  Because we aim to deliver MVC
features, there should almost always be enough time in a single release to both
research and deliver a feature that adds value for our customers.

Be sure to follow the [CE contribution guidelines](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#implement-design-ui-elements) on correct
labeling practices for the ``product discovery`` label.

#### Wireframes

When relevant, you can include a wireframe in your issues in order to illustrate
your point. You don't need to include wireframes on your own; our UX/design team can
help us on that matter. Simply ping them if you need their help. We like
[Balsamiq](https://balsamiq.com/) for its simplicity and its sketch-style approach.
If are struggling for inspiration, you can also paste screenshots of similar
features in other products.

#### What is a Meta issue?

We assign the `Meta` label to issues that contain a large list of todos. If you
are familiar with the Agile methodology, it's similar to an epic. At GitLab we
have a short release cycle: the 22nd of every month. In some cases we won't be
able to tackle all the tasks of a meta issue in a single release. This is why
we centralize everything that we need to do in a meta issue, then break it
down to issues small enough that they will fit into one release. Most of the
time, meta issues generate lots of comments and passionate discussions. As a
consequence, they always lead to something great.

Meta issues themselves generally should not be assigned to a milestone as the
actual work is covered in sub-issues. Sometimes, for example if you want a meta
issue to show up in our [direction](/direction) page for a given release, you may
add a milestone, but *only* if you know for sure that all sub-issues will be
*completed* by that milestone. Don't assign a milestone for when you're going to
*start* a meta issue.

#### Long-lasting issues

A general guideline is that an issue should only span one release. If we know an
issue is going to span multiple releases, split it up into multiple issues.

Meta/epic issues are the exception to this rule, but should be kept to a
minimum and only serve to guide broader subjects, not a single feature
over multiple releases. This is to make sure we stick to our values of
the [minimally viable change](#the-minimally-viable-change).
This means that feature issues should be closed after the first iteration
whenever possible. We'll know more in the future and this keeps any remaining
issues short and actionable.

In addition, it's often a good idea to throw away an original plan and
start fresh. Try to do this more often, even more than you're comfortable with.
Close the issue and create a new one.

#### Which issue should you be working on?

When you don't have any specific tasks assigned, you should work on issues that are
labeled `Product work`, in both the EE and CE projects. These are issues that need
our attention the most.

#### Feature assurance

Before a new features is shipped, the PM should test it out to make sure it
solves the original problem effectively. This is not about quality assurance
(QA), as developers are responsible for the quality of their code. This is about
feature assurance (FA). Feature assurance is necessary because sometimes there
are misunderstandings between the original issue proposal and the final
implementation. Sometimes features don't actually solve the intended problem,
even though it seemed like it would, and sometimes solutions just don't feel as
useful as intended when actually implemented.

If you can test out the feature during development, pulling down branches
locally (or with a review app!), that's great. But sometimes it's not feasible
to test a feature until it's bundled into a release candidate and deployed to
GitLab.com. If so, make sure to test out features as soon as possible so any new
issues can be addressed before final release. Also, take the FA cycle into
account when scheduling new milestone work.

If you are looking to test code that has not been merged to GitLab.com or is not yet
part of an RC, you can pull the branch down locally and test it using the [GitLab
Development Kit (GDK)](https://gitlab.com/gitlab-org/gitlab-development-kit).

#### Managing Upcoming Releases

Refer to the [Product Development Timeline](/handbook/engineering/workflow/#product-development-timeline)
for details on how Product works with UX and Engineering to schedule and work on
issues in upcoming releases.

#### Planning for Future Releases
{: #planning-future-release}

Product Managers assign milestones to issues to indicate when an issue is likely
to be scheduled and worked on. As we consider more distant milestones, the certainty of
the scope of their assigned issues and their implementation timelines is increasingly
vague. In particular, issues may be moved to another project, disassembled, or merged
with other issues over time as they bounce between different milestones.

The milestone of an issue can be changed at any moment. The current assigned milestone
reflects the current planning, so if the plan changes, the milestone should be updated
as soon as possible to reflect the changed plan.  We make sure to do this ahead
of starting work on a release. Capacity is discussed between the PMs and the
engineering managers.

In general, closer-to-current-time milestones are assigned to issues that are
higher priority. The timing also reflects an approximate product roadmap, with more
distant milestones reflecting increasing uncertainty.

The milestones are:

- Milestones associated with an actual upcoming release, e.g. `9.4`, `9.5`, etc.
- `Next 3-4 releases`
- `Next 4-7 releases`

These assigned milestones should be used as a signal for GitLab stakeholders and
collaborators, to help them with their own respective workflows.

In addition, we have two special milestones: `Backlog` and `Awaiting further demand`.
Product Managers assign these issues to milestones that they have reviewed and
make sense, but do not fit within the upcoming release milestones due to either
a lack of comparitive urgency or because we have not yet seen enough user
demand to prioritize the item yet.  The best way to demonstrate urgency on
either of these items is to vote on them and, if possible, add comments
explaining your use case and why this is important to you.

Again, the milestone of an issue can be changed at any moment, including for both
of these special milestones.

For a detailed timeline, see [the product development timeline](/handbook/engineering/workflow/#product-development-timeline).

#### Content of an MVP

We only ship in a Minimally Viable Product style. Here are some guidelines about
it:

* The issue should be the smallest iteration we can do to address the problem.
* The issue that describes the change should be as concise a possible, while
  providing enough information to understand:
    * the context
    * what we want to achieve
    * who it is for
    * what the use cases are
* The MVP should be achievable in one iteration.
* If relevant, check if we can measure the usage of the feature by modifying the
  usage ping.
* If the issue generates a lot of discussion, make sure that the issue
  description always reflects the latest decisions at the current point in time.
* Feel free to edit the issue description without keeping a history of the
  previous content, as long as it reflects the latest decisions.
* It's not shipped until it's documented, no matter what the change is.

#### When to create or close an issue

You should create an issue if:

- There isn't already an issue for what you're intending to write. Search first.
- a feature is mentioned in chat channels like #product, #competition or elsewhere
- a customer requests a particular feature

You should consider **not** creating an issue when:

- It's an iteration on something we haven't built yet.
- You're planning very far ahead and it's something specific. The further away something is,
the more vague or encompassing the issue should be. So, for example, create just one issue
for a distant new feature, rather than several issues that will follow each other.
This will reduce the total amount of issues.
- There is already an existing issue. Even if the quality is low, people might
have linked to it. Consider rewriting the description instead and leaving a comment
that you did so. Closing issues to reopen the same issue is generally not a good idea.

Close issues that are either:

1. duplicated elsewhere.
1. no longer relevant due to other reasons.
1. 'not the next iteration': an iteration on a proposed feature that is unlikely to ship in the next few months.

When closing an issue, leave a comment explaining why you're closing the issue and link
to anything of relevance (the other duplicate, the original feature that this is an iteration on, etc).

The 'not the next iteration' issues are the most important ones to resolve.
It is very easy to create a big plan with meta issues and lots of improvements, <-- this sentence was incomplete, so this is a guess -->
but it is essential that we iterate and ship the _minimum viable_ change.
We have to ship the iteration, wait for it to be used, and look for the feedback.
As a product manager you must think about the bigger picture when making a proposal to improve the product.
It's important to avoid writing this down as a bunch of issues.
Come up with a plan but only record the first step.
This way we can preserve the efficiency of [our value of iteration](/handbook/values/#iteration).
Closing issues whenever possible is an important part of your job and helps to keep a clear view of what is next.
Consider using the following template to close an issue:

> Closing this because XXX is something we should do first. When that feature is
finished, we can learn from observing it in use. If we learn that this issue is
still relevant, we can then reopen it. See /handbook/product/#when-to-create-or-close-an-issue
for more detail about this policy.

#### Competition Channel

When someone posts information in the `#competition` channel that warrants
creating an issue and/or [a change in `features.yml`][features], follow this
procedure:

- Create a thread on the item by posting `I'm documenting this`
- Either do the following yourself, or [link](#competition-channel)
to this paragraph for the person picking this up to follow
- If needed: create an issue
- [Add the item to the `features.yml`][features]
- If GitLab does not have this feature yet, link to the issue you created
- Finish the thread with a link to the commit and issue

#### Shifting commitment mid-iteration

From time to time, there may be circumstances that change the ability for a team
to ship the features/issues they committed to at the beginning of the iteration.
When this happens, as a PM you must ensure the related issues  and the roadmap
are updated to reflect the new plan (for example, remove `deliverable`
tag, update `milestone`, etc.). Additionally, notify your manager of the shift
and update the [kick-off document](https://docs.google.com/document/d/1ElPkZ90A8ey_iOkTvUs_ByMlwKK6NAB2VOK5835wYK0/edit)
to reflect the status of the item within the iteration (merged, not merged).

### Where should you look when you need help?

* The first thing you should do is read this page carefully, as well as the
[general handbook](/handbook/).
* You can ask questions related to Product in the `#product` Slack channel.
* General questions should be asked in `#questions`.
* Specific Git related questions should be asked in `#git-help`.
* HR questions should be asked in `#peopleops`.

### Shipping

#### Internal and external evangelization

Before shipping a new or updated feature, you are responsible for championing
it, both internally and externally. When something is released, the
following teams need to be aware of it as they will all need to do something
about it:

* Marketing: depending on the importance of the feature, we need the help of
marketing to promote this feature on our different communication channels.
* Sales: sales needs to know what's new or changed in the product so they can
have better arguments to convince new or existing customers during their sales
process.
* Support: as they are in constant contact with our users and customers,
support should know exactly how our products work.

You can promote your work in several ways:

* start with documenting what will be released and share this documentation with
the different teams
* schedule meetings, if you think it's important, with the teams listed above.

#### GitLab University

To promote a major new feature internally, you can ask to host a GitLab <-- internal promotion, but GitLab University is external? -->
University, a company wide demo session. This is a great opportunity to make
sure every one is on the same page.

### Major feature rollout

Major features deserve proper attention from Product and Marketing. With a
proper rollout, we'll have ample marketing opportunities and receive more
feedback ahead of, during, and after the release.

Here is the ideal rollout schedule. For each step there is an indication for
who is responsible for it.

1. Feature is drafted in an issue (PM)
1. Feature is planned in an upcoming release (PM)
1. A feature proposal blog post is made (PM or Dev), which includes:
	* What we are planning on doing.
	* How people will be able to get it: CE or any EE Editions.
	* A link to the issue.
	* When it'll be available, if possible.
	* Anything else that is interesting to share in order to fuel the discussion.
1. Feature is implemented, and documentation is written (Dev).
1. Feature should appear on the website (Marketing)
	* For very significant features: Feature page on the website is made and
      pushed, with the mention "Available from X.X"
	* For other features: Feature should be listed on some page (/comparison,
      Enterprise page, /features page).
1. Feature is launched with the release (Marketing)
	* "Available from X.X" is removed
	* Documentation and other resources are linked
	* Pricing page is updated if needed
1. Feature is highlighted in a blog post (Marketing)
	* This post is linked from the feature page on the website (if applicable)

### Communicating product vision

Occasionally, we rally around a product vision, a direction to aim towards, to
improve alignment internally and externally. We usually start out with a clear,
simple concept like [going faster from idea to production](/2016/08/05/continuous-integration-delivery-and-deployment-with-gitlab/#from-idea-to-production-with-gitlab),
or shipping [complete DevOps](/2017/10/04/devops-strategy/). We announced our
first Master Plan as part of our [Series B funding announcement](/2016/09/13/gitlab-master-plan/),
and our second master plan with our [Series C announcement](/2017/10/09/gitlab-raises-20-million-to-complete-devops/).
While the first iterations and presentations are great for aligning the product team
and announcing the vision to the world, the text and slides only go so far to
convey the depth of the vision. So, we usually iterate on the vision by fleshing
it out more in various stages and communicating it in different ways, usually
increasing fidelity over time.

This iteration may look like this, for example:
* start with a [Google doc](https://docs.google.com/document/d/1TKqHSwCdxXOb27cqKoHOrnYIA4waZE25SVsexLqp8zE/edit),
* turn that into a [single-source-of-truth based on issues](/direction/product-vision/),
* then [slideware](https://docs.google.com/presentation/d/1d6vL4dz-V_JxiStu4keL01SLd7w0JfNfcHzyetczp7k/edit)
* then a [mockupware video](https://youtu.be/lRAKmTzpGXE)
* then an [interactive prototype](https://framer.cloud/UaofH/index.html) and [recorded video](https://youtu.be/RmSTLGnEmpQ)
* then a seamless, but still fake video demo
* then finally a production demo.

The interactive prototype video is a good time to reiterate the vision
with a blog post.

Additionally, the [direction page](/direction/#devops-stages) contains the specific vision for each devops stage along with 
links to the epics that contain the work to be done. We aim to use these epics and issues as the single source of truth for 
our plans, and as such we strive to maintain them up-to-date with the latest developments and plans.

### How and when to reject a feature request

Rejecting a feature request or a merge request is not an easy thing. People can
feel quite protective of their ideas. They might have invested a lot of time and
energy in writing those ideas. You can be tempted to accept a feature only to
avoid hurting the people who thought of it. Even Worse, if you reject an idea too
harshly, you might discourage other people to contribute, which is something we
should strive to avoid.

However, as the number of issues and merge requests grows incessantly, we should
be diligent about rejecting features we are sure will not work out. It's better for
everyone: for the product team, so we don't maintain a huge backlog of things we
will never do anyway, and for the users who won't have to wait for our feedback
indefinitely.

Note: it's fine to not respond to issues that we think have potential until they
gather momentum.

Feature requests and merge requests can be rejected for the following reasons:

* Not within our scope: the Direction page [lists all the areas](/direction/#scope)
where GitLab, the product, won't go. Point the issue's author to this article
and close the issue.
* We don't want another setting: whenever we can, we try to [avoid having settings](#convention-over-configuration).
Some settings are unavoidable, but most aren't. Ask the user to change how she
approaches the feature in order to get rid of the setting.
* Too complex: We want to have a simple, user-friendly product that does complex
things, not the other way around. Tell the user to take a step back and think
about the problem to be solved in the first place. Offer directions on
what could be done instead. If she's not willing to do it, indicate that you will
have to close the issue/merge request because it will go nowhere.
* Brings an Enterprise exclusive feature to the Community Edition: this problem
is already addressed in the [Stewardship page](/stewardship/#contributing-an-existing-ee-feature-to-ce).
Indicate that we will investigate whether the feature can be ported to the
Community Edition, discuss it with other teams members and come back to the user
in a timely fashion.
* Low priority: sometimes features are interesting but we simply don't have the
capacity to implement them. In that case, simply tell the truth and indicate that
we don't have enough resources at our disposal to do it at the moment.

Don't forget to thank the authors for the time and effort taken to submit the
feature request/merge request. In all cases and without exception, you should be
nice and polite when interacting with users and customers.

### Responsibilities and Expectations

As a PM you're expected to:

- Follow the issues you've been involved with / are assigned to as a PM. That
  includes reading all comments. Use email notifications for this.
- Make sure the issue description and title is updated when necessary. It
  should always reflect the current state of the issue.
- Make sure issues are moved forward when needed. You should not only avoid
  being the bottleneck, you should also be the person moving issues forward when
  they get stuck or overlooked.
- Make sure features solve the original problem effectively.
- Make sure features are complete: documentation, marketing, API, etc.
- Know when to cut corners and when not to. If we merge documentation a day
  later, that's usually acceptable. Conversely though, learning from a customer
  that documentation is lacking is not.
- Excite and market new features and changes internally and externally.
- Help build a vision for GitLab and GitLab's features.
- Understand deeply whatever it is you're working on. You should be spending a
  lot of time learning about your subject matter.
- Have regular meetings (at least once a week) with customers.
- Make sure marketing materials related to your work are up to date.

#### Customer meetings

It's important to get direct feedback from our customers on things we've
built, are building or should be building.

As a PM you should have regular meetings with customers that are using the
things you've been working on, and also with customers that are not in order
to get an idea of why they're not switching to our solution.

##### Set up a meeting

To set up a customer meeting, identify what you're interested in learning
and prepare appropriately.

You can find information about how customers are using GitLab through Sales
and version.gitlab.com. Sales and support should also be able to bring you
into contact with customers.

There is no formal internal process to schedule a customer meeting, but
if the need arises, we can formulate one.

##### During and after

During the meeting, spend most of your time listening and obtaining information.
It's not your job to sell GitLab, but it should be obvious when it's the time
to give more information about our products.

After the meeting, make sure all your notes and feedback land in issues.

#### Marketing materials

As a PM you're responsible for making sure changes you've shipped are well represented
throughout GitLab's documentation and marketing materials. This means that on
release, [`features.yml`][features] is updated, documentation is merged and deployed, and
any existing content is updated where necessary.

It's not acceptable to do this after the release. GitLab is very complex, and features
and functions are easily missed, even those that provide significant value to customers
(e.g. the many ways you can authenticate with GitLab).

You can recruit the help of the marketing and technical writing team if needed,
but it's highly recommended to do small updates yourself. This takes less time
and overhead than communicating what needs to be done to someone else.

#### Release posts

As a PM, you are [accountable](/handbook/marketing/blog/release-posts/#general-contributions)
for adding new features (under your umbrella) to the monthly release post, respecting the
guidelines defined in the
[release posts handbook](/handbook/marketing/blog/release-posts/) and its **due dates**.
Be sure to go over all the details.

Every month, a PM will take the
[leadership](/handbook/marketing/blog/release-posts/#authorship)
of the release post, and will be responsible for delivering it in time.

### Communication guidelines for product managers

As a product manager, you're vastly more knowledgeable about GitLab than others.
This means that you have the responsibility to always provide a balanced and complete
view when discussing anything related to product. Other people won't have the same
background and context you might have.

For example, when someone involved in sales asks you about upcoming issues in a particular
area, you would respond with:

- a clear overview of what is coming (link to the single source of truth)
- how that relates to the customer's request
- that this is flexible and we are interested in hearing more from the customer
- if necessary: a suggestion to discuss this directly with the customer

This seems obvious, but a slight misunderstanding can have big consequences, for
example: promising a customer that something will be done by a certain date is very
different than indicating that we're working on something and hope to have a first
iteration in the near future.

#### Issue state
<-- This section seems to repeat a lot of the "When to create or close an issue" section -->

When an issue is open, this signals that we're intending or considering implementing that change.
It's important to close issues that we're not considering implementing in the near future,
so that we avoid creating uncertainty with customers, and colleagues.

When closing an issue for this reason, make sure to update the issue body and leave a comment
explaining why the issue is being closed. Issues can be reopened if we change our stance on them.

#### Working with Product Marketing (PMM)

Product marketers and managers should be joined at the hip. Just as a feature without documentation
should not be considered shipped, benefits of GitLab that we're not actively talking about might
as well not exist.

Product marketers rely on product managers to be guided to what is important and high impact.
In general, you should:

- always mention the [appropriate PMM](/handbook/product/categories) on epics and high level issues
- regularly meet/talk async with the PMM that is aligned with your product area
- proactively reach out for input when contemplating new features
- involve PMM as early as possible with work on important changes

## Permissions in GitLab

Use this section as guidance for using existing features and developing new ones.

1. Guests are not active contributors in private projects. They can only see, and leave comments and issues.
1. Reporters are read-only contributors: they can't write to the repository, but can on issues.
1. Developers are direct contributors, and have access to everything to go from idea to production,
   unless something has been explicitly restricted (e.g. through branch protection).
1. Masters are super-developers: they are able to push to master, deploy to production.
   This role is often held by maintainers and engineering managers.
1. Admin-only features can only be found in `/admin`. Outside of that, admins are the same as the highest possible permission (owner).
1. Owners are essentially group-admins. They can give access to groups and have
   destructive capabilities.

To keep the permissions system clear and consistent we should improve our roles to match common flows
instead of introducing more and more permission configurations on each resource.

For big instances with many users, having one role for creating projects, doing code review and managing teams may be insufficient.
So, in the long term, we want our permission system to explicitly cover the next roles:

1. An owner. A role with destructive and workflow enforcing permissions.
1. A manager. A role to keep a project running, add new team members etc.
1. A higher development role to do code review, approve contributions, and other development related tasks.

All the above can be achieved by iteratively improving existing roles and maybe [adding one more](https://gitlab.com/gitlab-org/gitlab-ce/issues/45414).

[Documentation on permissions](https://docs.gitlab.com/ee/user/permissions.html)

## Internationalisation

GitLab is developed in English, but supports the contribution of other
languages.

GitLab will always default to English. We will not infer the language /
location / nationality of the user and change the language based on that.
You can't safely infer user preferences from their system settings either.
Technical users are used to this, usually writing software in English,
even though their language in the office is different.

## Paid Tiers

### Talking about Paid-only decisions

When talking about why a certain change goes into a Paid tier instead of Core, mention the [stewardship page][stewardship] in the handbook
directly and link to it.

[stewardship]: /stewardship/#what-features-are-paid-only

### Stewardship

Our stewardship of the open source project that is GitLab Community Edition is incredibly important.
We are expected to act as good stewards and have to work hard to maintain that right, which is documented
on the [stewardship page][stewardship].

If you want to make any changes to this page, create a merge request and assign it to the CEO.

### What goes in what paid tier

Please see [The likely type of buyer determines what features go in what tier](/handbook/product/pricing/#the-likely-type-of-buyer-determines-what-features-go-in-what-tier).

### Starter, Premium, and Ultimate requirements

All Starter, Premium, and Ultimate features must:

- Work easily for our customers that self-host GitLab. i.e. Their
  licenses need not be updated and the new feature is default-on for the
  instance.
- Work with GitLab.com Bronze / Silver / Gold subscriptions. This means there has to be
  some way of toggling or using the feature at a namespace level.
- Have documentation.
- Be featured on [products](/products) and [comparison](/comparison) at launch.

### Pricing plans

For more information about how we think about pricing, please see the
[pricing page in the handbook](/handbook/product/pricing/).

### Designing features for paid tiers

To make it possible to ship a feature for paid tiers, ideally the code is
completely separate. For example, the frontend and backend of the feature only exist in
the `gitlab-ee` project. However, this is not always possible.

In cases where it's preferable to have the backend code live in the `gitlab-ce`
repository, it's acceptable to only ship the frontend for the feature in EE.
In practice this makes the feature paid-only.

### Bringing features to lower tiers

If you are considering bringing a feature that exists in Premium to Core, for
example, follow this process:

- Get approval from either the VP or Head of Product, and the CEO
- Create a confidential issue describing the plan and the reasons behind this change
- Share this issue for feedback with the rest of the team at GitLab
- Join the weekly Sales Team call on Mondays at 9am Pacific, explain the proposal,
  and ask for feedback there or in the issue

After appropriate consideration, update all stakeholders on the decision that you've made
and move forward with making that change (or simply close the issue with the reasoning for why not).

## GitLab.com

GitLab.com runs GitLab Enterprise Edition.

To keep our code easy to maintain and to make sure everyone reaps the benefits
of all our efforts, we will not separate GitLab.com codebase from the Enterprise Edition codebase.

To avoid complexity, [GitLab.com tiers and GitLab self-managed tiers](/handbook/marketing/product-marketing/#tiers) have a 1:1 match.
No exceptions to this rule are acceptable.

- Free: Core features
- Bronze: Starter features
- Silver: Premium features
- Gold: Ultimate features
- Public projects are considered to have a Gold subscription level

Since we are not able to give admin access and do not yet have full feature
parity between self-managed instances and GitLab.com, we avoid saying that there is
a one to one match between subscription levels and tiers in marketing materials.
This has been a source of confusion in the past for customers.

### Restriction of closed source Javascript

In addition, to meet the [ethical criteria of GNU](https://www.gnu.org/software/repo-criteria-evaluation.html),
all our javascript code on GitLab.com has to be free as in freedom.
Read more about this on [GNU's website](https://www.gnu.org/philosophy/javascript-trap.html).

## Private tools and dashboards for monitoring and KPI tracking

[Feature usage](https://redash.gitlab.com/dashboard/feature-adoption)

[EE usage](https://version.gitlab.com/): dev.gitlab.org account

[Grafana](https://dashboards.gitlab.net): Google gitlab.com account

[Kibana](https://log.gitlab.net): dev.gitlab.org account

[S3stat](https://www.s3stat.com): GitLab 1Password account

[Sentry](https://sentry.gitlap.com): dev.gitlab.org account

## Writing about features

As PM we need to constantly write about the features we ship: in a blog post,
internally to promote something, and in emails sent to customers.

While we want every PM to have a unique voice and style, there are some
guidelines that one should take into account when writing about features. Let's
highlight them with a concrete example, Preventing Secrets in your repositories,
 that [we shipped in 8.12](/2016/09/22/gitlab-8-12-released/#preventing-secrets-in-your-repositories-ee).

* Start with the context. Explain what the current situation is without the
  feature. Describe the pain points.

> It's a bad idea to commit secrets (such as keys and certificates) to your
repositories: they'll be cloned to the machines of anyone that has access to the
repository. If just a single one is insecure, the information will be
compromised. Unfortunately, it can happen quite easily. You write
`git commit -am 'quickfix' && git push` and suddenly you've committed files that
were meant to stay local!

* Explain what we've shipped to fix this problem.

> GitLab now has a new push rule that will prevent commits with secrets from entering the repository.

* Describe how to use the feature in simple terms.

> Just check the checkbox in the repository settings, under push rules and
GitLab will prevent common unsafe files such as .pem and .key from being committed.

* Point to the documentation and any other relevant links (previous posts, etc).

### Writing release blog posts

For every monthly release, there is a blog post announcing features.
The blog post should contain everything _exciting_ or _disruptive_.
All new features should appear in the blog post.
We want to help people understand exciting features (which are often new), and increase adoption.
Disruptive features may change workflows or even introduce unavoidable inconveniences.
We want to anticipate questions and avoid confusion by communicating these changes through the blog post.
Smaller tweaks and bug fixes don't necessarily need to be mentioned,
but if interesting, can be included at the bottom of the post.

## Areas

There is a hierarchy of bundling features:
<-- hierarchy? In general, this whole section is unclear. What is an area, exactly? -->

1. DevOps lifecycle stages (stages), see [SDLC](/sdlc/)
1. Product categories (categories), see [SDLC](/sdlc/)
1. Feature areas (areas), see end of ['Plan Positioning' Google Doc](https://docs.google.com/document/d/19RNBDoy-rLmR3PEhN8GJVOdb8Et2-IMjaMPYcXzUUEI/edit#)
1. Individual features (features), see [Features](/features/)

The areas are used to position the plans (CE, Starter, Premium, Ultimate).
Each plan has a maximum of 7 areas.

When we introduce a new feature we look for each plan if it matches an area.
We start at Ultimate and go down to CE, the first area that matches is the plan for the feature.
For CE the areas are equal to the 7 stages of the DevOps lifecycle.
This is because if areas of non-CE plans don't match it ends up in CE, so it has to cover everyone.

## Links

- [Engineering Workflow](/handbook/engineering/workflow)
- [Release posts handbook](/handbook/marketing/blog/release-posts/)

[features]: https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/doc/features.md
