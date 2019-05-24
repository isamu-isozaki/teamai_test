---
layout: markdown_page
title: Dormant Username Policy
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

##### Overview
Dormant usernames can be re-assigned if both of the following are true:

1. The user's last sign in was at least two years ago.
1. The user is not an owner on any active projects.

If the account contains data, GitLab Support will attempt to contact the user over a two week period before reassigning the username. If the account contains no data the dormant username will be released immediately.

Usernames and namespaces associated with unconfirmed accounts over 90 days old may also be released immediately.


##### Notes:
When applying any of the Macros ensure to replace the placeholder **â€œREQUESTEDUSERNAMEâ€** with the username requested.
______________

##### Workflow

1. Search for the requested username in [GitLab.com admin](https://gitlab.com/admin/users/index.html.md), once found visit the users admin profile.
1. Apply the **â€œAccount::Dormant Username::Internal Checklistâ€** Macro
1. Answer all questions in the **â€œInternal Checklistâ€** (Yes/No/index.html.md) ensuring to cross check the information found in the admin section. 
1. If all answers are **Yes** for the internal checklist follow: [Username is available](#username-is-available/index.html.md) 
1. if the username is not available follow: [Username is not available](#username-is-not-available/index.html.md)

##### Username is available 

1. Reply to the requester with the **Account::Dormant Username::First Response** Macro
1. Create a **new ZenDesk ticket** with the **username owner's email address (found in admin/index.html.md)**. 
1. Apply the **â€œAccount::Dormant Username::Contact Username Ownerâ€** Macro and mark the ticket as **Pending**. 
1. Make an internal comment providing a link to the ticket â€œrequesting user's ticketâ€
1. Wait for **a response** or the ticket to be **automatically reopened** in a week.
1. Apply the **â€œAccount::Dormant Username::Contact Username Ownerâ€** Macro a second time and mark the ticket as **Pending**.
1. Wait for **a response** or the ticket to be **automatically reopened** in a week.


##### Username owner responded
If the username owners makes a response (donâ€™t remove my username/index.html.md) follow these steps:

1. Apply the **â€œAccount::Dormant Username::Cancel Requestâ€** Macro to the **username owners response**.
1. Apply the **â€œAccount::Dormant Username::Failed Username Requestâ€** to the **username requesters ticket**. 


##### Username owner has not responded

If the contacted user makes no response (within a 2 week period/index.html.md) the ticket will be **automatically marked as open and an email sent to the assigned agent** 

If the username owners makes no response follow these steps:

1. Rename the username:
1. Navigate to the username in admin - https://gitlab.com/admin/users
1. Select â€œEditâ€ on the user's profile
1. Append â€œ_idleâ€ to the userâ€™s username 
1. Save changes


1. Apply the **â€œAccount::Dormant Username::Successful Username Requestâ€** Macro to the **username requesters ticket** and mark the ticket as **Solved**. 
2. Mark the **username owners ticket** as **Solved**


##### Username is not available 

1. Apply **"Account::Dormant Username::Failed Username Request"** Macro and mark ticket as **Solved**


##### FAQs

1. Does a login in response to dormant request mean that the account is active? No, the user has to explicitly reply to the dormant request saying "I want to keep my username". If the user hasn't responded and has just logged in, send a final message saying something like, "I see you logged in at X, but you need to let us know here if you want to keep your username".
1. What constitutes data in the account? A group, a project, etc. means data. Even if the project or group is empty.


__________________

**Macros**

* [Account::Dormant Username::Failed Username Request](https://gitlab.zendesk.com/rules/94534768/edit/index.html.md)
* [Account::Dormant Username::Internal Checklist](https://gitlab.zendesk.com/rules/93505588/edit/index.html.md)
* [Account::Dormant Username::First Response](https://gitlab.zendesk.com/rules/94687707/index.html.md)
* [Account::Dormant Username::Contact Username Owner](https://gitlab.zendesk.com/rules/94531288/edit/index.html.md)
* [Account::Dormant Username::Cancel Request](https://gitlab.zendesk.com/rules/94534828/edit/index.html.md)

**Automations**

* [Dormant Username Check](https://gitlab.zendesk.com/rules/94693587/edit/index.html.md)
