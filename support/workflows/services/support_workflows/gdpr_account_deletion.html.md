---
layout: markdown_page
title: GDPR Driven Account Deletion
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

## Overview

Use this workflow when a user wants to delete their account but **not** accept the revised ToS related to the GDPR

## Notes: 
This workflow only applies if the user has **not** accepted the advised ToS. 
If they have accepted it, they have access to GitLab.com and can delete their account and retrieve their data themselves.


______________

### Service Agent Workflow (ZenDesk/index.html.md)

1. Apply the **"Account::GDPR Deletion - GitLab.com"** Macro

This macro will simply advise the user as follows and close the ticket:

```
Hi,

We understand that you want to completely remove your GitLab.com account.

Due to the complexity of servicing these requests, we're asking our users to please email `gdpr-request@gitlab.com`.

Please ensure that you:
- send the email from the address associated with your GitLab.com account
- include the GitLab username you'd like removed

Please note that:
- in many circumstances we will not be able to provide a full export of associated repositories
- any groups that you're a sole owner in will be deleted, along with any projects contained therein

Once you've submitted your request, we'll have the various teams remove your associated data and send you final confirmation when deletion is complete.

Please also note, that if you have accepted the updated ToS we will **not** take action on this request, and redirect you to:
https://gitlab.com/profile/account
From there, you can delete your account and associated data yourself.

Thanks for your understanding,

```
### Workflow for Requests submitted to: `gdpr-request@gitlab.com`

>Note: The following snippet is for reference **only**. Prefer the [issue template in the gdpr-request tracker](https://gitlab.com/gitlab-com/gdpr-request/blob/master/.gitlab/issue_templates/deletion-meta-issue.md/index.html.md)


```
## Related issue: ___

1. [ ] Services Agent: Impersonate the user to verify the user has **not** accepted the GDPR terms or `TermAgreement.find_by(user_id: User.find_by!(username:'<username>'/index.html.md)/index.html.md)`. (If they have accepted: stop and advise them how to delete their account themselves/index.html.md)
1. [ ] Services Agent: Verify that the `username` is associated with the originating email on GitLab.com
1. [ ] Services Agent: Create a new *confidential* issue in the `gdpr-request` issue tracker with the originating email address as the title. 
   - [ ] Copy the contents of this workflow into it.
   - [ ] Link the original issue in the **Related issue** field above
   - [ ] Respond to the original issue with a note indicating that it has been received.
1. [ ] Services Agent: Check in SFDC for any records related to this email address and have the account owner remove them. If there are none, remove ~SFDC-removal
   - [ ] Services Agent: Once you've contacted the account owner, add them as an assignee in this issue
   - [ ] Account owner: remove all records in SFDC pertaining to this account, when finished, remove the ~SFDC-removal tag
1. [ ] JJ: Ensure that this email address is removed from all mailing lists and deleted from the database completely. Remove the ~email-list-removal tag.
1. [ ] Services Agent: Tag a ZD admin to ensure that this email address (and associated tickets/index.html.md) are removed from ZenDesk
   - [ ] ZD Admin: delete all user data in ZD and remove ~ZD-removal
1. [ ] Services Agent: If the submitter has requested their data, discuss this with your manager before proceeding
     - [ ] Create an ~"SE Escalation" to initiate an export and wait for it to be completed before proceeding
1. [ ] Services Agent: Delete any groups that are blocking the deletion
1. [ ] Services Agent: Delete the user and remove the ~GitLab-removal tag
1. [ ] Services Agent: If all steps above have been completed, notify the user their request has been completed by commenting on the original issue and closing both this issue and the original. 

/label ~meta-issue
/label ~email-list-removal
/label ~SFDC-removal
/label ~ZD-removal
/label ~GitLab-removal
/assign @jjcordz
/assign me
```

### Response template for incoming requests
```
Greetings,

We have received your request for account deletion. We're working on removing any personally identifiable information on GitLab.com and associated systems.
You'll receive an additional notice once this process is complete.

Thanks for your understanding,
<Person who owns the request>

```
### Email template for successfully deleted accounts
```
Hi there,

As requested, your GitLab.com account has been deleted and all personally identifiable information related to your account had been removed.

Please do note that while your personal data has been removed from all production systems, it may persist in backup copies until they expire. GitLab.com backups expire every 2 weeks.

As allowed by the GDPR, we'll also maintain a copy of your original account deletion request sent to `gdpr-request@gitlab.com` and this message as a record of our compliance.

Regards,
<Person who owns the request>
```
__________________

**Macros**

* [Account::GDPR Deletion - GitLab.com](https://gitlab.zendesk.com/agent/admin/macros/360027176693/index.html.md)

