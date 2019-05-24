---
layout: markdown_page
title: Customer calls
category: General
---

## On this page
{:.no_toc}

- TOC
{:toc}

----

## Customer calls

### Scheduled calls

All scheduled calls should be organized via the support project [issue tracker](https://gitlab.com/gitlab-com/support/support-team-meta/issues/index.html.md) using the [customer call template](https://gitlab.com/gitlab-com/support/support-team-meta/blob/master/.gitlab/issue_templates/Customer%20call.md/index.html.md).

The template can be used when coordinating a call with other engineering/sales team members or when scheduling another Support Engineer in a more preferable timezone.

#### Intake, upgrade and installation support

For Premium Support customers, and customers who have purchased Implementation Support, we offer intake and installation support. Premium Support customers also receive live upgrade assistance. The different levels of service that are offered are described on the [support page](/support/index.html.md), and Implementation Support is described in more detail in the [support handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/support/#implementation-support/index.html.md).

Call/screen sharing sessions involve guiding customers through the GitLab upgrade process or taking control of the customers server to perform the upgrade. You should make sure that the customer has a backup before you start the call, as they can take a lot of time to complete and you don't want to do them while in the call. You should also make sure you know as

**Important information to collect**

1. Type of installation: Source/Omnibus
1. Current GitLab version
1. Version you're upgrading to (it isn't always the latest/index.html.md)
1. Use of GitLab CI (need to upgrade to 8.0 first, then 8.+/index.html.md)

We collect this information in Zendesk and link it to the organization, see the
[responding to tickets section in onboarding](https://github.com/isamu-isozaki/teamai_test/tree/master/support/onboarding/index.html.md).

### Unscheduled calls

While engaging with customers you should always be prepared to jump on a call with them. It is easier to get
all the information you might need on a 20 minute call than on 10 2-minute emails. If a conversation goes through
several back and forth emails and the problem still isn't close to being resolved, suggest a call via WebEx or
Google Hangouts.

If you feel too inexperienced to handle a call, ask someone more experienced to handle the call and
listen in if at all possible. After someone else had the call with the customer it is still your responsibility
to handle the ticket as long as the ticket is still assigned to you.

#### Call summary

Following your scheduled or unscheduled call you should complete a summary of the call in Zendesk using the
macro `General::Post Customer Call`.  This will provide a record of events for the next support agent in the hot queue
as well as the customer.  It will also provide valuable information for support agents in the future who search Zendesk
looking for similar issues and their resolutions.
