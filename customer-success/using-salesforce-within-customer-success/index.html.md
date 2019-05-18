---
layout: markdown_page
title: "Using Salesforce within Customer Success"
---

# Using Salesforce within Customer Success
{:.no_toc}

## Customer Success Section
{:toc}

On an account view in Salesforce, there is a Customer Success section, with the following fields:

* Health Score - A field to record the overall customer health (details TBD on this)
* GitLab Customer Success Project - Where you enter the URL of the project created using the template described above
* Customer Slack Channel - A field to record Slack channel(s) used for internal and external customer collaboration. If a channel is internal, make sure it follows the naming convention"#organisation-name-internal"
* Solutions Architect - The Solutions Architect aligned with the acccount
* Technical Account Manager	- The Technical Account Manager aligned with the acccount

## Salesforce Objects

Salesforce operates using a series of objects. Standard objects are objects that are included with Salesforce. Common business objects like Account, Contact, Lead, and Opportunity are all standard objects.

Custom objects are objects that you create to store information that’s specific to your company or industry. For GitLab, we have created four custom objects that are specific to Customer Success. These are POC's, SOW's, EBR's and Onboarding objects. We can link these custom objects to accounts and opportunities, and create automations such as allowing us to auto-populate specific fields and notify users when a task is in need of completion.

### Onboarding objects

The Onboarding object is a way for the Customer Success team to track and manage the customer onboarding experience. 

* When a New Business opportunity is set to 'closed-won' a new onboarding object is created. 
* The purchase date field is auto-populated with the close date from the opportunity.
* The object and opportunity will be automatically associated with one another.

##### Fields:

* Purchase date (date field, automatically populated, editable)
* Onboarding start date (date field, manually populated, editable)
* Onboarding finish date (date field, manually populated, editable)
* Onboarding status (picklist) - Not started (default), Scheduled, In Progress, Completed 
* Days of onboarding count (like the POC object, not hidden)
* Gemstone type (automatically populated, but editable picklist) - Diamond, Pearl, Sapphire, Ruby, Quartz
* General onboarding notes (text field)

#### Compulsory fields after status is set to Completed

* Onboarding experience survey sent? y/N checkbox
* Onboarding experience survey results received? y/N checkbox
* Onboarding experience score (picklist of 1-5) (decided by TAM if no survey results received)
* Onboarding takeaways - how could we have done better? (text field)

#### Gemstone Automations

```
if >5000 users   
OR Ultimate AND >2000 users 
OR >500k iACV
= diamond

else if >2500 users
OR Ultimate AND >1000 users
OR >250k iACV
= pearl

else if >1000 users
OR >100k in iACV
= sapphire

else if >500 users
OR >50k in iACV
= ruby

else
= quartz
```

