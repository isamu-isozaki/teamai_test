---
layout: markdown_page
title: Associating needs-org tickets with appropriate organization
category: Zendesk
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

## Associating tickets with the `needs-org` tag with appropriate organizations
Occassionally tickets come in without an associated organization, which means that no SLA is applied.

Potential reasons this might occur:
- we've never seen anyone from the organization in ZD before (i.e. this is an organization's first ticket)
- the user is using a generic domain name that we cannot assign to a ZD organization (e.g. `@gmail.com`)
- the company has more than one division with a support level, but only a single email domain
- the user is writing from a domain name that doesn't match what we have in ZD (e.g. they're using a personal email address for a work-related issue)
- the user or organization has a trial license

It could equally be the case that a ZD organization was manually created and the SLA type is out of date / incorrect.
Many of the same principles apply here.


> Please avoid manually creating organizations. 


### Determining if this workflow applies
This workflow applies if:
- ZD is prompting you to create an organization
- The Tag `needs-org` is applied (implied by above)
- You have reason to believe that this ticket belongs to a customer
- The domain TLD is *not* a generic domain (e.g. `gmail.com`)

![ZD prompts for an org to be created](/images/handbook/support/zendesk_needs_org-create.png)

#### Note on Trial License
While SFDC syncs organizations nightly to ZD, it does not include trial licenses. So organizations on a trial will not show in ZD, and this workflow _does not_ apply and ZD admins should _not_ manually create these organizations.

To check if a customer is on a trial: In SFDC (see instructions below), the `Initial Source` will likely say `Trial` and `Account Type` will say `Prospect` instead of `Customer`. 

This may display slightly differently if the organization was a `Former Customer`.

In the Customers portal, there is currently **nothing** to distinguish if a user or organization is on a trial except that there are no invoices or other evidence of billing.

### Finding the existing organization in ZenDesk
You may attempt to find the organization within ZenDesk using the search functionality. Do note that TLDs don't necessarily correspond to company names, so you may need to search in SFDC to find the appropriate organization.

Also note that users may be using generic mail providers you might not be familiar with, so the TLD on their email address may not correspond with their company at all. 

> When in doubt, check SFDC

![Selecting an organization in ZD](/images/handbook/support/zendesk_needs_org-finding-org.png)

### Finding the existing organization in SFDC
1. Log in to to SalesForce using the shared credentials in 1Password.
1. Enter a domain or full email address into the search bar at the top

![Search bar, in repose](/images/handbook/support/zendesk_needs_org-sfdc-search.png)

1. Look for results in the **Accounts** section. You should also be able to see if they have a support level if they have one.

![Account Name and Support Level in search results](/images/handbook/support/zendesk_needs_org-sfdc-accountname.png)

1. Click the **Account Name** to get a more detailed view in the **GitLab Subscription Information** section.

![Detailed view with support level](/images/handbook/support/zendesk_needs_org-sfdc-subscription.png)

#### Organization exists in SFDC but service level does not match ZenDesk
At times, the organization exists in ZenDesk, but has the wrong service level. You can force a resync for the specific organization.

1. Ensure that the **Account** in SFDC says the organization is a `Customer`.
1. `Edit` the `Support Level` to something aside from the current level.
1. `Save`.
1. `Edit` the Account again to change the `Support Level` back to the original.
1. `Save`.

If you refresh the organization page in ZenDesk, the proper service level should immediately be reflected. However, for existing tickets where the user was already associated with the organization, the appropriate tag will need to be added manually to the tickets.

### Finding the exisiting organization in [customers.gitlab.com](https://customers.gitlab.com)
1. Log in to [customers.gitlab.com](https://customers.gitlab.com) with the shared admin credentials in 1Password.
1. In the **Customers** section, search for a domain or full email address
1. You can *impersonate* an account to find out if they have a current subscription

### Adding the domain (ZenDesk Admins only)
> **Important**: Be extra careful here. If a large company has multiple subscriptions it may not be appropriate
to add the domain. You'll need to add individual customers to the appropriate organization (see below)

Once you've determined the appropriate domain to add and identified the correct ZD Organization, you can click 
the `Domains` field to add it.

![Filling in an organization domain in ZD](/images/handbook/support/zendesk_needs_org-adding-org.png)

### Adding a customer to an organization (All ZenDesk Users)
If you don't have admin access on ZD, you can still make sure the proper SLA is applied by adding the user to the appropriate
organization.

1. Click on the customers name in ZD
1. In the "Org" field type the organization name

![Adding a user to an existing organization](/images/handbook/support/zendesk_needs_org-add.png)

### Verifying that the ticket now has the proper SLA applied
Now that you've added the apporpiate domain, head back to your original ticket and verify that it is associated with
the appropriate organization and SLA.

![Verifying SLA](/images/handbook/support/zendesk_needs_org-verifying-sla.png)

### Associated Trigers:
- [Add need-org tag](https://gitlab.zendesk.com/agent/admin/triggers/360001567348)
- [Remove need-org tag](https://gitlab.zendesk.com/agent/admin/triggers/360017109414)
