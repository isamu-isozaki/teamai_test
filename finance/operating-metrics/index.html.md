---
layout: markdown_page
title: "Operating Metrics"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Review Process
We track a wide range of dimensions and metrics on our corporate dashboard. Many definitions are self evident but some are not.

### Customers
We define customers in the following categorical level of detail:
1. Subscription: The number of organizations that have entered into a unique subscription contract with GitLab for which the term has not ended. As customers become more sophisticated users of GitLab the number of subscriptions may decline over time as Accounts and Parents consolidate subscriptions to gain more productivity.
1. Account: We define an Account as an organization that controls multiple subscriptions that have been purchased under a group with  common leadership. In the case of the U.S. government, we count U.S. government departments and major agencies as a unique account.
1. Parent: We define a Parent as an accumulation of Accounts under an organization with common ownership. In the case of the U.S. government, we count U.S. government major agencies as a unique parent account. (In Salesforce this is the `Ultimate Parent Account` field) 

### Monthly Recurring Revenue (MRR)
Recurring revenue recognized in current month.

### Annual Recurring Revenue (ARR)
The sum of Monthly Recurring Revenue plus True-ups received in the month divided by twelve multiplied by 12. =((MRR+True-ups/12)*12)

### Days Sales Outstanding (DSO)
Average Accounts Receivable balance over prior 3 months divided by Total Contract Value (TCV) bookings over the same period mutilpied by 90 that provides an average number of days that customers pay their invoices.  Link to a good [definition](https://www.investopedia.com/terms/d/dso.asp)  and [Industry guidance](https://www.opexengine.com/software-industry-revenue-growth-accelerating-and-hiring-expected-to-jump-according-to-new-siiaopexengine-report/) suggests the median DSO for SAAS companies is 76 days. Our target at GitLab is 45 days.

### Average Sales Price (ASP)
Gross IACV per won deal.

### Gross Incremental Annual Contract Value (Gross IACV)
Value of new bookings from new and existing customers that will result in recurring revenue over the next 12 months. Gross IACV includes True Ups 

#### Growth Incremental Annual Contract Value (Growth IACV)
Contract value that increases at the time of subscription renewal

#### New Incremental Annual Contract Value (New IACV)
Contract value from a new subscription customer 

### Lost Renewal
Contract value that is lost at the time of subscription renewals. Lost Renewals examples include cancellations at or before the subscription renewal date. 

### Downgrade
Contract value that results in a lower value than the previous contract value. Downgrade examples include seat reductions, product downgrades, discounts, and customers switching to Reseller at time of renewal. 

### Credit
Lost or lowered contract value that occurs before a subscription renewal or subscription cancellation 

### Incremental Annual Contract Value (IACV)
Value of new bookings from new and existing customers that will result in recurring revenue over the next 12 months less any credits, lost renewals, downgrades or any other decrease to annual recurring revenue. Excluded from IACV are bookings that are non-recurring such as professional services, training and non-recurring engineering fees (PCV). Also equals ACV less renewals. However, bookings related to true up licenses, although non-recurring, are included in IACV.

### Annual Contract Value (ACV)
Current Period subscription bookings which will result in revenue over next 12 months. For multiple year deals with contracted ramps, the ACV will be the average annual booking per year.

### PCV (ProServe Contract Value)
Contract value that is not considered a subscription and the work is performed by the Professional Services team

### Total Contract Value (TCV)
All bookings in period (including multiyear); bookings is equal to billings with standard payment terms.

### Retention, Net (Dollar Weighted)
Current period MRR plus true-ups from customers that were on board 12 months prior divided by MRR plus true-ups from 12 months prior.

### Retention, Gross (Dollar Weighted)
Remaining cohorts from Actual Subscription customers active as of 12 months ago multiplied by revenue from 12 months ago divided by actual Subscription customers as of date 12 months prior multiplied by revenue from 12 months ago. [Industry guidance]("http://www.forentrepreneurs.com/saas-metrics-2/") suggests median gross dollar churn performance for SaaS/subscription companies is 8% per year

### Customer Acquisition Cost (CAC)
Total Sales & Marketing Expense/Number of New Customers Acquired

### CAC Ratio
Total Sales & Marketing Expense/ACV from new customers (excludes growth from existing).  [Industry guidance](http://www.forentrepreneurs.com/2017-saas-survey-part-1/) reports that median performance is 1.15 with anything less than 1.0 being considered very good.

### LTV to CAC Ratio
The customer Life-Time Value to Customer Acquisition Cost ratio (LTV:CAC) measures the relationship between the lifetime value of a customer and the cost of acquiring that customer. [A good LTV to CAC ratio is considered to be > 3.0.](https://www.klipfolio.com/resources/kpi-examples/saas-metrics/customer-lifetime-value-to-customer-acquisition-ratio)

### New ACV / New Customers
Net IACV that come from New Customers divided by the number of net closed deals in the current month

### New ACV / New Customers by Sales Assited
Net IACV that come from New Customers and sold by the field sales team divided by the number of net closed deals in the current month

### Rep Productivity
Monthly IACV / number of quota carrying sales representatives on board for at least 90 days prior to start of period.

### Magic Number
IACV for trailing three months / Sales & Marketing Spend over trailing months -6 to months -4 (one quarter lag). [Industry guidance](http://www.thesaascfo.com/calculate-saas-magic-number/) suggests a good Magic Number is > 1.0.

### MQL
[Marketo Qualified Lead](/handbook/business-ops/#customer-lifecycle)

### SQL
[Sales Qualified Lead](/handbook/business-ops/#customer-lifecycle)

### Cost per MQL
Marketing expense divided by the number of MQLs

### Sales efficiency ratio
IACV / sales and marketing spend. [Industry guidance](http://tomtunguz.com/magic-numbers/) suggests that average performance is 0.8 with anything greater than 1.0 being considered very good.

### Marketing efficiency ratio
IACV / marketing spend

### Field efficiency ratio
IACV / sales spend

### LTV
Customer Life-Time Value = Average Revenue per Year x Gross Margin% x 1/(1-K) + GxK/(1-K)^2; K = (1-Net Churn) x (1-Discount Rate).  GitLab assumes a 10% cost of capital based on current cash usage and borrowing costs.

### CSAT
Customer Satisfaction - A measure of the satisfaction of service from a customer's interaction with the GitLab Support team. Based on survey responses from customers after the ticket is solved by the GitLab Support team using a Good/Bad rating. (CSAT = Satisfied / Total Survey Responses)

### SLA
Service Level Agreement - GitLab Support commits to an initial substantive response in a specified amount of time from the time the customer submits a ticket.  The SLA for this first reply is based on a customer's Support plan.  The SLA is currently measured on tickets submitted by customers with our top Support plans (Premium for Self-managed, Gold for Gitlab.com). The SLA is calculated by (Number of Times SLA met / Total Tickets SLA was applicable).

### Capital Consumption
TCV less Total Operating Expenses.  This metric tracks net cash consumed excluding changes in working capital (i.e. burn due to balance sheet growth). Since the growth in receivables can be financed with using cheap debt instead of equity is a better measure of capital efficiency than cash burn.

### Monthly Metrics Review

Purpose:  We review all key operating metrics that either i) appear in the Corporate metrics sheet or ii) are included in the our Operating Model. The goal for the monthly meeting is to understand month to month variances as well as variances against the plan, forecast and operating model.

Agenda:
1. Review metric and conclude on implications for operating model.
1. Discuss proposals for different measurement.
1. Determine if external benchmarks are required.
1. Discuss proposals for addition of new metrics.
1. Discuss proposals for deprecation of existing metrics

Timing:  Meetings are monthly starting on the 10th day after month end.

Invitees:  Mandatory attendees are the owner of the metric and eteam functional representative and the CFO.  Optional attendees are the rest of the e-team and anyone who has an interest in the metric.

Meeting Format:
1. The metric owner will prepare a google slide presentation with the content to be reviewed. 
1. A google doc will also be attached for participants to log questions or comments for discussion.
1. The slide header or text on the slide should convey whether the metric result is good or needs improvement.
1. Wherever possible the metric being reviewed should be compared to Plan, OKR target or industry benchmark.
1. The metric owner is expected to present a summary of highlights which should not last more than three minutes.
1. The metric owner is responsible for preparing the document in advance of the meeting. The owner should update the meeting invite and send to all guests so they know the materials are ready for review.
1. The first 10 minutes of the meeting is reserved for the participants to review the materials with the meeting starting at 10 minutes after the calendar start time.
1. For an example of a presentation to model after search this slide file on Drive "Sales Metrics- 2018-09-21"

