---
layout: markdown_page
title: "Online Growth"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Online Growth
The Online Growth team attracts new visitors through organic and paid channels, tests incremental changes for conversion rate improvement, and tracks campaign performance.

## Requesting Marketing Campaigns

If you would like to request a paid marketing campaign to support your event, content marketing, or webcast, create an issue in the Online Growth repo and use the `marketing-cmp-template` template. 

## Requesting LinkedIn Inmail as part of campaign

LinkedIn Inmail campaigns are a good way to reach people at specific companies, industries, and more. They work best for inviting people to events and webinars if you do not have specific people in mind (unlike a Marketo campaign/index.html.md). If you would like to request an Inmail campaign as part of your markeing campaign, create an issue in the Online Growth repo and use the `linked-inmail` template.

## Create a Culture of Testing and Optimization
In order to iteratively improve the site, we should test all major site changes before implementions.  Testing requires a control and a variant within the same time period, while holding all other variables constant.  Using a/b testing tools will allow us to create tests that follow testing best practices and gather data about what works or does not work to encourage people to spend time on our site or have a conversion event. With testing, we can makes informed decisions about what works for our audience and helps them reach their goals, and what works for us to help use meet our business goals.

- Build a test: If you would like to request an a/b or multivariate test, create an issue in the [Online Growth Repo](https://gitlab.com/gitlab-com/marketing/online-growth/issues/index.html.md) and use the `ab-test` template. Assign the issue to `@lbanks`.
- CRO process and MVCs: Not all changes to pages need to be tested, only pages that we want to optimize for conversion activities. These pages/elements are often being tested:
    - Homepage
    - Top navigation
    - Pricing page
    - Free trial
    - Contact sales
- Please check the [A/B test issue board](https://gitlab.com/gitlab-com/marketing/online-growth/boards?=&label_name[]=a%2Fb%20test/index.html.md) to see if a page you plan to update is being tested and also to see if a page you want to test is being tested or in plan to test.  The URL will be the first word or `HP` for the homepage.  If you have an MVC update to any of the pages in the `Doing` column, contact @lbanks and we can scheduled tests around MVC updates or determine if updates can wait for tests to finish.  Tests take 1 day to 4 weeks depending on traffic and conversion volume.

## Links on about.gitlab.com

We should link to resources that will help our readers. Be sure to include links to blog posts, guides, and other reference material. You can also include links to company or product websites if they are relevant to your topic. These links do not need to be "nofollowed" if they are informational.

However, we should use [Google's guidelines on nofollowing links](https://webmasters.googleblog.com/2016/03/best-practices-for-bloggers-reviewing.html/index.html.md) when we exchange a link for a product or service. It's also a best practice to ask for a nofollow link when we sponsor and disclose our links to sponsored content.

## URL Tagging

All URLs that are promoted on external sites and through email must use UTM URL tagging to increase the data cleanliness in Google Analytics and ensure marketing campaigns are correctly attributed. For a primer course, please see the [training video](https://drive.google.com/a/gitlab.com/file/d/0B1_ZzeTfG3XYNWVqOC11NWpKWjA/view?usp=sharing/index.html.md). This explains the why and how of URL tagging.

Our internal URL tagging tool can be accessed on Google Sheets under the name "Google Analytics Campaign Tagging Tool" which can be found on the Google drive. You will also find details in this spreadsheet on what "Campaign Medium" to use for each URL.

UTM best practices: lowercase, not camelcase, and no spaces, .com or special characters (&*%$+#@, etc./index.html.md) for new tags.  if you need a new campaign medium, please check with the online growth team as new mediums will not automatically be attributed correctly.

## Weekly Website Health Check

Every Friday a website health check should be performed. This check is meant to ensure that there are no issues with the website that could cause issues with traffic to the site. These are the following things to check to ensure the health of the site:

* [Google Webmaster Tools](https://www.google.com/webmasters/tools/index.html.md/index.html.md)
* [Bing Webmaster Tools](http://www.bing.com/toolbox/webmaster/index.html.md)
* [Google Analytics](https://analytics.google.com/analytics/web/index.html.md/index.html.md)

Issues to look for in each of these tools:

* **Google Webmaster Tools**: Check the dashboard and messages for any important notifications regarding the website. Also check under `Search Traffic` > `Manual Actions` for any URLs that have been identified as spam or harmful content.
* **Bing Webmaster Tools**: Check all the links under `Security`.
* **Google Analytics**: Compare organic site traffic from the most previous week compared to the previous week and look for any large fluctuations.

## Reporting

Information about reporting done by the Online Growth team and across the Marketing functional group can be found in the [Business Operations - Reporting](https://github.com/isamu-isozaki/teamai_test/tree/master/#reporting/index.html.md/index.html.md) section.

## Online Growth Tools

We use a variety of tools to support the other team within the company. Details about the tech stack, who has access and the system admins is found in the [Business Operations handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/business-ops/#tech-stack/index.html.md) section.

## Adding Redirects To GitLab's Website

Occasionally we will need to change URL structures of the website and we want to make sure that people trying to view those pages can find the information they need.

To set up a redirect, follow the instructions for [adding a redirect to the company handbook](https://github.com/isamu-isozaki/teamai_test/tree/masterhttps://github.com/isamu-isozaki/teamai_test/tree/master-usage/#adding-redirects-to-the-handbook/index.html.md)

## Google Analytics Crash Course

### Dimensions vs Metrics

Dimensions are the different attributes of your data. For example, the landing page is a dimension that is the first page a person views when they come to the site.

Metrics are the numbers that are being measured, such as number of page views or number of sessions.

Each dimension and metric has a scope, so it’s important to understand the three different scopes:  
1. User-level
1. Session-level
1. Page-level

Due to the scoping, not every dimension can be combined with every metric. In most cases, the dimensions and the metrics should match the scope.

### Understanding Reporting

#### Setting a date range

You can use the calendar in the top right to set the active date range. You can also select the `compare to` box to compare metrics from different time periods. This will allow you to see month over month or year over year growth for the desired metrics.

#### Annotations

Annotations are used to mark a point in time in Google Analytics. They can be used to mark an important event such as a change to the setup of Google Analytics, or an event that heavily impacted traffic positively or negatively.

To create an annotation, double-click on a date. The double-click will bring up the annotation field where you can enter details, and select `private` or `public`. Public annotations can be seen by anyone that has access to that view within Google Analytics, and private annotations can only be seen by you.

#### Data Tables

Most reports have a data table below the graph. The data tables contain a dimension and associated metrics.

The `Primary Dimension` of the data tables can be changed by selecting a different primary dimension from above the table.

A secondary dimension can also be added by clicking on the `Secondary Dimension` button above the table and selecting the secondary dimension you’d like to add to the table.

### Audience Reports

The audience reports are used to understand characteristics of your users such as location, and browser used, and user behavior over multiple visits such as average session time.

### Acquisition Reports

The acquisition reports help you know how people find the website. These reports will help you to analyze the benefits of the different digital marketing efforts that you are involved in.

#### Channels Report

The `All Traffic > Channels` report breaks down all the different channels that are sending traffic to the site. You can click on any of the channels to drill down  and get more granular data about that specific channel. For example, if you click on the `Referral` channel, you will see which sites are referring traffic to your site.

### Behaviors Reports

The behaviors section is about how users use the website. This includes what pages of the site people are looking at as well as how they flow through the site.

#### All Pages Report

The `All Pages` report shows the number of times a given page was viewed within the selected period of time. You can change the primary dimension to `Page Title` if it is easier to tell what the page is by looking at the title rather than the URL.

`Avg. Time on Page` and `Bounce Rate` can be used to find underperforming content or content that is very engaging to users and can be used in future marketing efforts.

#### Landing Pages and Exit Pages

The `Landing Pages` and `Exit Pages` reports are scoped at the session and tell us how many people are beginning a session at a certain page (landing page/index.html.md) and how many people are ending a session at a certain page (exit page/index.html.md).

These reports can be valuable to see what content is bringing people to the site and what content is causing people to leave the site.

#### Events

Events can be set up to track actions that people take on the website, such as clicking links or selecting drop downs. These events can be set up in Google Tag Manager and for the most part won’t require any additional code to be placed on the website.
