---
layout: markdown_page
title: GDPR Article 15 Requests
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

## Overview

Use this workflow when a user is requesting information under GDPR Article 15. The request may look something like:

---
1. Please confirm to me whether or not my personal data is being processed. If it is, please provide me with the categories of personal data you have about me in your files and databases.

   a. In particular, please tell me what you know about me in your information systems, whether or not contained in databases, and including e-mail, documents on your networks, or voice or other media that you may store.

   b. Additionally, please advise me in which countries my personal data is stored, or accessible from. In case you make use of cloud services to store or process my data, please include the countries in which the servers are located where my data are or were stored.

   c. Please provide me with a copy of, or access to, my personal data that you have or are processing.


1. Please provide me with a detailed accounting of the specific uses that you have made, are making, or will be making of my personal data.

1. Please provide a list of all third parties with whom you have (or may have/index.html.md) shared my personal data.

1. If you are additionally collecting personal data about me from any source other than me, please provide me with all information about their source, as referred to in Article 14 of the GDPR.

1. If you are making automated decisions about me, including profiling, whether or not on the basis of Article 22 of the GDPR, please provide me with information concerning the basis for the logic in making such automated decisions, and the significance and consequences of such processing.

1. I would like to know whether or not my personal data has been disclosed inadvertently by your company in the past, or as a result of a security or privacy breach.


---


** These requests must be filled within 30 days. **

### Service Agent Workflow (ZenDesk/index.html.md)

1. Apply the **"Account::GDPR Article 15 - GitLab.com"** Macro

This macro will simply advise the user as follows and close the ticket:

```
Hi,

We understand that you want some information about the personal data GitLab has about you per Article 15 of the GDPR.

Due to the complexity of servicing these requests, we're asking our users to please email `gdpr-request@gitlab.com`.

Please ensure that you:
- send the email from the address associated with your GitLab.com account (if you have one/index.html.md)
- include the GitLab username if applicable

Once you've submitted your request, we'll have the various teams review our systems for your personal data and send you final confirmation after this process is complete.

Thanks for your understanding,

```
### Workflow for Requests submitted to: `gdpr-request@gitlab.com`

