---
layout: markdown_page
title: License Troubleshooting
category: Support Workflows
---

## On This Page
{:.no_toc}

- TOC
{:toc}

----
## Overview
Refer to this page when a customer is having problems with licensing for self-managed or GitLab.com.

## GitLab Self Managed Subscriptions

When a customer reports problems when registering their license key, please check the points below in order to diagnose the problem:

1. How many active users are in the GitLab instance of the customer? Does their license key supports that number of active users?

    This is the main issue that we've noted when receiving requests related to problems with registering a license.

    You can ask the customer the following:

    > How many active users do you have? (You can find this on the admin dashboard at `http://<hostname>/admin/users` next to the "Active" tab/index.html.md)

1. If the customer reports the following validation error:

    > During the year before this license started, this GitLab installation had 0 active users, exceeding this license's limit of 5 by -5 users. Please upload a license for at least 0 users or contact sales at renewals@gitlab.com

    That usually means that that GitLab instance has more active users than the number allowed by the license key. Please ask the customer for the number of active users and suggest to buy more seats if required.

    That validation error [has been fixed](https://gitlab.com/gitlab-org/gitlab-ee/merge_requests/4961/index.html.md) but the fix will be included in the `10.7` version of GitLab.

1.  If the customer reports the following validation error:

    ![You have applied a True-up for 2 users but you need one for 3 users.](/imageshttps://github.com/isamu-isozaki/teamai_test/tree/master/support/support_license-troubleshooting.png/index.html.md)

    That usually means that the number of true-up purchased is invalid. If you consider that the customer has purchased an adequate true-up please follow these steps:

    1. Go to the [license app](https://license.gitlab.com/index.html.md/index.html.md)
    2. Find the last license key by email or company name
    3. Duplicate the license key
    4. Edit the `true up count` field with the correct number
    5. Save the license key

1. If you can't solve the problem with any of the above steps, please contact `@ruben`.

## GitLab.com Subscriptions

In order to purchase a GitLab.com subscription, we need the customer to have an account on [GitLab.com](https://gitlab.com/users/sign_in/index.html.md). Please ask the customer to create an account first, in case they don't have one yet.

If the customer can't see their Groups when purchasing a subscription, please let them know that they need to create a Group on [GitLab.com](https://gitlab.com/users/sign_in/index.html.md) first.

### Troubleshooting sales-assisted transactions for GitLab.com

After purchasing through Salesforce, an account is automatically created on customers.gitlab.com with the same email from Salesforce.

1. The customer should to go to https://customers.gitlab.com/customers/password/new and reset their account password
2. After they have logged in, ask them to access the "Subscriptions" menu
3. They'll be able to click onto "Edit" over a subscription
4. They'll be redirected to GitLab.com for OAuth login
5. At this point, they need to make sure they're logging using the account they want to license on GitLab.com
6. Ask them to select the Group they want to license then click "Update"

For other type of problems please contact `@ruben`.
