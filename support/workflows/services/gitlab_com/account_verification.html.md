---
layout: markdown_page
title: Account Ownership Verification
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

## Overview
While this workflow focuses on disabling [Two-factor Authentication](http://docs.gitlab.com/ee/profile/two_factor_authentication.html/index.html.md) on a GitLab.com account, this same workflow should be used any time ownership of an account needs to be verified.

2FA removal and other account actions can only be taken if the [workflow](https://about.gitlab.comhttps://github.com/isamu-isozaki/teamai_test/tree/master/support/workflows/services/support_workflows/2fa_removal.html#workflow/index.html.md) below is successful.

## Access by User Action
In many cases, users can regain access to their account using the following methods:

### User has recovery codes
Users can try and login using their saved [two-factor recovery codes](https://docs.gitlab.com/ee/user/profile/account/two_factor_authentication.html#recovery-codes/index.html.md).

### User has a valid SSH key:

If a user didn't save their recovery codes, new ones can be generated with the command below via SSH if they've previously added an SSH key to their account. The new recovery codes can then be used at sign in. This option is presented to users in the Zendesk macro. If they cannot use this method then move on to the manual methods below.

```
ssh git@gitlab.com 2fa_recovery_codes
```

If a user has added an SSH key to their account but receives a `Permission denied (publickey/index.html.md)` error when using the command above, they may need to manually register their private SSH key using `ssh-agent` if they're using a non-default SSH key pair file path. Direct the user to [this](https://docs.gitlab.com/ee/ssh/README.html#working-with-non-default-ssh-key-pair-paths/index.html.md) documentation on how to resolve this.

## Access with Support Intervention
If the user is unable to remove 2FA or otherwise regain access to their account using the above methods and responds with the need for further verification, then the user can provide evidence of account ownership.

If a user has lost their account recovery codes and has no SSH key registered, proving they
own the account can be difficult. In these cases, please use the [Risk Factor Worksheet](https://docs.google.com/spreadsheets/d/1NBH1xaZQSwdQdJSbqvwm1DInHeVD8_b2L08-V1QG1Qk/edit#gid=0/index.html.md) (internal only/index.html.md).

______________

**Note: as of Aug 2018 GitLab is no longer accepting government issued ID as proof of account ownership**

______________

### Workflow
As part of access recovery, if 2FA removal is not involved, then skip the following steps and move on to the next section.

1. Apply the **"Account::2FA Removal Verification - GitLab.com"** Macro
2. Mark the ticket as "Pending"
 
#### If the user responds with the need for further verification

1. Using the [Risk Factor Worksheet](https://docs.google.com/spreadsheets/d/1NBH1xaZQSwdQdJSbqvwm1DInHeVD8_b2L08-V1QG1Qk/edit#gid=0/index.html.md) (internal only/index.html.md), determine the appropriate data classification level and verification challenges that will be used.
   * By default, the originating email should be the same as the one listed on the account.

1. Leave an internal note on the ticket with the relevant admin link, your proposed data classification level, and verification challenges.

1. Request that your selections be peer-reviewed by another member of the team. If you’re reviewing the selections of another team member, ensure that you leave an internal note on the ticket that you approved them.

1. Once approved, respond and have the user go through the selected challenges then use the worksheet to assess the risk based on their responses.

#### User responds with repository verification

1. Verify the file uploaded
    + File contains the provided text string.
    + File has been uploaded to a "Personal Repository"
2. Apply an "Internal Comment" with a link to the commit (if not already included/index.html.md)

#### User Successfully Proves Account Ownership

1. If the user is able to pass all challenges:
   1. As an internal note, list the data classification and risk score.
   1. For disabling 2FA: log into your admin account and locate the username in the users table or by going to `https://gitlab.com/admin/users/usernamegoeshere`
      1. Under the account tab, disable 2FA.
      1. Use the **Account::2FA Removal Verification - GitLab.com - Successful** macro.
   1. For other situations, ensure the email on the account is the same as the requestor's email.
      1. Notify the user of any changes that have been made to the account
      1. If they do not know the password, let the user know they should use the [password reset](https://gitlab.com/users/password/new/index.html.md) option to regain access and then set up 2FA to secure their account.

#### User Fails to Prove Account Ownership

1. If the user is unable to pass the selected challenges:
   1. Inform them that without verification we will not be able take any action on the account. For 2FA, use the **Account::2FA Removal Verification - GitLab.com - Failed** macro.
   1. Mark the ticket as "Solved"



__________________

**Macros**

* [Account::2FA Removal Verification - GitLab.com](https://gitlab.zendesk.com/agent/admin/macros/103721068/index.html.md)
* [Account::2FA Removal Verification - GitLab.com - Failed](https://gitlab.zendesk.com/agent/admin/macros/103790308/index.html.md)
* [Account::2FA Removal Verification - GitLab.com - Successful](https://gitlab.zendesk.com/agent/admin/macros/103772548/index.html.md)

### GitLab Team Members

If the user is a GitLab employee, follow the below process:

1. Perform steps for SSH key and recovery codes, if possible.
2. Confirm authenticity of the request by contacting the employee via phone or video call.

