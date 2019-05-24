---
layout: markdown_page
title: "UX Designer"
---

### On this page

{:.no_toc}

- TOC
{:toc}

## UX Designer

Like other departments at GitLab, we follow the [GitLab Workflow](https://github.com/isamu-isozaki/teamai_test/tree/master/communication/#everything-starts-with-an-issue/index.html.md) and the [Engineering Workflow](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/workflow/index.html.md/index.html.md). Reviewing those resources is a good starting point for context on the UX designer workflow below.

### UX Designer onboarding

If you are just starting out here at GitLab, welcome! Make sure to review all the pages here in the UX section of the handbook, they will help you get oriented. There is also a specific page dedicated to [UX Designer onboarding](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ux/uxdesigner-onboarding/index.html.md).

### Working on issues

#### Scheduling of issues in a milestone
All issues in a milestone labeled [Deliverable](https://gitlab.com/groups/gitlab-org/issues?state=opened&label_name%5B%5D=Deliverable/index.html.md) that need UX will be assigned to a UX designer by the kickoff. The UX Manager is responsible for scheduling.

Issues labeled [Stretch](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Stretch/index.html.md) may or may not be assigned to a UX designer by the kickoff. 

#### Priority for UX issues
UX works on issues in the following order:
* Has the current release milestone and is labeled Deliverable
* Has the current release milestone and is labeled Stretch
* Has the next release milestone
* [Has the **Accepting Merge Requests label**](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Accepting%20Merge%20Requests/index.html.md)
* [Has milestone **Next 2-3 months**](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&milestone_title=Next+2-3+months&label_name%5B%5D=UX/index.html.md)
* [Has milestone **Next 3-6 months**](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&milestone_title=Next+3-6+months&label_name%5B%5D=UX/index.html.md)
* [Has milestone **Backlog**](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&milestone_title=Backlog&label_name%5B%5D=UX/index.html.md)
* [Popular or with high community involvement (number of comments or upvotes/index.html.md)](https://gitlab.com/groups/gitlab-org/issues?label_name%5B%5D=UX&scope=all&sort=upvotes_desc&state=opened/index.html.md)
* [Everything else](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=UX/index.html.md)

#### Work
Define the scope:
* Product Managers(PM/index.html.md) and UX Designers are very closely related although they might seem different. Both PM and UX Designers work within the _problem–solution_ spectrum in order to better understand the problem that needs to be solved and to determine the most viable solution that addresses that problem. Over-communicate with PMs, it's the best way to understand the problem and arrive at a solution.
* Bring another designer in to have an additional set of eyes on your process if needed. This might make it easier to discuss holistic design decisions and to provide feedback regarding any uncertain elements in your work.
* Loop in other members of engineering. Encourage them to contribute to finding the solution. They will have important insight into possible technical limitations.
* Before coming up with any solution, discuss the scope with the PM, ask questions, and define what the problem really is (often it's not what people think it is/index.html.md).
* Investigate whether there is [existing UX Research](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ux/ux-research#ux-research-archive/index.html.md) or data that could help inform your decision and measure the results. If there isn't, consider looping in UX Researchers to conduct or assist you in conducting research for the problem.
* UX issues have a tendency to expand in scope. Aggressively split off new issues, ideas, and concepts into their own issues. Mark the new issues as related to the original issue. Large issues become really challenging to drive decisions in and make progress on. If you’re ever unsure how to split apart large issues, work with the UX Manager.
* Developers should be able to ship a product within one life cycle. If a feature is too large to ship within one release, work together to determine the best way of splitting the feature into smaller segments.
* Bring developers into the conversation early. Ask for feedback on how to split up features while still maintaining the integrity of the UX.
* Encourage developers to scope down features into multiple merge requests for an easier, more efficient review process. When deciding whether to merge into master or a feature branch, be mindful of maintaining the integrity of the UX.
* When breaking up features into smaller parts, make sure that the end design goal is known. Giving everyone the full picture will help developers write code aimed at achieving that goal in the future.
* Keep the issue description updated with the agreed scope, even if doesn’t impact your work. This is everyone’s responsibility. The issue description must be the Single Source Of Truth (SSOT/index.html.md), not the discussion or individual comments.

Propose a solution:
* Add comments with your proposals. Propose **one** solution, not multiple alternative solutions for others to pick, as this undermines your position as a UX expert and leads to a [design by committee](https://en.wikipedia.org/wiki/Design_by_committee/index.html.md) situation. If you have a good reason to propose multiple alternative solutions make sure to explain why.
* Wireframing, mockups, and prototyping all have their own place. You should utilize the best tool for communicating a problem/design/solution.
* Proposals don't need to have images. Sometimes words can paint a surprisingly good picture of how an experience should feel, look, and behave.
* Frame discussion around the problem being solved, not the designs specifically.
* Anticipate questions that others might have and try to answer them in your proposal comments. You don’t have to explain everything, but try to communicate a bit of your rationale every time you propose something. This is particularly important when proposing changes or challenging the status quo. This reduces the feedback loop and time spent on unnecessary discussions while contributing to the credibility of the UX Department, who deal with a lot of *seemingly* subjective issues.
* Keep the SSOT updated with what’s already agreed upon so that everyone can know where to look. This includes images or links to your design work.
* If you’re working with design files, follow the instructions in the [GitLab Design project contribution guidelines][gitlab-design-project-contribution-guidelines] and regularly commit them.
* If you are proposing a solution that will introduce a new UX paradigm, or change an existing one, please consider the following: 
1. Will this pattern be inconsistent with other areas of the application? 
1. Will other areas of the application need to be updated to match? 
1. Does this new pattern significantly improve the user experience? 
1. If you decide that it is worth changing/updating the pattern, there are additional steps that must be followed. See the [Maintain](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/ux/ux-designer#maintain/index.html.md) section below for those steps.

#### Deliver

* Once your work is complete, make sure that the issue description, the SSOT, is updated with a section called "Solution". This is where you should direct people when they have questions about what should be done and how.
* As applicable, commit all design assets and files according to the instructions in the [GitLab Design project contribution guidelines][gitlab-design-project-contribution-guidelines].
* Whenever possible, you should provide spec-previews using the Sketch Measure plugin. Details on how to use this are located in the [design repository on the contribution page](https://gitlab.com/gitlab-org/gitlab-design/blob/master/CONTRIBUTING.md#superpowers-/index.html.md).
* Once UX work is completed and all feedback is addressed, remove the [UX][ux-label] label, add the [UX ready][ux-ready-label] label, and:
    * If the issue is not scheduled, mention the [responsible product manager](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#who-to-talk-to-for-what/index.html.md) to [schedule it](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/workflow/#scheduling-issues/index.html.md)
    * Remain assigned. You will be the 'go-to' person for UX questions and reviews on this issue.

#### Follow through

* Keep the SSOT in the description updated until the issue is closed. This applies to both text and mockups. Previous content (by a PM, for example/index.html.md) should be removed or archived into a separate section in the description. If the developer working on the issue ever has any questions on what they should implement, they can ask the designer to update the issue description with the design.
* For obvious changes, make the SSOT description update directly. [You don't need to wait for consensus](https://github.com/isamu-isozaki/teamai_test/tree/master/values/index.html.md/index.html.md). Use your judgement.
* Make sure you remain assigned and that you’re subscribed to the issue and related merge requests. Continue to follow them, addressing any additional UX issues that come up.

#### UX Reviews

* UX is part of the MR review process.
* UX Review requests should be prioritized, tackle them as quickly as you are able.
* Test it locally, do not rely on screenshots.
* Be thorough, there should be as little back and forth as possible.
* If you are asked to review an MR for an issue you were not assigned to, remind the author who the assigned designer is and assign to original designer for review.
* When reviewing an MR, please use the following order of importance:
    * Functionality first - does it work?
    * Edge cases - are there any unexpected edge cases?
    * Visual consistency/accuracy.
* Remember to stick to the issue, create issues for further updates to avoid scope creep.

#### Maintain

If the UX work introduces or changes any of the UX standards or building blocks:

* [Create an issue](https://gitlab.com/gitlab-org/gitlab-design/issues/new?issuable_template=UX%20Pattern/index.html.md) in the [GitLab Design Project](https://gitlab.com/gitlab-org/gitlab-design/index.html.md) and follow the pattern checklist to record the new standard and update the [GitLab Pattern Library Sketch file](https://gitlab.com/gitlab-org/gitlab-design/blob/master/gitlab-pattern-library.sketch/index.html.md).
* Once the pattern has been added to the [GitLab Design Project](https://gitlab.com/gitlab-org/gitlab-design/index.html.md), create an issue and MR to add the pattern and documentation to the [GitLab Design System](https://gitlab.com/gitlab-org/design.gitlab.com/index.html.md).
* As applicable, create issue(s/index.html.md) to update areas of the application that are affected by this pattern. 
* Add an agenda item to the next UX weekly call to inform everyone of those changes.
* If the change/addition is a significant one, consider adding it to the Company Call to inform the company of the changes.

#### Approach

As design can be subjective, discussion can heat up. Always try to be [direct](https://github.com/isamu-isozaki/teamai_test/tree/master/values/#directness/index.html.md), but [kind](https://github.com/isamu-isozaki/teamai_test/tree/master/values/#kindness/index.html.md). Try to give your best reasoning for your choices and evaluate everyone's opinions. Come up with a solution instead of discussing endlessly. If you think additional perspective is needed, mention a fellow UX Designer in the issue.

[ux-guide]: https://docs.gitlab.com/ee/development/ux_guide/
[ux-label]: https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX
[ux-ready-label]: https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX+ready
[gitlab-design-project-contribution-guidelines]: https://gitlab.com/gitlab-org/gitlab-design/blob/master/CONTRIBUTING.md
[twitter-sheet]: https://docs.google.com/spreadsheets/d/1GDAUNujD1-eRYxAj4FIYbCyy8ltCwwIWqVTd9-gf4wA/edit
