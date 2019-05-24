---
layout: markdown_page
title: Support Channels
---

## On this page
{:.no_toc}

- TOC
{:toc}

----

Our [support engineers](/job-families/engineering/support-engineer/index.html.md) handle the channels listed below. They are sorted in order of priority (strictest SLA at top/index.html.md), and as a result, it is possible that channels that appear lower in this list experience longer delays in receiving responses. We are actively [hiring](/jobs/index.html.md/index.html.md) more Support Engineers to strengthen the team and provide support to the community.

## Emergency Tickets

When an emergency ticket comes in, it triggers a [PagerDuty](https://gitlab.pagerduty.com/index.html.md) incident. All Support Engineers must have the PagerDuty application installed on their phones once they are added to the on-call rotation schedule.

When a PD incident is triggered, the alarm will go off for the person on call. You should acknowledge the incident within 5 minutes, or the person on second level support will be alerted. The PD incident will have the link to the corresponding Zendesk issue from where you will continue the conversation with the customer.

Once acknowledged, you need to login to [Zendesk](https://gitlab.Zendesk.com/index.html.md), go to the corresponding ticket and let the customer know that you will handle their case. On this response you should ask for the best way to contact them. Usual channels are Phone, Skype, [WebEx](https://github.com/isamu-isozaki/teamai_test/tree/master/support/onboarding/#webex/index.html.md) or Hangouts. It is also a good idea to send them a meeting link where you are waiting, requesting that they join and to let you know if they will not be able to join.

Once the emergency has been resolved, return to the ticket in [Zendesk](https://gitlab.Zendesk.com/index.html.md) and document any steps taken to resolve the issue.

### Crisis Situations

If you are unable to help the customer and their instance is in a critical state (unavailable, uncertainty of data loss, etc./index.html.md), you should **escalate** the PD incident to second level support, and work through the issue together. It may also be necessary to ask for assistance from a developer in the appropriate slack channel. While you are waiting for help to join the call, focus on getting their server to a usable state.

If an emergency takes longer than an hour to resolve, and/or multiple people are or need to be involved, **start a google doc** that is open to the customer and the wider team at GitLab, and keep track of the issues and ideas there. Zendesk's 'linear' display of communication with a customer is not as effective in crisis situations, and the majority of developers do not have access to Zendesk in the first place. Announce the google doc in the appropriate slack channel (`#infrastructure`, `#development`, `#general`/index.html.md) so that individuals can contribute solutions and ideas. When the crisis has been resolved, be sure to transfer pertinent know-how from the google doc to relevant documentation, handbooks, and/or issue trackers, so that the google doc can be deprecated a.s.a.p.  In addition, Support Engineers and Developers involved in the crisis should make time to have a hangout for hand-off to make sure that everyone has the chance to recover and stay clear-headed.

## Security Disclosures

We have a [Responsible Disclosure Policy](/disclosure/index.html.md/index.html.md). Emails sent to security@gitlab.com go into Zendesk and receive an autoresponder that says:
`"Thank you for your responsible disclosure of a potential GitLab vulnerability. We'll follow up with you within one business day."`
We also accept reports via [HackerOne](https://hackerone.com/gitlab/index.html.md), see [more information](https://github.com/isamu-isozaki/teamai_test/tree/master/support/channels#hackerone/index.html.md) on this channel.

Please be very patient with these reports. Do not say 'there is no problem', you might be misunderstanding something that can lead to a 0 day disclosure. Give examples and keep asking questions until you understand the problem or until the researcher concludes there is no problem. If someone invested time to help us, offer to mention them on our [Security Researcher Acknowledgments page](/vulnerability-acknowledgements/index.html.md/index.html.md) even if there was no actual vulnerability. If you say that we'll get back to them **always** mention that they can email us at any time for an update. This is really important to prevent a 0 day disclosure resulting from us forgetting to respond.

If you need help from developers to diagnose the issue please open a confidential issue so we can work in private. Only if the security report is _about_ confidential issues, then use dev.gitlab.org instead. If someone opens a public issue please leave a message:
`"Thank you for helping to make GitLab more secure! We removed the contents of your vulnerability disclosure to keep it private. We opened an internal issue to look at your disclosure. Can you please use our [Responsible Disclosure Policy](/disclosure/index.html.md/index.html.md) to send us an email that references this url so we can communicate in private?"`

### PGP Process

The key used to encode/decode PGP messages is stored in our Support Vault on 1Password. We only provide our public PGP key upon request because it makes collaborating much harder and only a small percentage of all disclosures are serious enough to require that overhead.

See [PGP Process](https://github.com/isamu-isozaki/teamai_test/tree/master/support/pgp_process/index.html.md) for information about using the security PGP key pair and decrypting messages.

### HackerOne

We also use [HackerOne](https://hackerone.com/gitlab/index.html.md) to manage security reports. The HackerOne dashboard lists all reports for which you need to respond within one business day. These reports are also piped into ZenDesk, but they need to be responded to from the HackerOne dashboard and closed manually in ZenDesk upon completion of the initial response. Remember that all researchers should receive feedback as with regular support tickets, and you should not hesitate to triage or escalate the report.

The complete workflow for handling HackerOne reports can be found on the [Security page](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/security/#hackerone-reports/index.html.md).

If you need to grant HackerOne permissions to a new GitLab user, have an admin send an invitation from HackerOne and add you to the Internal group. You can find out who the admins are by asking on the #support channel.

## Regular Zendesk Tickets

You should always answer the tickets in a [FIFO](https://en.wikipedia.org/wiki/FIFO_(computing_and_electronics/index.html.md)/index.html.md) manner. Make sure that you answer the tickets that are assigned to you first and then move on to new tickets that have come in and are unassigned, again using FIFO. When you need others to help please create an issue on the relevant GitLab issue tracker.

## Follow up on Issues Posted on GitLab Issue Tracker

For ZenDesk issues you will have created issues on the relevant issue tracker.
Please refer to the priority as listed under [GitLab Workflow in the handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/communication/#gitlab-workflow/index.html.md).

## GitLab.com Support Tracker

For issues specific to GitLab.com that have nothing to do with availability we have the [Support Tracker](https://gitlab.com/gitlab-com/support-forum/issues/index.html.md). This forum must also be checked periodically for new issues and to report back if an issue has been solved. Ensure that you assign the issue to yourself to enable you to keep track of the issue and also to enable other support engineers to easily pick on unassigned tasks at a glance. Some people use this forum to report issues they are having with their self hosted installation. In that case, you should refer them to the [CE issue tracker](https://gitlab.com/gitlab-org/gitlab-ce/issues/index.html.md) or to our [Getting Help](/getting-help/index.html.md/index.html.md) page, depending on the issue they are having.

## GitLab CE/EE/Omnibus Issue Trackers

It is always encouraged to take a look at all our issue trackers and respond to bug reports or feature
requests:

- [GitLab EE](https://gitlab.com/gitlab-org/gitlab-ee/issues/index.html.md) some customers create issues here instead of emailing us. When a new issue is created here, a ticket is created in ZenDesk, so we always know when this is the case.
- [GitLab CE](https://gitlab.com/gitlab-org/gitlab-ce/issues/index.html.md)
- [Omnibus](https://gitlab.com/gitlab-org/omnibus-gitlab/issues/index.html.md)

See [the issue triage policies](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/issue-triage/index.html.md) for the above trackers for more information on how issues should be handled.

## TODO Docker

TODO Questions from Docker's [GitLab CE](https://hub.docker.com/r/gitlab/gitlab-ce/index.html.md/index.html.md) page flow into ZenDesk.

## Non Channel Work

If you have time for it please improve GitLab: fix bugs, add features, and polish the website. You can also consider hanging out on IRC to answer questions and help people (#gitlab on freenode.net/index.html.md).
