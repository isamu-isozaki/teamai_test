---
layout: markdown_page
title: "Customer Reference Program"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Customer Reference Program

The goal of our Customer Reference Program is to provide opportunities for customers to share their story on how GitLab has helped them overcome the challenges, blockers and pain points within their organizations.


The goals of the Gitlab Customer Reference Program include:
- **Credibility** -Reinforce our credibility as an end-to-end DevOps solution partner.
- **Shorten the sales cycle** - Having our advocates involved with sharing their story with potential sales, analysts and the marketplace can help potential sales close sooner
- **Increase Revenue** - A successful Customer Reference Program helps increase revenue by attracting new clients and increasing retention rates.
- **Customer Advocacy** - Encourage our customers to share their success stories with others who are learning about or evaluating GitLab.

### Customer Reference Types
Some examples of the types of assets we'd use as customer references once we have approval from the customer:
* Logo (The ability to name a company as a customer and use their logo in our marketing materials)
* Live sales reference (both calls and possible in-person)
* Website content
  * Case studies
  * Blog posts
  * Videos
  * Podcasts
  * Usage quotes
* Event speakers (At industry, third-party and company events)
* References for analysts and press
* Quotes (can be attributable with approval or anonymous)
* Anecdotes (short "snackable" stories, can be attributable with approval or anonymous) Read [GitLab's customer anecdotes](#customer-anecdotes).

### Customer Case Studies
The most recent customer case studies are found on the [GitLab customer's page.](https://about.gitlab.com/customers/)
When we build case studies, we need to have quantifiable metrics and business value to help describe how GitLab helped a customer achieve a signficant business result.  Below are a sample of KPIs / dimensions we need to find in a good case study.

**Faster**
* Improved cycle time - the time it takes for an idea to reach production.
* More frequent deploys -  related to cycle time, but easier to measure

**Savings**
* Reduced IT spend - We reduced budget by x.   Or we saved $ with GitLab
* Improved efficiency - We shipped more features in the same time…

**Business Value**
* Increased revenue

**Better / Quality**
* Reduced defects / errors
* Reduced security issues/vulnerability
* Decrease of customer support calls

If a proposed customer case study doesn't have at least one metric to include, then we consider working with the account team to help identify a solid metric before building the case study.

#### Publishing to the website

1.	Start by creating a `.yml` file in `/data/case_studies` directory under Marketing site repo (www-gitlab-com project).
2.	Keep the name of file same as company name (this is not mandatory but it is easier to manage), for eg; if company name is "Foobar", create a file as `/data/case_studies/foobar.yml`.
3.	Once created, add contents of the file using this sample Case Study template, and then update the values of each property based on case study details, remember, do NOT change property names.
4.	Once this file is added, you'll need to restart marketing site server by first closing it using Ctrl+C and then running bundle exec middleman again.
5.	When the server is started, you can view generated Case Study page in your local instance of marketing site under the URL, for eg; http://localhost:4567/customers/foobar.
6.	Please note that you don't need to restart server again if you make any changes to foobar.yml file, this is required only when a new file is added to the `/data/case_studies` directory.

### Customer references collection

Today, we don't have a central collection for customer service, but we are starting to build one. For now we are capturing customer stories in an issue. If you have a customer story or anecdote [leave a comment on issue 1834](https://gitlab.com/gitlab-com/marketing/general/issues/1834).

To initiate a formal case study process, follow the process listed [here](https://about.gitlab.com/handbook/marketing/marketing-sales-development/content/case-studies/)

### Reference Program Process
1. Adding a new reference customer
    1. AE nominates customer for the program to Customer Reference Manager
    2. CRM - AE briefing <br>
Key info needed:
		- Industry / Vertical
		- Region/Geo
    - Tier (core, starter, premium, ultimate)
    - [GitLab Use Case] (https://about.gitlab.com/handbook/use-cases/)
    - Customer Segment (strategic, large, smb)
    - Deployment size (licenses)
    - Customer Story (why GitLab, key metrics, etc)
    - Who did we beat?<br>
 	 3. AE Introduces CRM to customer
		- Describe the Customer Reference program
    - Describe the types of reference activities and gauge their interest
		- Gauge their interest participation level
     4. Update Customer Reference Spreadsheet (and record in SFDC) with details from interview to make sure the customer is identified as a potential reference and their desired activity level. 

### Sample Interview Questions/topics
    * What led you to GitLab, what problems were you trying to solve?
    * Why did you choose GitLab and what other tools were you using or considering?
    * What has been your experience with GitLab?  
    * How did you make the business case for GitLab and what metrics have you seen improve?
    * What have you heard from the GitLab users, what was the adoption curve like?
    * What has been the most unexpected success you have experienced? Adoption rates? Improved speed? 
    

### GitLab DevOps Customer Advisory Board
**Purpose:** To help foster DevOps transformation and adoption we are establishing a Customer Advisory Board, where we focus on sharing DevOps best practices and lessons learned with each other. We believe that transparency and sharing  is a key way to help encourage the success of DevOps transformations.  The GitLab customer advisory board is intended to be home to learning and collaboration so we can all experience success through DevOps transformation.

**Members** Executives/Champions for DevOps within their organizations

**Frequency:**  We will try to meet virtually every 6 to 8 weeks

**Membership:** Approximately 15 - 20 customers, GitLab

**Meeting Recordings** Meetings are recorded for internal and member use

**Meeting Schedule**

***Kickoff Meeting-September 5, 2018***
- Member introductions-9 members in attendance
- Group goals  
- Top DevOps challenges

***GitLab Road Map review-September 26, 2018***
- Member introductions- 7 members in attendance
- Road Map review
- Within Depth, what is holding you back the most from adopting existing features/capabilities?
- Within Breadth, what are you most excited about?
- Within Roles, what are you most excited about?

***GitLab Create review-October 17, 2018***
- Member introductions
- Customer Sharing
- Review of Create

***GitLab CI/CD review-November 7, 2018***
- Member introductions
- Customer Sharing
- Review of CI/CD

### GitLab Special Interest Group

***Purpose:*** We are forming Special Interest Groups to foster specific and focused discussions about how to apply DevOps practices and GitLab capabilities in specific domains such as planning, development,  CI/CD, security, etc. These Special Interest Groups will encourage sharing and collaboration of DevOps best practices and lessons learned between users and GitLab.

We believe that transparency and sharing is a key way to help us all learn and improve how we deliver for our customers. GitLab special interest groups are intended to be home to learning and collaboration.

***Members*** Technical utilizers and advocates of GitLab

***Frequency:***  We will try to meet virtually every 6 to 8 weeks

***Membership:*** Approximately 8-15 users, GitLab Product Manager





### Customer Anecdotes
Customer anecdotes are short, "snackable" customer stories. These can be used on a call or in a meeting to share a point about GitLab by validating it with the customer story. An anecdote can be a summary of a formal, attributable case study or just an anonymous story from a conversation you had with a customer. It's important to keep customers anonymous unless we have explicit approval to use their name.

**Remove the complexity of multi-tool environments**

A communications company recently shared how they built their technology stack. "GitLab checks so many boxes for us that we don't need other tools." The company then explained they they are operating with a team of 2 people because GitLab makes the environment so simple. They said another organization would probably have to employ 15 people to accomplish what they can. 

**Administrative overhead**

We hosted a dinner for customers and prospects to mingle with each other and share stories. When the topic of managing the DevOps toolchain came up, the Head of Risk at a large US bank mentioned that she had a team of 20 to keep SDLC tools running in her org. A GitLab customer, the managing director of a product group for a global investment management corporation said, "this is going to break your heart, but I have 1 guy that spends 25% time to keep GitLab up and going for my team of 1500 devs."

**Deliver value faster** 

Pinterest is not a GitLab customer, but uses Kubernetes together with Jenkins. Because there's no [native kubernetes integration](/kubernetes) for Jenkins they needed to dedicate a [team of 4 spending 6 months](https://kubernetes.io/case-studies/pinterest/) to build a custom system to control access managment and allow teams to to self-serve builds. This is functionality that comes out of the box on day one with GitLab. 

**Adoption at an incredible pace**

A large enterprise in the software space is a recent GitLab Premium customer wanting to replace Perforce. They predicted that it would take them 3 years to hit 6K active users. But, the developer experience was so superior that they ended up hitting 6K active users in only 8 months.

**Security is at the center**

A publishing firm is utilizing GitLab best of breed CI/CD functionality and with upcoming product advancements they have informed us that GitLab is a mission critical application for them. They also chose GitLab over the competition because security is currently the biggest aspect they want to improve on internally.

**Removing the wait**

A financial services company recently stated that their teams went from two week releases to six times per day using GitLab. They are able to release this quickly because they do not need to wait for infrastructure.

**No babysitter required**

An online gaming development house has a team of 9 looking after its toolstack for SDLC. GitLab is one of the tools in the stack, but is self-sufficient enough that they only deal with it every six months.

**Providing happiness everyday**

A large media company recently stated that GitLab is the best architected application they have ever used. According to this company, "This product is a joy to use. We cannot believe how much incremental value you crank out with each release."



### Customer Case Studies

#### [Ticketmaster - 15x faster build time](https://about.gitlab.com/2017/06/07/continous-integration-ticketmaster/)
Ticketmaster is a global event ticketing leader with one of the world's top five e-commerce sites, getting almost 27 million monthly unique visitors. Ticketmaster was using Jenkins for continuous integration. Weighed down by plug-ins and legacy development, their pipeline was taking 2 hours to complete. After getting stuck late on a friday night waiting for the build to complete, their ops team began exploring other options. They were able to run their pipeline on GitLab CI/CD in 8 minutes for a 15x increase.

#### [Axway - 26x faster release cycles](https://about.gitlab.com/customers/axway/)
Axway, is a global enterprise software company with over €300 million in yearly revenue. Axway wanted to adopt DevOps practices but their legacy Subversion toolchain was blocking them. By moving from Subversion to Git using GitLab as their Source Code Management (SCM) solution they were able to implement DevOps integrating GitLab into tools like JIRA, for issue management and Jenkins for continuous integration. They increased demployents from once-a-year to every two weeks.

#### [Paessler - 120X increased QA efficiency](https://about.gitlab.com/customers/paessler/)
Paessler AG provides the award-winning PRTG Network Monitoring software used by over 150,000 IT administrators in more than 170 countries. QA engineers were manually testing software with a routine set of tasking taking an hour to complete. By implementing GitLab pipelines they were able to automate QA tasks requiring only 3 minutes of effort for a 120x efficiency increase.

#### [Equinix - increased DevOps agility](https://about.gitlab.com/customers/equinix/)
Equinix is a leading global data center company. Their client-side development teams are responsible for building software products and business critical applications,  increase development speed, self-serviceability, and ship fixes and features quickly. Equinix needed a version control and continuous integration tool for distributed workflows to support globally distributed development teams.

#### [Other customer case studies](https://about.gitlab.com/customers/)


