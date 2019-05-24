---
layout: markdown_page
title: "GitLab Proof of Concept"
---

# Proof of Concept (POC/index.html.md) Guidelines
{:toc}

GitLab wants prospects to enjoy a successful Proof of Concept with GitLab Enterprise Edition. A POC is a collaboration between GitLab and the prospective customer for evaluating GitLab Enterprise Edition.  

The target duration for a POC is 2 weeks, extended to a total duration of not more than 8 weeks for highly complex evaluations. A GitLab Customer Success collaborative project should be utilized as the default method to manage a POC, while a [document](#POCdoc/index.html.md) is available when using a GitLab.com project is not an option.

GitLab Solutions Architects should set a limit of 3 concurrent POC's as a best practice in order to provide excellent customer service and to enable a target of achieving 24 hour or less response times to inquiries during any POC. If more than 3 concurrent POC's are required, the SA should assess their ability to support the additional requirements and/or discuss viability with other SA's in their region.

## Tracking a Proof of Concept in Salesforce

### Salesforce Object

In order to track a POC correctly in Salesforce, the Strategic Account Leader should position the opportunity as Stage 3. The Solutions Architect will manually create a POC when the prospect or customer has indicated interest in moving forward with a guided POC. To track a POC, click the *Proof of Concepts* tab from the top menu bar in Salesforce. Create a new POC using the *New* button. Alternately, the Solutions Architect may select the relevant Opportunity, scroll down to the related list labeled *Proof of Concepts* and click on the "New Proof of Concept" button. This will automatically associate the POC with that Opportunity while all other fields need to be manually completed. 

Complete the following fields at minimum:  
  
  * **POC Owner** - this is the Strategic Account Leader
  * **Technical Account Manager** - this is the TAM who will be part of the POC
  * **Solutions Architect** - this is the SA who owns execution of the POC
  * **Proof of Concept Name** - this commonly is named identical to the opportunity name
  * **Account** - this is the company name
  * **Opportunity** - this is the associated opportunity name (this opportunity should be in stage 3/index.html.md)
  * **POC Start Date** - the date the POC is expected to begin
  * **POC Close Date** - the date the POC is expected to End
  * **POC Type** - this is style POC being executed

POC Types include:

  * **Paid** - prospect has paid GitLab for a high attention (dedicated Customer Success time/index.html.md) or extended time evaluation of the software (> 3 months/index.html.md)
  * **Guided** - the most common enterprise-level POC, which follows the flow detailed on this page
  * **Lite** - for smaller opportunities requiring minimal touch points throughout the POC
  * **On-site** - intense, condensed POC executed at the customer site within a tight evaluation window (< 2 weeks/index.html.md)

Once the POC begins, the Solutions Architech should change the **Status** field from *New* to *In Progress*. When the POC is complete, the Solutions Architect should change the **Status** to *Closed* and the **Result** should be identified as *Successful* or *Unsuccessful*.

# Proof of Concept Details

## POC Key Players

#### Customer  

*  Executive contact - Someone with business level, budgetary buy in
*  At least one pilot team to execute the POC
*  Technical POC lead

#### GitLab Role / Responsibilities

*  Strategic Account Leader (SAL/index.html.md) - Relationship manager, owns temporary license, POC kickoff, SFDC admin, scheduling
*  Solutions Architect (SA/index.html.md) - Primary technical contact, POC lead
*  Technical Account Manager (TAM/index.html.md) - Project management; Ensures all tasks in playbook are done on time; included in communication and calls for visibility
*  Professional Services - On-hand if needed, include for visibility only
*  Support - On-hand if needed

*Note: in the case of a "lite" POC, the Solutions Architect is expected to be the sole GitLab contact. "Lite" is determined case-by-case by the size of the prospect as well as their ability to engage with GitLab.*

## POC Meetings and Tasks

#### POC Kickoff Checklist

* Solutions Architect: Ensure the customer architecture is prepared to support an on-premises POC
* Solutions Architect: Ensure customer network has access to GitLab.com
* Solutions Architect: Customer Success project is created in GitLab as per the [handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/customer-success/tam/#to-start-a-new-customer-engagement/index.html.md)
* Solutions Architect: POC document is created if this is required by the customer, otherwise default to the Customer Success project
* Solutions Architect: Ensure POC goals and business outcomes are clearly identified prior to kickoff
* Solutions Architect: Notify GitLab Support of POC dates, customer, and other relevant information
* Strategic Account Leader: Opportunity updated in Salesforce, set to Stage 3-Technical Evaluation, with POC Information entered per the [handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/business-ops/#opportunity-stages/index.html.md)
* Strategic Account Leader: Signed NDA by the legal team if required
* Strategic Account Leader: Schedule Internal kick off meeting (detailed below/index.html.md)
* Strategic Account Leader: Schedule kickoff meeting with customer
* Technical Account Manager: Review collaborative project content prior to internal kickoff meeting

### Meeting Cadence

Calls may be recorded with customer consent, and recordings may be stored in the Recorded Meetings folder in the project repository for mutual benefit.  

#### Internal Kickoff Meeting - 1 - 1.5 hours, led by the Solutions Architect

##### Attendees

*  Strategic Account Leader
*  Solutions Architect
*  Technical Account Manager

##### Agenda

*  Collaboratively review customer success project README to ensure everything is correct
*  POC document review (only if a document is required for the POC/index.html.md)
*  Discussion of strategy, whether GitLab Support or Professional Services need to be notified/included in the POC
*  Strategic Account Leader to schedule external kickoff with customer

#### External Kickoff Meeting (Remote/index.html.md) - 1 hour, led by the Solutions Architect

##### Attendees

*  Strategic Account Leader
*  Solutions Architect
*  Technical Account Manager
*  Professional Services (if required/index.html.md)
*  Customer Executive contact
*  Customer Technical POC lead

##### Agenda

*  Screen share with the the customer to discuss the below agenda items
*  Collaboratively review customer success project README to ensure everything is correct
*  Agree on due dates for POC completion, add to project POC milestone
*  Review project POC issues - add new issues if necessary with agreed due dates
*  Review POC document with customer (only when required/index.html.md)
*  Establish cadence with customer, Strategic Account Leader to schedule DURING this call
*  Create issues for each cadence call with customer under the POC milestone for call notes
*  Provision licenses and establish if customer needs help getting GitLab set up and configured

#### Week One Retrospective call, led by the Solutions Architect

##### Attendees

*  Strategic Account Leader (visibility only/index.html.md)
*  Solutions Architect
*  Technical Account Manager (visibility only/index.html.md)
*  Professional Services (if required/index.html.md)
*  Customer's Technical POC Lead

##### Agenda

* What went well?
* What went wrong?
* What do we need to change?
* Review success criteria - are we on track?

#### POC Wrap Up Meeting - Led by the Strategic Account Leader

##### Attendees

*  Strategic Account Leader
*  Solutions Architect
*  Technical Account Manager
*  Professional Services (if required/index.html.md)
*  Support (if required/index.html.md)
*  Customer Executive contact
*  Customer Technical POC Lead

##### Agenda

* Did we meet the success criteria?
* Did we meet the goals for the customer? Is this a technical win?
* Next steps
* Send out POC survey feedback form

## POC Calendar

#### Week one

*  Work with customer to set up and configure GitLab if required
*  Intro to GitLab via demo covering areas specific to customer needs
*  Conduct cadence calls as agreed in kickoff meeting

#### Week two

* Week One Retrospective (Monday/index.html.md)
* End of POC cadence call (Friday/index.html.md)

## <a name="POCdoc"></a>POC Template Document

As an alternative (or in addition/index.html.md) to using a collaborative GitLab project, a document is available which helps outline the details of a POC. In the [document](https://docs.google.com/document/d/1anbNik_H_XDHJYyZPkfr4_6wvIXgqbwvWynN9v9tj2E/edit#/index.html.md) (only accessible to GitLab team members/index.html.md), provides the framework for a successful POC by addressing current state issues, persistent challenges, business problems, desired state and outcomes.  

This document suggests and verifies specific success criteria for any POC, as well as outlining a mutual commitment between GitLab and the identified prospect parties. It also specifies the limited timeframe in which the POC will occur.  

### Using the POC Template

The template provides a standardized approach to the POC process, but the document requires customization for each and every POC to be executed.  

To use the template, begin by making a copy of the master document for each POC.  

Edit each area highlighted in yellow within the document to include pertinent information for any particular prospect. This information includes basic data like the prospect name and GitLab team member details, as well as data to be collaboratively identified with the prospect, such as success criteria, trial location, and the client pilot team(s/index.html.md).  

After all the highlighted sections have been completely filled in, collaboratively complete the **Date** and **Owner** column fields within the **Project Plan** and **Roles and Responsibilities** sections.  

Finally, ensure both GitLab and the prospect have a copy of the document. Schedule all meetings associated to the POC via calendar invites prior to distributing the GitLab Enterprise Edition license for the POC.  
