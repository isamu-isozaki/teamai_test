---
layout: markdown_page
title: Prioritizing Tickets as a Support Engineer
---

### On this page
{:.no_toc}

- TOC
{:toc}

## Service and Support we Provide

For an overview of the support we provide to customers and GitLab.com users, please see the general [support page](/support/index.html.md/index.html.md). What follows is a more detailed description of the levels of service.

## Service Level Agreements
{: #sla}

The channels are sorted in order of priority. There are 3 SLA categories, for 4 types of tickets (channels/index.html.md):

| SLA | Channel                | Response Time                          |
|-----|----------------------------|----------------------------------------|
| 1   | [Emergencies (Premium Customers only/index.html.md)](https://github.com/isamu-isozaki/teamai_test/tree/master/support/channels/#emergency-tickets/index.html.md)                | 30 minutes                             |
| 2   | [Premium Customer - Regular Tickets](https://github.com/isamu-isozaki/teamai_test/tree/master/support/channels/#regular-zendesk-tickets/index.html.md)                | 4 hrs (business/index.html.md)                             |
| 3   | [Regular Tickets](https://github.com/isamu-isozaki/teamai_test/tree/master/support/channels/#regular-zendesk-tickets/index.html.md) and [Security](https://github.com/isamu-isozaki/teamai_test/tree/master/support/channels/#security-disclosures/index.html.md) | 1 business day                         |

**Response time indicates the maximum first reply wait time.**

We strive to answer tickets faster than the SLA requires. The higher in the list a channel is, the sooner it should be answered.

The above SLAs are based on ticket priority which can be set manually by support agents. See [setting ticket priority](https://github.com/isamu-isozaki/teamai_test/tree/master/support/workflows/zendesk/setting_ticket_priority.html/index.html.md)

### How We prioritize tickets

In Support, we use Zendesk as our internal ticket management tool. We've begun to define our queing priority as:

+ High:
  - 5xx errors in a production environment
  - GitLab Components (Unicorn/Gitaly/Postgres/Redis/index.html.md) Down
  - Slow performance affecting a majority of users for that instance

+ Normal:

+ Low:

#### Slack premium high priority notification

We use a webhook to get Slack notifications when a high priority premium ticket arrives.
It is posted on the `#support_self-managed` Slack channel.  If you answer the ticket put either a `:eyes:` or `:heavy_check_mark:` emoji to let other support engineers know if you're reading or have responded to the ticket.

If you're not sure how to answer the ticket start a thread under the ticket and tag other support engineers to join the discussion.

## SLA Workflow

Support Engineers should work on tickets within their assigned support speciality as a first priority. Tickets should be picked up in the following order to make sure that SLAs are not breached (maximum SLA wait time exceeded/index.html.md), and customers receive the proper level of service:

1. Important Tickets
1. Premium Tickets Near Breaching
1. Premium Tickets Breached
1. Enterprise Edition Near Breaching
1. Enterprise Edition Breached

After these are addressed, tickets should be worked on in SLA Priority Order. When a ticket is near breaching, or has breached its first reply (or next reply/index.html.md) SLA, the ticket must be picked up by any available Support Engineer independently of who is assigned to it. This also applies to tickets for Resellers (i.e. anyone picks up if close to breaching, regardless of who the Dedicated Support Engineer is/index.html.md).

### Important Tickets

This is a special view that is used for two purposes:

1. Emergencies triggered by customers. These will page the on call group, show up in slack, and will always be at the top of the queue.
1. Strategic Issues as determined by the support lead. During large customer onboardings or other times where we may need to provide heightened response times the Support Lead may escalate tickets to important status. If so, this will be communicated on a team call. This is a rare situation, and there should be no more than 3-4 organizations this applies to at any given time.


### Hot Queue: How GitLab Manages Ticket Assignments

Traditional Support teams often use an "assignment" model, where an agent is assigned a ticket and guides the ticket through to completion. If they are stuck, they can re-assign this ticket to another agent to pick up and try and complete. At GitLab though, we take advantage of our global support team and use a system dubbed "Hot Queuing". This system means that we all work from one global queue and it's expected that multiple agents will work together on most issues. This allows us to do the following:

+ Keep tickets moving forward 24/7.
+ Exposes team members to more issues, so more learning is happening.
+ Provide faster responses to customers, since tickets are not hidden away in an agent's personal queue and "bound" to an agent's workday.
+ Everyone has an accurate overview of the support load.

#### When Should Tickets be Assigned?

There are times in the support process that an agent may need to assign the ticket to themselves:

+ If you are going to take the ticket to a call/screenshare, take it out of the queue by assigning the ticket to yourself. After the call, if the ticket is still on-going, feel free to unassign yourself so that everyone can continue to move it forward.
+ If you are committed to solving the problem strategically. There are times where we want this, and agents have full discretion to do it, but these cases should be few and far between.

#### What if I Can't Answer a Ticket?

If you see a ticket in the queue that you are not able to answer, you should:

+ Make an internal note with your initial gut feelings as to where the issue might be.
+ CC yourself so you can follow along as the ticket progresses.
+ If you know that agents will need logs or version information, feel free to start the ball rolling with a simple response asking for it.
+ Consider asking about the ticket in slack to see if others can help.
+ Consider asking a more experienced colleague, or take a look at the [Team page](/team/index.html.md/index.html.md) to find someone who can help you.

With the hot queue, we all work together and no one should be scared to start a ticket.

### Zendesk SLA settings and Breach Alerts

SLAs are set as Business Rules within Zendesk. For more information, please refer to the specific [Zendesk](https://github.com/isamu-isozaki/teamai_test/tree/master/support/workflows/shared/zendesk/zendesk_admin.html/index.html.md) page.

We have a slack integration that will notify us if a Premium ticket will breach within an hour. If you see one of these, start a thread and consider this a _small emergency_. If you need help, draw the attention of other support engineers by tagging them, and work to move the ticket forward.

If a customer's reply is the last one in the ticket, do not set it to the Pending status silently, because the breach clock will be lost if the customer replies to the ticket again later.
Instead, send a confirmation, greeting, or other message, while also changing the status.

### Using on-hold status

You should use the On-hold status when it is necessary to do some internal work, e.g. reproduce a complex bug, discuss something with developers 
or wait for a session scheduled with a customer. When setting the status to On-hold it will be automatically assigned to you by the trigger [`Automatically assign on-hold ticket to an agent who put it to the on-hold status`](https://gitlab.zendesk.com/agent/admin/triggers/360033242313/index.html.md).
If you think that it should be assigned to someone else (e.g. session is scheduled for another engineer/index.html.md), feel free to re-assign it. Tickets without assignee will be automatically reopened by the trigger
[`Automatically reopen on-hold tickets without assignee`](https://gitlab.zendesk.com/agent/admin/triggers/360028981853/index.html.md). Tickets in on-hold status _with_ an assignee will be automatically reopened in 4 days by the automation [`Reopen on-hold tickets after 4 days`](https://gitlab.zendesk.com/agent/admin/automations/360028978393/index.html.md).

If a customer's reply is the last one in the ticket, do not set it to the On-hold status silently due to the same reasons as stated above in the
[Zendesk SLA settings and Breach Alerts](#zendesk-sla-settings-and-breach-alerts/index.html.md) section. 
Instead, reply to the ticket while also changing the status.