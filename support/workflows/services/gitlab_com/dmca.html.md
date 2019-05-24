---
layout: markdown_page
title: DMCA Removal Requests
category: GitLab.com
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

# Overview
At times we would receive DMCA take down requests for users who host copyrighted content belonging to others. Below is a guide on how to handle incoming requests for GitLab.com. 

**DMCA complaints have a 24 hour Service Level Agreement.**

## Workflow

### First 24 hours

1. Legal reviews the request to validate that the content is still active and forwards the request to support. (If it is not a valid DMCA complaint, please refer to the Trademark or PII workflows./index.html.md)
1. Forward the notice to the user in a new ticket using the `DMCA::Notice to Content 'Owner'::First Touch` macro. Set the requestor email to the email address(es/index.html.md) belonging to the GitLab.com user and paste the content of the forwarded notice into the space provided.
1. In the original ticket from Legal, reply that you've forwarded the notice to the user and will be pending that ticket for 24 hours before the next follow-up using the macro `DMCA::Notice to Legal::First Touch`.

### Next 24 hours

1. Confirm whether the content is still live.
1. If the content is still live and the user has not responded, proceed to send a follow up notice to them using the `DMCA::Notice to Content 'Owner'::Second Touch` macro. Be sure to paste the content of the forwarded notice in the space provided.
1. In the original ticket from Legal, reply that you've sent a follow-up using the `DMCA::Notice to Legal::Second Touch` macro.

### Taking action

1. If the content still remains active and the user has not responded to the notice, pull up the projects in question and make them private, then block the user.
1. Send another follow-up to the user, this time informing them that action has been taken, using the macro `DMCA::Notice to Content 'Owner'::Final Touch (takedown/index.html.md)`.
1. In the original ticket from Legal, reply that you've sent a follow-up and taken action using the `DMCA::Notice to Legal::Final Touch` macro.

## User disputes a takedown notice

Should the user dispute the takedown request, follow the below steps:

1. The user should submit a valid counter-notice; tag Legal in the counter-notice response to vet.
1. If the counter-notice is determined to be valid, Legal forwards the counter-notice to the reporting party.
1. Make an internal note on the ticket to the user that the counter-notice has been forwarded and leave pending for a further 24 hours.