>Note: The following snippet is for reference **only**. Prefer the [issue template in the gdpr-request tracker](https://gitlab.com/gitlab-com/gdpr-request/blob/master/.gitlab/issue_templates/GDPR-Section-15-Request.md/index.html.md)


```
## Related issue: ___

1. [ ] Agent: Identify if the requestor has an account on GitLab.com
1. [ ] Agent: Verify that the `username` is associated with the originating email on GitLab.com
1. [ ] Agent: Create a new *confidential* issue in the `gdpr-request` using the GDPR-Section-15 template
   - [ ] Link the original issue in the **Related issue** field above
   - [ ] Respond to the original issue with a note indicating that it has been received.
1. [ ]  Agent: Check in SFDC for any records related to this email address
   - [ ] Agent: If they are listed as a prospect, contact the owner to see if they can give any context for how this user was put into SFDC
   - [ ] Agent: If they are listed a customer (or former customer/index.html.md), note that below.
   - [ ] Agent: If they have a billing address, company name or phone number note that below.
1. [ ]  Agent: Check to see if they have a user account in ZD, check the box below if they do.
1. [ ]  Agent: Check to see if they have an account on customers.gitlab.com, check the box below if they do.
   - [ ] See if they have a billing address or organization name listed and note it below.

1. [ ] JJ: Check in Marketo to see if they exist, check the box below if they do
1. [ ] JJ: Check in MailChimp to see if they exist, check the box below if they do

1. [ ] Services Agent: If all steps above have been completed, notify the user using the template in the GDPR Article 15 Workflow by commenting on the original issue and closing both this issue and the original. 


## Relationship with GitLab:
- [ ] GitLab.com User
- [ ] Newsletter subscriber
- [ ] Prospect
   - [ ] Did a trial of GitLab.com or Self-managed
   - [ ] Provided information in person at a marketing event
   - [ ] Other???

## Data we have
- [x] Name
- [x] Email
- [x] IP address
- [ ] Social identities (if provided on GitLab.com profile/index.html.md)
- [ ] Location (if provided on GitLab.com profile/index.html.md)
- [ ] Billing address
- [ ] Company / Organization Name
- [ ] Phone number

## Places where their data exists
- [ ] GitLab.com
- [ ] customers.gitlab.com
   - [ ] Zuora (if they have a subscription/index.html.md)
- [ ] SFDC
- [ ] ZD
- [ ] MailChimp
- [ ] Marketo
- [ ] Outreach

/label ~meta-issue

/assign @jjcordz me

/confidential

/due in 3 weeks

```

### Response template for incoming requests
```
Greetings,

We have received your Article 15 GDPR request. We're working on identifying any personally identifiable information on GitLab.com and associated systems.
You'll receive an additional notice once this process is complete.

Thanks for your understanding,
<Person who owns the request>

```
### Email template for successfully deleted accounts
```
Per your request under Article 15 of the GDPR please review the following:

1. Your personal data is being processed as a result of your having ______ (signed up for our newsletter || signed up for a GitLab.com account || attended a webinar/index.html.md). You provided to us the following personal data:
- Name
- Email
- IP address
- Social identities
- Location
- Billing Address
- Company / Organization Name
- Phone number

GitLab.com data may be stored in GCP, Azure or AWS clouds, all in US regions. All data on GitLab.com that is stored is accessible to you through https://gitlab.com/profile and https://gitlab.com/profile/active_sessions.

If you were a GitLab customer, you can access your customer data at https://customers.gitlab.com/customers/edit

2. We use your data to:
- verify account ownership in the event that credentials are lost or forgotten
- send email updates (if you have opted in/index.html.md)
- generate invoices and bill you (if you are a customer/index.html.md)

3. We have not shared your personal data with any 3rd parties. However, we do use 3rd party companies to process personal data as a part of normal company operations. As such, we have (or may have/index.html.md) used the following 3rd parties to process your personal data:
- ZenDesk (in the event you have created a support request, either by email or through the support portal at https://support.gitlab.com/index.html.md)
- Marketo (in the event that you requested to be on our email list, either by opting in at account signup or through our website https://about.gitlab.com/index.html.md)
- MailChimp (in the event that you requested to be on our email list, either by opting in at account signup or through our website https://about.gitlab.com/index.html.md)
- Zuora (in the event that you are a GitLab.com or GitLab Self-managed customer and provided billing information/index.html.md)
- Mailgun (we use this service to send outgoing emails from GitLab.com such as account confirmation emails, password resets and other notifications/index.html.md)
- Salesforce (in the event that you are a GitLab.com of GitLab Self-managed customer, or provided your personal information in a demonstration or trial/index.html.md)
- license.app (in the event that you are a GitLab.com of GitLab Self-managed customer, or provided your personal information in a demonstration or trial/index.html.md)
- Outreach (in the event that you are a GitLab.com of GitLab Self-managed customer, or provided your personal information in a demonstration or trial/index.html.md)
- Drift (in the event that you have ever reached out to us via webchat/index.html.md) 
- Cookiebot (in the event that you have accepted cookies from GitLab/index.html.md)

4. We have not collected any personal data about you from any source other than yourself.

5. We don't make any automated decisions about you based on your personal information.

6. As of the time of writing we have not positively identified any cases in which we inadvertently disclosed any of your personal data, whether by volition or as a result of a security or privacy breach.

If you have any additional queries, please contact gdpr-request@gitlab.com

Thank you,
<name>

```
---

**Macros**

* [Account::GDPR Article 15 - GitLab.com](https://gitlab.zendesk.com/agent/admin/macros/360027176693/index.html.md)

