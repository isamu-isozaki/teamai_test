---
layout: markdown_page
title: Setting ticket priority
category: Zendesk
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

## Setting Ticket Priority

Manually setting a ticket's priority in Zendesk will change the overall ticket [SLA](/handbook/support/support-engineering/prioritizing-tickets.html#sla), for both the first and next replies. This allows support to prioritize the active ticket queue more effectively .

### Effect of Prioritization on SLA (non-premium customers)

| Priority | First/Next Reply - SLA (business hours) |
|----------|-----------------------------------------|
| Low      |  16 hours                               |
| Normal   |  12 hours                               |
| High     |  8 hours                                |
| Urgent   |  4 hours                                |

### Prioritization Guidelines

Tickets should be prioritized based on the guidelines below. The priority can change at any stage in a ticket's lifecycle.

#### Low

+ Minor problems
+ Fix or workaround is known
+ Core GitLab functionality is not affected, and does not affect customer's work
+ Documentation related
+ General information questions
+ Feature requests

#### Normal

+ Minor problems
+ GitLab is not functioning correctly
+ Customers may be inconvenienced, but are able to continue working
+ Low impact on general GitLab usage

#### High

+ Major problems
+ Partial loss of GitLab functionality
+ Customer's ability to operate is seriously affected
+ High impact on GitLab usage

#### Urgent

+ Major emergencies only
+ Full loss of GitLab functionality, service is completely unavailable
+ GitHost (GitLab Hosted) instance down
+ Customers cannot continue to work at all
