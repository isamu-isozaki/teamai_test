---
layout: markdown_page
title: Pricing
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Departments

Pricing affects product, marketing, and sales.
Therefore general pricing decisions are made by the CEO.

Product makes most decisions on a day to day basis about what feature should go
in what plan based on [the paid tiers](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#paid-tiers/index.html.md).
Therefore this pricing page is in the product handbook.

## Four tiers

We have four pricing tiers.
How we make decisions on a day to day basis are specified on our [stewardship page](/stewardship/#what-features-are-paid-only/index.html.md). 

| Self-managed tier | Core | Starter | Premium | Ultimate |
| GitLab.com | Free | Bronze | Silver | Gold |
| Per user per month | $0 | $4 | $19 | $99 |
| [Buyer](https://about.gitlab.comhttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/product-marketing/#buyer-personas/index.html.md) | **Individual Contributors** | Engineering/Operations **Manager** | **Director** of DevOps/IT/Operations | **Chief** Architect, CIO, CTO, CISO, Chief Risk Officer |
| Helps with | entire DevOps lifecycle | Prioritization, Automation | Advanced Kubernetes management, Progressive delivery, Availability | Value streams, Risk, Compliance, Security, Governance |
| Main competitor | None | Atlassian | GitHub | Collabnet |
| Type of sell | No sell | Feature | Benefit/solution | Transformation |

Progressive delivery:

- Canary deploys
- Incremental rollouts
- Feature flags
- Targeted deployments
- Auto revert
- Auto remediate

Advanced Kubernetes management:

- Monitoring
- Routing to clusters
- Stateful workloads / data

## Why have

## Type of sell

- A feature sell means that people want to buy the extra features. This can be done self-serve.
- A benefit sell means that people buy the business outcomes that come with fully utilizing GitLab. You need case studies, metrics like the [conversational development index](https://docs.gitlab.com/ee/user/admin_area/monitoring/convdev.html/index.html.md), and a quarterly checkin with a technical account manager from customer success to review the status of the adoption plan. A competitive process can include a bake-off to show people are 10x faster in starting new projects with GitLab.
- A transformation sell means that people want to transform as an organization. They want to reduce cycle time with 10x and want us to help them. We do workshops with transformation consultants, and define a complete shared project.

## Hybrid sales model

There is a big price difference between the different tiers (0$, $4, $19, $99 per user per month, a price difference of infinite, 5x, 5x/index.html.md). For GitLab Inc. the majority of revenue is coming from the large enterprises buying the top two tiers.

Most companies in a similar situation would focus only on the highest tiers.
There will be pressure to increase our lowest tier to for example $8.
But we want to make a our hybrid model work for the following reasons:

1. We want to keep being a [good steward of the open source project](/stewardship/index.html.md/index.html.md).
1. The lower two tiers are a scalable way to create future customers.
1. If organization are already using Atlassian JIRA we want to be competitive with BitBucket on pricing. If they buy BitBucket it is hard for us to win them back. If they buy GitLab they discover that it can replace JIRA and over time they might buy a higher tier.

Raising the price of the lowest tier will prevent people from starting with GitLab.
It will raise short term revenue at the expense of our long term market-share.
Instead of raising prices we should focus on communicating the value of the higher tiers.
This will get easier over time when we introduce more features.
In 2016 sales people focussed on free vs. starter, in 2018 on starter vs. premium, hopefully in 2020 on premium vs. ultimate.

Charging $8 for the lowest tier and discounting aggressively when we're up against BitBucket doesn't work. It is unfair to customer that are not aware of this discount and most customer are self-serve, we never talk to them.

You can also check the viability of the different tiers by the conversion from tier to tier.
For example if 5% of users upgrade from free to starter, starter to premium, and premium to ultimate your prices are balanced.
If much more people upgrade from free to starter than from starter to premium then starter is underpriced.
Please note that when a customer chooses starter over premium that is much more visible to us than users not buying at all and this might cause us to focus too much on the first case.

A conversion rate of 5% for installations / organizations should not be confused for 5% of the market revenue.
There are organizations of different sizes and larger ones are more likely to pay and purchase a higher tier.

A 5x higher price doesn't mean there is 5x more value, just like the Starter tier doesn't provide infinite more value than the gratis Core tier.
When deciding between tiers organizations should look at the ratio between how much extra value they get divided by how much extra they pay.
If this ratio is comfortably above 1 it makes sense to move to a higher tier.
The value is in making people more effective, save time on integrating tools, faster time to value, and retiring other tools.
This should more than pay for the increased price of a tier.
An analogy would be the Iphone: it is twice as expensive as an average Android phone, and while it doesn't deliver twice as much value, the extra value is worth it the extra cost.

A low price for the lowest tier is also how we mitigate the first risk of [only selling a suite](#only-sell-a-suite/index.html.md).

As [Stripe documented](https://stripe.com/atlas/guides/business-of-saas#hybrid-sales-approaches/index.html.md) hybrid is hard because "The most common result of attempting both models simultaneously is that only one of the models receives any traction, and (because these models weave themselves into all operations of the company/index.html.md) it typically strangles the other.".

## Combining features in plans

We tried selling one feature at a time but this was was not feasible.
An improved version of that would be selling 7 main features instead of 3 plans.
Examples of main features would be High Availability, Security, Service Desk, etc.

The advantages are:

1. Gradual upgrading to more expensive features.
1. Pay only for the features you use.
1. Add-ons are a common way of selling this.

The disadvantages are:

1. It is [suboptimal for both the buyer and GitLab Inc.](http://cdixon.org/2012/07/08/how-bundling-benefits-sellers-and-buyers/index.html.md/index.html.md).
1. It is hard for the buyer to estimate how much of each feature they will need.
1. The complexity lengthens the sales process.
1. For users it is unclear what features they can use.
1. The true-up process becomes more complex.
1. The customer has to administer a process how users can get more features.
1. Features get less usage and therefore the improvements are slower.
1. It is hard to do with a hybrid sales model where there is a 25x difference between the lowest and highest paid plan.

We currently think the disadvantages outweigh the advantages.

## Multiple plans for one customer

We considered selling multiple plans to the same customer, allowing them some users on every plan.

The advantages are:

1. Gradual upgrading to more expensive features per team.
1. Pay only for the features you use.

The disadvantages are:

1. The current plans have a blended price assuming 75% of users should pay for the 5x less expensive plan so plan prices would increase by 2.5x `1/(0.25+(0.75/5/index.html.md)/index.html.md)`.
1. It is hard for the buyer to estimate how much of each tier they will need.
1. The complexity lengthens the sales process.
1. For users it is unclear what features they can use.
1. It is not common in the industry, buyers don't expect it, and it isn't a boring solution (a sub-value under our [efficiency value](https://github.com/isamu-isozaki/teamai_test/tree/master/values/#efficiency/index.html.md)/index.html.md).
1. The true-up process becomes more complex.
1. Some features are can't be disabled on a per user basis, like High Availability (HA/index.html.md).
1. The customer has to administer a process how users can get a higher plan.

We currently think the disadvantages outweigh the advantages.

Counting different types of users or other modifications of a user definition tend to lead to the same problems as above.

## True-up pricing

- With true-up pricing the license/sale is never blocking user growth.
- We currently charge 100% for people added during the year because some organizations gave an intentionally too low estimate when we charged 50%. If we technically can count user-days we can make it fair for everyone. But not sure if the technical and sales complexity is worth it.
- We're also doing quarterly true-up on request for larger customers.

## Price difference between self-managed and SaaS

Arguments to charge more for SaaS:

1. The costs of SaaS are higher for GitLab.
1. It is more logical in revenue recognition.

Arguments to at least make them equal:

1. Self-managed pricing in general tends to be higher.
1. There is more market demand for self-managed.
1. No incentive for sales to sell SaaS over self-managed.
1. Self-managed tends be be a better experience.
1. We want to incentivize customers to move to SaaS with us.

Not sure what is normal in the market, Adobe did a good job but they moved from perpetual licensing to subcriptions but it is hard to [compare the two prices](http://blogs.adobe.com/acrolaw/2015/05/a-new-way-to-buy-acrobat-dc-subscription/index.html.md/index.html.md).

## When is a dollar not a dollar?

This is the title of a [great article](https://codingvc.com/when-is-a-dollar-not-a-dollar/index.html.md/index.html.md) of which we'll apply the 8 points to GitLab below:

1. Cost vs. revenue: we can help both to reduce costs and increase revenue, make sure you align to what the priorities of the prospect are.
1. Principle agent problem: for a VP of Engineering you probably want to highlight our features that give her more visibility over features that save developers time.
1. Existing expense vs. new expense: we can make use of existing budgets, be aware that multiple can apply (dev tools, security, operations, DevOps transformation/index.html.md).
1. Above vs. below discretionary spending limits: one more reason to have multiple pricing tiers.
1. Selling services vs. customized products vs off-the-shelf products: we're selling a high margin product and augment with services when needed to make the customer more successful.
1. Selling to many stakeholders vs. one stakeholder: this is another reason for our multiple tiers, Starter is sold to the single stakeholder of development teams, Ultimate is sold to multiple stakeholders and will need the CIO to enforce the transformation.
1. Monthly vs. upfront payments: that is why we only do yearly upfront, sometimes even multi-year upfront. Also yearly is the standard for enterprises (Salesforce sells it like this/index.html.md) and helps reduce support costs that are an order of magnitude grater for .com (most likely to be monthly/index.html.md) vs. self-managed.
1. Selling vs. upselling: this is why we have multiple tiers.

## Only sell a suite

Most companies evolve in the following way:

1. Sell one product
1. Sell multiple products
1. Sell multiple products and a suite of them
1. Only sell a suite

An example is Microsoft Office where it is costly to buy components of Office365 separately, although higher tiers include more products.
At GitLab we decided to skip the intermediate steps and immediately only offer a suite that includes all our products.
Having our complete scope included in our open source version is even part of our [stewardship promises](/stewardship/#promises/index.html.md).

Selling only a suite has risks, after the => is how we mitigate those at GitLab:

1. Lose potential customers if people want one product. => Offer a Starter tier that is priced competitively with single products from competitors.
1. Leave money on the table if people want all products. => Offer an Ultimate tier that is great value if you adopt everything of GitLab.
1. Discount because people don't want all the products. => Make a discount conditional on not using part of the product.
1. Tiers are harder to define than if you would have separate products. => Hard to mitigate, we have to work extra hard on communicating the differences.
1. No revenue feedback from customer about what products they value more. => The product function focusses on usage data as our best proxy for value.

Companies evolve to selling only a suite for the following reasons, after the => is how this applies to GitLab:

1. Makes it easier for organizations to adopt the other products. => This is essential, organizations have official solutions and GitLab grows with organic adoption from developers.
1. Show customers the benefit of a [single application](/direction/#single-application/index.html.md). => This is essental since people are skeptical, showing beats telling.
1. More usage of all the products. => This is essential for us due to our [breadth over depth strategy](strategy#breadth-over-depth/index.html.md)
1. Harder to displace the suite once it is in place. => This will help if competitors offer a service based on our open source code.

We're going even further than selling a suite by integrating everything in a single application. We do that because of the advantages mentioned on our [direction page section about us being single application](/direction/#single-application/index.html.md). A secondary effect is that the user doesn't have to make a buying, or even an adoption, decision.

## Value creation

There are two factors that determine how much value Gitlab creates for an organization, in order of importance:

1. Scope: how many parts of GitLab you use, indicated by the DevOps score, how many components of GitLab are in use.
1. Size: how many people work in an organization and use GitLab.

When an organization is larger the benefits of GitLab are larger because:

- Coordination take up a greater amount of the work. 80% is coordination costs it is much more valuable to reduce that then when it is 20%.
- Harder and more expensive to train people and enforce best practices.
- More silo's that benefit from innersourcing.
- More cancellations, longer cycles, more time to win.
- Higher requirements for governance.

## Value capture

Since GitLab is an open core projects we'll always create much more value then we (are able to/index.html.md) capture. Based on the value created the straightforward way to capture value would be to:

1. Scope: charge a higher price per user the more of GitLab you use.
1. Size: Charge a higher price per seat the more users you have.

These straightforward ways are not possible for the following reasons:

1. Scope: charging more for adoption would hurt the adoption of GitLab for the whole lifecycle. In January 2018 version control is 10 times more popular then the next feature (CI/index.html.md). We need the features to spread organically so people can create the more value with GitLab. People are much more willing to pay when they are already using a part of the lifecycle.
1. Size: many other software companies limit the maximum amount of users in certain [tiers](https://about.gitlab.comhttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/product-marketing/#tiers/index.html.md). For GitLab we can't do this because the open source version can't contain artificial restrictions. We can do it in our proprietary tiers but this doesn't seem symmetrical. It also feels unfair if you have to pay more simply by being a bit larger then the limit.

So we're left with charging for features.
We can't charge for each feature separately since that in unwieldy for the customer.
So we charge with for tiers that contain a bundle of features.
We  select features in the (more expensive/index.html.md) paid tiers that:

1. Scope: become more useful and valuable as your DevOps score increases
1. Size: become more useful and valuable as your organizational size increases

Adding features to a (more expensive/index.html.md) paid tier is not the only thing stopping users from adopting them but it is a very important factor.

To simplify the above we base our feature groupings on champion position, see below.

## The likely type of buyer determines what features go in what tier

Our plans are based on [the buyer](#four-tiers/index.html.md) that buys GitLab, from individual contributor, to lead, to director, to CxO.
The feature is put in the plan based on what champion is most likely to care about it.
Buyers make sense since a higher cost plan needs a higher placed buyer.

Alternatives that don't work:

1. Pricing based on company size doesn't work, some small companies need the features of the most expensive plan.
1. [Scope and size](#value-capture/index.html.md) don't work.
1. Pricing based on maturity is strange because organizations at the beginning of their journey should pay the most, since in a greenfield you benefit the most quickly and extensively from GitLab.

## DevOps score is not maturity

What is interesting is that GitLab creates more value as you adopt more of it.
This shouldn't be confused with DevOps maturity.
DevOps maturity is how advanced your practices are an how fast your DevOps lifecycle is, shown in [cycle analytics](https://docs.gitlab.com/ee/user/project/cycle_analytics.html/index.html.md).
With the best practices embedded in GitLab you will mature faster than without it, GitLab enables a 200% faster DevOps lifecycle.
But DevOps maturity is mostly about organizational change, GitLab the product is just an enabler of it.
Even if an organization uses everything of GitLab (high DevOps score/index.html.md) they can still have a slow process (slow lifecycle/index.html.md).
We know there is a correlation between a higher DevOps score and a faster lifecycle, but especially in organizations new to DevOps it is a trend, not an absolute.
Linking our tiers to maturity would mean we don't ask any money from the large organizations that currently have a slow lifecycle but that are making it faster by adopting all of GitLab.
These large organizations with a slow lifecycle benefit the most from GitLab since they can adopt it completely because they are not held back by an existing toolchain.
