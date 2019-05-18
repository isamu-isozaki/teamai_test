---
layout: markdown_page
title: Confirmation Emails
category: GitLab.com
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

### Overview
This workflow covers cases when a user says they are not receiving their confirmation email.

### Check GitLab Admin
1. In GitLab Admin, [search for the user](https://gitlab.com/admin/users) by username or email address to confirm the account has been created. Alternatively, search using [the API in browser](https://gitlab.com/api/v4/users?search=email@email.test) if needed.
  * No account? Use the ZD macro under `Account` -> `Does not exist` or if you believe it's applicable, `Verify self-managed or .com`.
2. Check the email address against what the user has reported.
  + Did they make a typo when registering? See [Fix Email Address](#fix-email-address) below.
  + If not, [check Mailgun](#check-mailgun) as below.

#### Fix Email Address
If the user made a typo:
1. Make sure the account in question is a new account.
2. When viewing the user in the admin area, click `Edit`.
3. Fix the email address to the correct one and save your changes.

### Check Mailgun
On the first attempt, if our email system could not get through (usually server says it's non-existent or similar), then our mail server will put a supression on sending further emails.

1. Sign into Mailgun using the `supporteam` login in the Support team 1Password vault.
2. Go to [https://mailgun.com/app/logs/mg.gitlab.com](https://mailgun.com/app/logs/mg.gitlab.com).
3. Search the logs using the search on the right for the particular email address and see if email is being bounced or delayed.
    + If email is delayed, respond to the user and ask them to wait.
    + If email is bounced, remove the email from the suppressions list here: [https://mailgun.com/app/suppressions/mg.gitlab.com/bounces](https://mailgun.com/app/suppressions/mg.gitlab.com/bounces)

#### Removing a Bounced Email Address Block in Mailgun
2. In the list of views at the top, select `Suppressions`.
3. Ensure the left side drop down has `mg.gitlab.com` selected.
4. Search for the email address on the right side.
5. Select the relevant entry and delete it.

### Resend Confirmation Email
Once the problem has been fixed, you can [resend the confirmation email](https://gitlab.com/users/confirmation/new).

Let the user know you've sent a new confirmation email, and ask the user to check their inbox and spam folders.
