---
layout: markdown_page
title: "Business Operations - Tech Stack Details"
---

## On this page
{:.no_toc}

- TOC
{:toc}  

## Avalara
We use [Avalara](https://www1.avalara.com/us/en/index.html/index.html.md) to automate and manage all of our sales tax compliance obligations.

## Bizible
Bizible is our marketing attribution software that allows for connecting marketing and sales touch points over a prospect's or customer's lifecycle directly to revenue. It also allows up to directly tie the investment in our online advertising to records within our database.  Although Bizible has dashboards, we are not currently using the reporting to measure success or track marketing.  Bizible allows us to track our marketing activities at a more granular level within Salesforce, our single source of truth.

## By Appointment Only (BAO/index.html.md)
We are using By Appointment Only to help set meetings for Account Executives with leadership in target companies. This relationship is managed by SDR Lead - Jeffrey Broussard and tracked in a Salesforce campaign. 

## Carta
Stock option administration, capitalization table and equity management are all managed using the [Carta](https://carta.com/index.html.md/index.html.md) software platform.


## Clearbit  
Clearbit is a data enrichment tool that will be used to fill in important information for new leads created in Salesforce. This information could include address, phone number, industry, IT employees and other important values when assessing both the quality of the lead as well as routing. The technology uses proprietary logic to match prospects to companies in their extensive database.

## CloudExtend: Google Drive for NetSuite
[CloudExtend: Google Drive for NetSuite](https://www.celigo.com/products/netsuite-google-apps/index.html.md/index.html.md) is an integration application that connects the Finance team's G-Drive to NetSuite. A few benefits include streamlined Accounts Payable processing, centralization of document storage, and an improved audit trail.


## Cookiebot   
[Cookiebot](https://www.cookiebot.com/en/index.html.md/index.html.md) is a cookie and online tracking consent solution that complies with the consent and information requirements of the EU ePrivacy Directive 2009/136/EC and the General Data Protection Regulation (GDPR/index.html.md). Cookiebot is a self-serve cloud service provided to you by the ePrivacy company Cybot.

## DiscoverOrg  
DiscoverOrg provides our Sales Development Representatives and Account Executives with access to hundreds of thousands of prospects and their contact information, company information, tech stack, revenue, and other relevant data. Individual records or bulk exports can imported into Salesforce using extensive search criteria such as job function, title, industry, location, tech stack, employee count, and company revenue.  
![](sourcehttps://github.com/isamu-isozaki/teamai_test/tree/master/business-ops/tech-stack/DiscoverOrg-SFDC-homepage.png/index.html.md)


## DoGood

We are using [DoGood](http://www.mydogood.com/index.html.md/index.html.md) to help set meetings for account executives with leadership in target companies.

### Setting Meetings
We have notified DoGood of the individuals from their list that we would like to meet with. The outbound SDR team has supplied them with outreach email templates. DoGood will send emails to our desired contacts and see if they are interested.

### Accepting Meetings
If an individual expresses interest in meeting to learn more about GitLab, the SDR in charge of that account will create the contact in SFDC and ensure that the contact has the proper lead source and is attached to the appropriate account.

DoGood will have a short kickoff meeting with the account executive that will be taking the meeting, then make an introduction between the contact at the target company and the account executive.

### Tracking Meetings
The meeting and all further meetings with the contact will be tracked in SFDC as normal. After the completion of the meeting, we will report back to DoGood with one of three ratings:

1. Exceeded Expectations
2. Met Expectations
3. Did Not Meet Expectations


## Expensify
The company travel and expense management application. The platform provides employees a simple tool to create expense reports, which can then be managed from approval workflow through the final stage of reimbursement. 


## Google Analytics

[Google Analytics](https://www.google.com/analytics/index.html.md/index.html.md) captures all the analytics for GitLab pages outside of the actual app on https://gitlab.com. If you need access to Google Analytics, you can request access from the [Online Marketing Manager](/job-families/marketing/online-growth-manager/index.html.md/index.html.md) or [Marketing Operations Manager](/job-families/marketing/marketing-operations-manager/index.html.md/index.html.md).    


## Google Tag Manager

[Google Tag Manager](https://www.google.com/analytics/tag-manager/index.html.md/index.html.md) is used to manage the firing of the different JavaScript tags we deploy on our website. All marketing tags should be deployed through Google Tag Manager except in cases such as A/B testing software. If you need access to Google Tag Manager, you can request access from the [Online Marketing Manager](/job-families/marketing/online-growth-manager/index.html.md/index.html.md) or [Marketing Operations Manager](/job-families/marketing/marketing-operations-manager/index.html.md/index.html.md).


## LeanData  
When a lead is created in Salesforce, LeanData will be the tool that routes it to the appropriate user. Routing rules include sales segmentation, region, lead source, and owned accounts. For example, if a lead from a named account is created, it will be routed directly to the owner of the named account. Also, LeanData provide cross-object visibility between leads and accounts and contacts. When in an account record, a user can view "matched" leads by company name, email domain, and other criteria.

### What is LeanData?

LeanData enables strategic lead management within Salesforce so leads are assigned to the right reps. This is done by leveraging LeanData's fuzzy logic algorithms and lead-matching database. Whether we introduce a sales process based on named accounts, geographic territories, employee size (or all of the above/index.html.md), LeanData allows us to easily manage seemingly complex lead assignment rules.

### How It Works

LeanData is made up of three primary solutions: Lead/Account Matching, Lead Routing Rules, and Cross-Object Visibility.

#### Lead/Account Matching

The primary feature for LeanData is matching leads to accounts using a number of different criteria: company name, email address, and IP address. If a new lead is created in Salesforce, LeanData will review the criteria to determine if it matches an existing account in the system and will deliver the lead to the correct user as per our defined lead routing rules. Note that our matching criteria will include both the company information and region.   

#### Cross-Object Visibility

One of the most widely-known issues with the Salesforce architecture is the lack of relationship between the lead and account/contact objects. LeanData addresses this lack of functionality. A user can be in an account record and see all related lead records. Within the lead object, a user can view all related leads and accounts.

**LeanData from the Account Page**
 ![](sourcehttps://github.com/isamu-isozaki/teamai_test/tree/master/business-ops/tech-stack/leandata-contact.png/index.html.md)

* Merging a Duplicate Account
  * At this time, this feature is not supported. Please send a note via Chatter on the record you would like merged: "Please merge this account with `<URL of original account>`."

* Converting a Lead from the Account Page
  * Click on the "Convert" link for the lead you would like to add to the Account.
  * You can assign the contact to yourself or another user.
  * The account name will default to the account record you were just on. If you want to create a new account, select the "Create New Account" option.
  * "Do not create a new opportunity upon conversion" is defaulted to TRUE. If you want to create a new opportunity, uncheck this box.
  * Click the "Convert" button.

**LeanData from the Lead Page**
 ![](sourcehttps://github.com/isamu-isozaki/teamai_test/tree/master/business-ops/tech-stack/leandata-lead.png/index.html.md)

 * Merging a Duplicate Lead
  * Before you merge, please visit a Salesforce article regarding merging leads, ["Considerations for Merging Duplicate Leads"](https://help.salesforce.com/articleView?id=leads_merge_considerations.htm&type=0&language=en_US/index.html.md).
  * Click on the "Merge" link for the lead you would like to merge to the current Lead.
  * Select one lead as the â€œMaster Record.â€ The created date, created by, and read-only fields will retain information from the Master Record.
  * Select the fields that you want to retain from each record.
  * Click "Merge".
  * Click "OK".

 * Converting a Lead from the Lead Page
  * Click on the "Convert" link for the lead you would like to add to the Account.
  * You can assign the contact to yourself or another user.
  * The account name will default to the account record you were just on. If you want to create a new account, select the "Create New Account" option.
  * "Do not create a new opportunity upon conversion" is defaulted to TRUE. If you want to create a new opportunity, uncheck this box.
  * Click the "Convert" button.

## Looker
Looker is our primary analytics and visualization tool. Everyone in the company has view-only access to Looker. To request your account, make an issue in the [Looker project](https://gitlab.com/meltano/looker/index.html.md/index.html.md) using the "Looker Access" template.

## Marketo  
Marketo is our marketing automation platform managed by our Marketing Ops team. Anyone who signs up for a trial, requests contact from GitLab, attends a webinar or trade show, or engages in any other marketing activity, will end up in Marketo. These prospects will receive scores based on their level of engagement and these scores will be used by the Business Developement Representatives and Account Executives to prioritize which prospects to follow up with. Marketo is also our primary tool for delivering marketing communciation to prospects and customers.  


## Moz Pro  
[Moz Pro](https://moz.com/products/pro/index.html.md) is our all-in-one SEO tool set used by the Online Growth team for analysis of our website, effectiveness of keywords, optimization of landing pages and tracking our site rankings.  


## NetSuite
[NetSuite](http://www.netsuite.com/portal/home.shtml?noredirect=T/index.html.md) is the company Enterprise Resource Planning (ERP/index.html.md) system, which is primarily managed by the Finance team. The platform allows enhanced dimensional reporting as well as multi-currency and multi-entity reporting. This is where the General Ledger resides and all financial activity is ultimately recorded, which is critical to reporting the financial health of the company.


## Optimizely
[Optimizely](https://www.optimizely.com/index.html.md) is our A/B testing tool. We use it to improve user experience and increase conversion of key metrics such as sign-ups for GitLab.com and free trials requested.


## Outreach.io  
Outreach.io is a tool used to automate emails in the form of sequences. Users can track open rates, click through rates, response rates for various templates and update sequences based on these metrics. Outreach.io also helps to track sales activities such as calls. All calls that are made through Outreach.io Are automatically logged in Salesforce with a corresponding call disposition. See below for a list of current call dispositions, what they mean and scenarios on when to use each of them.

| Outreach.io Disposition | Meaning/Scenarios |
|---|---|
`Correct Contact: Answered`| The correct contact actully picked up the phone and you had a conversation with the contact|
|`Correct Contact: Left Message`| You were able to reach the voicemail for the correct contact and you left a message on their machine or with their Personal Assistant |
|`Correct Contact: Not Answered/Other`| You were able to reach the correct contact through a company directory but it kept ringing. You reached the contacts voicemail but their voicemail was not set up so you could not leave a message |
|`Busy`|Get a busy tone when calling|
|`Bad Number`|The phone number is not valid|
|`Incorrect Contact: Answered`| The wrong person answered the phone number that you had for this contact and it is the wrong persons phone number (They were not a personal assistant/index.html.md). They didn't take a message for the correct person or give helpful information|
|`Incorrect Contact: Left Message`|The wrong person answered the phone and it is the wrong persons phone number (They were not a personal assistant/index.html.md). They took a message for the correct person/gave you the correct number for the contact|
|`Incorrect Contact: Not Answered/Other`| You got through to the voicemail but the voicemail was for someone other than the person who you were trying to contact. Or the person was not listed in the company directory and you were calling the companies main number|

### External Resources
* [Outreach University](http://university.outreach.io/index.html.md/index.html.md)


## Salesforce   
Salesforce is our CRM of record. It integrates with all of the other applications in our business tech stack. Salesforce stores prospect, customer, and partner information. This includes contact information, products purchased, bookings, support tickets, and invoices, among other information.

### Standard Object Definitions

#### Lead   
A lead is a prospect who has yet to be qualified. Lead may have expressed interest by requesting contact, starting a trial, attending a webinar or trade show, or registering on GitLab.com or our customer portal. Leads are typically followed up by our Business Development Reps (BDR/index.html.md) or Account Executives. During this initial qualification process, a BDR will uncover certain details that will determine whether the prospect is qualified. For more information on the BDR Qualification process, [click here](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/marketing-sales-development/sdr/#qualifying/index.html.md). Once qualified, the lead is converted into an Account, Contact, and Opportunity. For all non-marketing and non-system adminstrators of Salesforce, all leads are read-only.

#### Account  
An account can either be a prospect who was qualified by a BDR or Account Executive, an existing customer, or a partner. Accounts will contain all company information, including billing and shipping address, company phone, website, support package, industry, employee count, and annual revenue. An account will be the parent record for associated contacts, opportunities, subscriptions, invoices, and payments.

#### Contact   
A contact is a person associated to an account record. Information contained in the contact record include name, mailing address, title, role, phone, and email. An account can have many contacts associated to it. Contacts can be added to opportunities via [Contact Roles](https://help.salesforce.com/articleView?id=000005632&type=1&language=en_US/index.html.md).

#### Opportunity   
An opportunity is created when a prospect has expressed interest in GitLab. The opportunity record includes information regarding close dates, contract value, and type. An opportunity will be in a certain stage, depending on where it is in the sales cycle. For more information on stages, [click here](https://github.com/isamu-isozaki/teamai_test/tree/master/sales/#opportunity-stages/index.html.md).

#### Tasks and Events   
Tasks and events are used when logging calls and meetings into Salesforce. Collectively called "activities", these records are meant to track interactions with customers and prospects. For example, you might create a task after you've attempted to call a prospect. You may also want to create a task as a reminder to complete a certain task, such as call a prospect or send an email. Tasks can also be created by external systems such as Marketo or Outreach when emails are sent to leads or contacts. External resources: [Difference Between a Task and an Event](https://success.salesforce.com/answers?id=90630000000gvEbAAI/index.html.md), [SFDC Task Documentation](https://help.salesforce.com/articleView?id=activities.htm&r=https%3A%2F%2Fwww.google.com.ph%2F&type=0/index.html.md)

### External Resources
* [Salesforce Success Community](https://success.salesforce.com/index.html.md/index.html.md)
* [Salesforce Help](https://help.salesforce.com/home/index.html.md)
* [Salesforce Glossary](https://help.salesforce.com/articleView?id=glossary.htm&type=0/index.html.md)


#### Commonly Asked Questions
* [How to Create a Report](https://help.salesforce.com/articleView?id=reports_builder_create.htm&type=0/index.html.md)
* [How to Create a List View](https://help.salesforce.com/articleView?id=customviews.htm&type=0&language=en_US&release=208.6/index.html.md)   

## OwnBackup
[OwnBackup](https://www.ownbackup.com/index.html.md/index.html.md) is a SalesForce backup tool. We use it to take backups of both data and metadata nightly for the production instance of Salesforce. 

### Backup Strategy
* We do a full backup of data once per week and incremental backups (stored as Synthetic Full backups/index.html.md) every 24 hours. 
* We do full backups of all metadata (Object definitions, Apex Classes, Templates, Layouts, Permissions, etc./index.html.md) every 24 hours. 
* Partial restores to a Sandbox will be done by the Business Operations team once per quarter to ensure our ability to restore to a workable state following a disaster. 

## Screaming Frog
[Screaming Frog](https://www.screamingfrog.co.uk/seo-spider/index.html.md/index.html.md) is a desktop web crawler we use to identify, track, and address crawl issues on our website.

## Sertifi  
Sertifi is used when a quote or other document requiring signature needs to be delivered to a prospect.


## Snowflake
[Snowflake](https://gitlab.snowflakecomputing.com/index.html.md) is our primary data warehouse. It is the single source of truth for all company data and powers Looker.


## Stripe
[Stripe](https://stripe.com/index.html.md/index.html.md) is a software application that enables GitLab customers to make online payments. Finance uses this system to collect information pertaining to payments made online.


## Terminus
[Terminus](https://terminus.com/index.html.md) is an account-based marketing tool. It allows us to show display ads to employees in target accounts. Terminus is integrated with Salesforce to allow us to select dynamically which accounts we would like to target. Standard IAB ad sizes are used.


## Unbounce
[Unbounce](http://unbounce.com/index.html.md/index.html.md) is for the creation of landing pages. The login information is in the marketing vault of 1Password. Currently, we use Unbounce to manage and create pages for our PPC traffic, webcasts, live/VIP events and any gated content (whitepapers, cheat sheets, etc./index.html.md).  

Before any Unbounce landing pages are published, final approval needs to be given by the design team to ensure sure the page meets our brand standards.  


## Xactly
Tracking and payment of variable compensation including sales commissions payment.


##  Zendesk   
Customer support tickets are managed through Zendesk and can be visible in the Lead, Account, or Opportunity object in Salesforce in the form of a Visualforce page. This provides visibility for non-Zendesk users into the support tickets created by their prospects and customers. For more information on this tool, you can visit the Support page [here](https://github.com/isamu-isozaki/teamai_test/tree/master/support/index.html.md).


## Zuora   
Zuora is our subscription management and billing system, primarily managed by our Finance team. A quote object within Salesforce is created with a specific configuration, and an order form (PDF/index.html.md) is be generated. Once the order form is signed, the Quote in Salesforce is converted to a Subscription in Zuora and the invoice is delivered or payment is applied if the customer provides their credit card details.