PLease visit [this page](https://about.gitlab.com/handbook/customer-success/tam/#customer-onboarding) for more information on Gemstones.

### Executive Business Review (EBR) objects

EBR objects allow the Technical Account Managers to track and measure the success of Executive Business Reviews held (or not held) with customers each year.

In order to appropriately track and create Executive Business Review Objects please follow the instructions below:

#### Creating the first EBR for an account

* If it is the first EBR for an account you can navigate to the EBR Tab. This can be located on the either the 'Sales' or the 'Service' App within Salesforce
* On the top of the list shown, you click on the 'New' button. This will enable you to create the new EBR object where you can provide the following. `Executive Business Review Name` is the name that you give this EBR. Select the `EBR Date` that the EBR is scheduled to occur on. 

Note: If the EBR Date changes, please see below for handling this situation in order relate the EBR to the appropriate account. This is done using the search functionality provided by the `Account` field. `EBR Status` should be set to either 'Not Started' or 'Scheduled' depending on the current state of the EBR. All other fields should be left alone. Please refer to the section below on if you should link the EBR to any Opportunities.  

#### Creating any successive EBR's and handling "Declined" or "Cancelled" EBR's

* In order to create any successive EBR's (anything besides the first EBR), DO NOT us the the 'New' button as this will cause errors with tracking. Instead, after the completion, cancellation or declined invite of an EBR, update the `EBR Success` to the appropriate value. This will automatically create the next EBR for the account 90 days after the `EBR Date` for the current EBR (ensuring that there is one EBR per quarter). 

A number of fields will also auto populate making the creation process of new EBR's much more efficient.

#### Tracking the performance of EBR's

* There are currently two picklist fields in order to provide tracking for EBR's:
    * `EBR Status` - This field shows the scheduling status of the EBR. This should be used to help monitor workflow (Scheduled vs Not Started) and also to track cancellations and declined EBR's as well as completed EBR's that were actually held.
    * `EBR Success` - This field tracks the overall success of the EBR with the default set to `Incomplete`. This field should only be updated once the EBR is held OR after a cancellation or declined EBR. This tracks what the  Technical Account Manager believes was the outcome of the EBR (or if it was declined or Cancelled).
* `Declined` vs `Cancelled` - The main differnce between a Declined EBR and a Cancelled EBR is dependant on how it is handled. 

For example, if a customer pushes to only have two EBR's a year, then two of the EBR's each year should be labeled as Declined. If an EBR is successfully scheduled but then for whatever reason the customer or GitLab has to cancel the EBR, then this value should be chosen.

Handling EBR Date Changes:
* If the `EBR Date` is changed and is still planned to occur within the same fiscal quarter that it was originally planned to take place, simply update the `EBR Date` field to the new scheduled date.
* If the `EBR Date` is changed to a date that is in the next fiscal quarter please treat it as if that EBR was declined. Update the `EBR Status` and the `EBR Success` field to `Declined` and save the EBR. Please review the section above on creating successive EBR's for an account.  

#### Linking EBR's to Opportunities: 
* Although all EBR's can be associated to an Opportunity, not all EBR's necessarily need to be associated to an opportunity. Only the four latest EBR's should be related to an upcoming opportunity. 

For example, If there is an upcoming opportunity in Q4 2019 then the only EBR's that should be related to this Opportunity should be the following EBR's, Q1-2019-EBR, Q2-2019-EBR, Q3-2019-EBR & Q4-2019-EBR (Assuming that the Q4 EBR took place before the opportunity close date).

* To link an Opportunity to and EBR use the "New EBR-Opportunity Associations" Button that is located above the "EBR-Opportunity Associations" related list. This is done on either the Opportunity you would like to associate the EBR with, or the EBR that you want to associate with the Opportunity. 

Scroll down to find the "EBR-Opportunity Associations" related list on the layout and click on "New EBR-Opportunity Associations" Button. From there, search and select the appropriate Opportunity and EBR that need to be associated with one another and save the record. 

### Statement of Work (SOW) objects

SOW objects in Salesforce are used to track the progress of our SOW's that are agreed upon with our customers. These SOW's describe the professional services that Gitlab will deliver to our client. As this is related to a billable service that we are extending to our clients all SOW's must be related to an appropriate Opportunity and an Account. 

The Opportunity that each SOW is associated with will contain information relevant to the Opportunity (Amount, IACV etc.) while the SOW itself will house notes, details and monitor the progress of the SOW (Go Live Date, Kick Off Date etc.). If a client would like to move forward with many professional services at once then all of these services would be encapsulated and related through one Opportunity and one SOW. 

If an existing client, who previously purchased professional services from Gitlab, would like to purchase addition professional services than a new Opportunity and SOW would be created in Salesforce. Review our section in the [handbook](/handbook/sales/#when-to-create-an-opportunity) about creating new opportunities if you have any questions around the Opportunity creation process.  

In order to track the contacts that are associated with a SOW, we utilize the SOW-Contact Association list. This can be accessed by navigating to the SOW page layout and locating the SOW-Contact Association related list. From there you can create a new association by looking up the contact that is associated with this SOW. Multiple contacts can be associated with a single SOW. 

### Proof of Concept (POC) objects

Please visit [this page](https://about.gitlab.com/handbook/sales/POC/) for POC documentation.

## Salesforce - Customer Success Automations

### New Zendesk Ticket Notifications

For all new Zendesk tickets that are created, the Technical Account Manager and Account Owner for the account that the ticket is associated with will receive an email notification alerting them of a new ticket. This currently is a one time notification that only occurs when the Zendesk ticket is first created in Salesforce. 
