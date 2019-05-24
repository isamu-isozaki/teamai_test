---
layout: markdown_page
title: Creating a DSE trigger (for Resellers/index.html.md)
category: Zendesk
---

### On this page
{:.no_toc}

- TOC
{:toc}

----


## Workflow - Adding DSE triggers to ZenDesk

### Overview


Use this workflow when adding a DSE trigger to ZenDesk as part of the Dedicated Support Engineering policy - https://github.com/isamu-isozaki/teamai_test/tree/master/support/#dedicated-support-engineers

______________

### Workflow



1. Ensure the reseller organization exists in ZenDesk
   - Search for the organization email domain in https://gitlab.zendesk.com/agent/admin/people
   - If the organization does not exist, create a new organization
https://gitlab.zendesk.com/agent/organizations/new

1. Navigate to the trigger page in ZenDesk (administrator account required/index.html.md)
   - https://gitlab.zendesk.com/agent/admin/triggers

1. Click â€œadd triggerâ€

1. **Trigger title:** DSE: Assign {RESELLER} to {AGENT}

*Configure the trigger with the following conditions:*

```
Meet all of the following conditions:
Ticket: Organization is {COMPANY}

Perform these actions:
Ticket: Assignee {AGENT}
Ticket: Priority High

```
*Replace {RESELLER} with the organization name (see first step/index.html.md). Replace {AGENT} with the Support Engineers first name.*
