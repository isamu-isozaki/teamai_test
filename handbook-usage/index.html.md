---
layout: markdown_page
title: "GitLab Handbook Usage"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Advantages

At GitLab our handbook is extensive and keeping it relevant is an important part of everyone's job. It is a vital part of who we are and how we communicate. We established these processes because we saw these benefits:

1. Reading is much faster than listening.
1. Reading is async, you don't have to interrupt someone or wait for them to become available.
1. Recruiting is easier if people can see what we stand for and how we operate.
1. Retention is better if people know what they are getting into before they join.
1. On-boarding is easier if you can find all relevant information spelled out.
1. Teamwork is easier if you can read how other parts of the company work.
1. Discussing changes is easier if you can read what the current process is.
1. Communicating change is easier if you can just point to the diff.
1. Everyone can contribute to it by proposing a change via a merge request.

## Flow structure

1. A (process/index.html.md) problem comes up, frequently in an issue or chat.
1. A proposal is made in a merge request to the handbook.
1. Once merged, the change is announced by linking to the diff in the MR or commit. Major ones are put in the agenda of the company call. Medium ones are posted in on the #handbook channel for visibility, with a one line summary of the change . If there was an issue, close it out with a link to the diff.

## Why handbook first

Documenting things in the handbook takes more time initially. You have to think about where to make the change, integrate it with the existing content, and then possibly add to or refactor the handbook to have a foundation. But it saves time over a longer period and this communication is essential to be able to continue scaling and adapting our organization. This process is not unlike writing tests for your software. Only communicate a (proposed/index.html.md) change via a change to the handbook; don't use a presentation, email, chat message, or another medium to communicate the components of the change. These other forms of communication might be more convenient for the presenter, but it is harder for the audience to understand the context and the implications for other processes. Having a "handbook first" mentality makes sure there is no duplication, the handbook is always up-to-date, and others are able to contribute.

## Handbook guidelines

Please follow these guidelines and remind others of them.

1. Most guidelines in this handbook are meant to help, and unless otherwise stated, are meant to help more than being absolute rules. Don't be afraid to do something because you don't know the entire handbook, nobody does. Be gentle when reminding people about these guidelines. For example say, "It is not a problem, but next time please consider the following guideline from the handbook."
1. If you ask a question and someone answers with a link to the handbook, they do this because they want to help by providing more information. They may also be proud that we have the answer documented. It doesn't mean that you should have read the entire handbook, nobody knows the entire handbook.
1. If you need to ask a team member for help, please realize that there is a good chance the majority of the community also doesn't know the answer. Be sure to **document** the answer to radiate this information to the whole community. After the question is answered, discuss where it should be documented and who will do it. You can remind other people of this request by asking "Who will document this?"
1. When you discuss something in chat always try to **link** to a URL where relevant. For example, the documentation you have a question about or the page that answered your question. You can remind other people of this by asking "Can you please link?"
1. To change a guideline or process, **suggest an edit** in the form of a merge request.
After it is merged you can talk about it during the company call if applicable. You can remind other people of this by asking "Can you please send a merge request for the handbook?"
1. When substantially changing handbook layout, please leave a link to the specific page of the review app **that is directly affected by this MR**. Along with the link, include as much info as possible in the MR description. This will allow everyone to understand what is the purpose of the MR without looking at diffs.
1. Communicate process changes by linking to the **merged diff** (a commit that shows the changes before and after/index.html.md). If you are communicating a change for the purpose of discussion and feedback, it is ok to link to an **unmerged diff**. Do not change the process first, and then view the documentation as a lower priority task. Planning to do the documentation later inevitably leads to duplicate work communicating the change and it leads to outdated documentation. You can remind other people of this by asking "Can you please update the handbook first?"
1. Remember, the handbook is not what we hope to do, what we should formally do, or what we did months ago. **It is what we do right now.** Make sure you change the handbook in order to truly change a process. To propose a change to a process, make a merge request to change the handbook. Don't use another channel to propose a handbook change (email, Google Doc, etc./index.html.md).
1. Like everything else, our processes are always in flux. Everything is always in draft, and the initial version should be in the handbook, too. If you are proposing a change to the handbook, whenever possible, skip the issue and submit a merge request. Mention the people that affected by the change in the merge request. In many cases, merge requests are easier to collaborate on since you can see the proposed changes.
1. Proposing a change via a merge request is preferred over an issue description. A merge request allows people to see the context of your change.
1. If something is a limited test to a group of users, add it to the handbook and note as such. Then remove the note once the test is over and every case should use the new process.
1. When communicating something always include a link to the relevant (and up-to-date/index.html.md) part of the **handbook** instead of including the text in the email/chat/etc. You can remind other people of this by asking "Can you please link to the relevant part of the handbook?"
1. If you copy content please remove it at the origin place and replace it with a link to the new content. Think about the information architecture so that you **Don't Repeat Yourself**. Duplicate content leads to updating it in the wrong place, keep it [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself/index.html.md).
1. Make sure to always cross-link items if there are related items (elsewhere in the handbook, in docs, or in issues/index.html.md).
1. The handbook is structured by function and result to ensure every item in it has a clear owner and location in order to keep it up-to-date. Please cross-link liberally to point people to other sections. Avoid unstructured content based on format like: FAQ's, lists of links, resource pages, glossaries, courses, videos, tests, or how-to's. These are very hard to keep up-to-date and are not compatible with organization per function and result. Instead put the answer, link, definition, course, video, or test in the most relevant place. Use descriptive headers so that people can easily search for content. Please mix different formats in the handbook on the same page. Having multiple formats to use is valuable and different people prefer different formats. Worry about the organization per function and result, not about how it will look if you embed different types of content.
1. The handbook is the process. Any sections with names like 'process', 'policies', 'best practices', or 'standard operating procedures' are an indication of a deeper problem. This may indicate a duplication between a prose description of a process and a numbered list description of the same process that should be combined in one description of the process.
1. Use headers liberally. If a page is longer than one screen, add an automatically generated Table of Contents (ToC/index.html.md) by copying [line 6 to 10 in this MR](https://gitlab.com/gitlab-com/www-gitlab-com/merge_requests/7141/diffs#f054d0f855ebef2a11559c362a356a2f9e010b99_6_6/index.html.md)/index.html.md). On the desktop, we have a side bar with the ToC but not on mobile. With is in mind, it is good to add one if there are more than 2 headers. Headers should have normal capitalization (don't use [ALL CAPS](https://en.wikipedia.org/wiki/All_caps/index.html.md) nor [TitleCase](http://www.grammar-monster.com/glossary/title_case.htm/index.html.md)/index.html.md). After a header have one blank line, this is [not required in the standard](http://spec.commonmark.org/0.27/#example-46/index.html.md) but is our convention.
1. If someone inside or outside GitLab makes a good suggestion invite them to add it to the handbook. Send the person the url of the relevant page and section and offer to do it for them if they can't. Having them make and send the suggestion will make the change and will reflect their knowledge.
1. All documentation that also applies to code contributions from the wider community should be in the GitLab CE project (for example in [CONTRIBUTING](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md/index.html.md) or the [code review guidelines](https://docs.gitlab.com/ee/development/code_review.html/index.html.md)/index.html.md), not the handbook that is only for team members.
1. Learn how to edit the [handbook using git](https://github.com/isamu-isozaki/teamai_test/tree/master/git-page-update/index.html.md). Please read through the [Writing Style Guidelines](https://github.com/isamu-isozaki/teamai_test/tree/master/communication/#writing-style-guidelines/index.html.md) before contributing.
1. When you submit a merge request, make sure that it gets merged quickly. Making single, small changes quickly will ensure your branch doesn't fall far behind master, creating merge conflicts. Aim to make and merge your update on the same day. Mention people in the merge request or reach them via Slack. If you get a suggestion for a large improvement on top of the exiting one consider doing that separately. Create an issue, get the exiting MR merged, then create a new merge request.
1. Only mark a merge request as "WIP" (Work in Progress/index.html.md) if it will negatively affect the company if merged too early. That can be the case for application code but is almost not possible for handbook MRs.
1. If you have to move content have a merge request that moves it and does nothing else. If you want to clean it up, summarize it, or expand on it do that haver the moving MR is merged. This is much easier to review.
1. The handbook is for things concerning (future/index.html.md) GitLab team members only. If something concerns users of GitLab, it should be documented in the [GitLab documentation](https://docs.gitlab.com/index.html.md/index.html.md), the [GitLab Development Kit (GDK/index.html.md)](https://gitlab.com/gitlab-org/gitlab-development-kit/index.html.md), the [CONTRIBUTING file](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md/index.html.md) or the [PROCESS file](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md/index.html.md).
1. Keep your handbook pages short and succinct. Eliminate fluff and get right to the point with the shortest possible wording. Keep in mind that the biggest challenge cited by new employees is the vast amount of information to take in during on-boarding.
1. We don't need [.gitkeep files](http://www.ryanwright.me/cookbook/git/gitkeep/index.html.md) in our handbook, they make it harder to quickly open a file in editors. Don't add them, and delete them when you see them.
1. Anything more than a spelling correction is better done in the terminal than with the online editor. All people that are reluctant to update the handbook are not using the terminal, a local editor, and a local preview. Please follow the instructions in [edit this website locally](https://github.com/isamu-isozaki/teamai_test/tree/master/git-page-update/index.html.md/index.html.md).
1. When mentioning currency amounts that team members may need to convert to their local currency (e.g. benefits, expenses, or bonuses/index.html.md), link those amounts to our [Exchange Rates](https://github.com/isamu-isozaki/teamai_test/tree/master/people-operations/global-compensation/#exchange-rates/index.html.md) section (e.g. [500 USD](https://github.com/isamu-isozaki/teamai_test/tree/master/people-operations/global-compensation/#exchange-rates/index.html.md)/index.html.md).
1. Try to add the why of a handbook process, what is the business goal, what is the inspiration for this section. Adding the why makes processes easier to change in the future since you can evaluate if the why changed.
1. Everyone should subscribe to the #handbook channel to stay up-to-date with changes to the handbook

## Adding Redirects to the Handbook

Because the handbook is a living, breathing document, page names, locations, and URLs are bound to change over time. If you make a change that could break one or more links elsewhere in the handbook, it will be necessary for you to set up a redirect. Working with our NGINX setup is a technical process, so we rely on the Production team to help with these requests.

Please do not create meta refresh (client side or JavaScript/index.html.md) redirects. 301 redirects are the correct method for ensuring good SEO and user experience of our site.

To do so, open an issue in the [Infrastructure project](https://gitlab.com/gitlab-com/gl-infra/infrastructure/index.html.md). Provide the following:
* Old URL that needs to be redirected
* New URL where users should now be sent
If you have any specific questions or concerns regarding the merge request, you can reach out via the `#production` channel on Slack.

## Management

It is each department and team member's responsibility to ensure the handbook stays current. People Operations will partner with a representative from each department (engineering, marketing, etc/index.html.md) through weekly reviews to verify the content in the handbook is accurate and follows the same format as outlined in the [Guidelines](https://github.com/isamu-isozaki/teamai_test/tree/masterhttps://github.com/isamu-isozaki/teamai_test/tree/master-usage/#guidelines/index.html.md). For questions on who to submit a merge request to, or assistance with the handbook, please ping `@gl-handbookupdate` on GitLab.

Any changes to the handbook as part of this review will be shared in the `#handbook` channel in Slack. People Ops will also ensure that questions asked in `#questions` are documented and all announcements on the company call have a relevant link.

## Screenshare the handbook instead of creating a presentation

Presentations are great for ephemeral content like [functional group updates](https://github.com/isamu-isozaki/teamai_test/tree/master/people-operations/functional-group-updates/index.html.md/index.html.md) and board presentations. [Evergreen content](https://www.thebalance.com/what-is-evergreen-content-definition-dos-and-don-ts-2316028/index.html.md) like a [leadership training](https://github.com/isamu-isozaki/teamai_test/tree/master/leadership/#training/index.html.md) should be based on the handbook. Please screenshare the handbook instead of creating a presentation for evergreen content because:

1. It saves you the effort of creating a presentation.
1. People can easily find the handbook section later on.
1. The handbook is checked and improved as part of the preperation.
1. The content is open to contributions.
1. The content is integrated with the rest of our processes.
1. Also see some of the [advantages of using our handbook](https://github.com/isamu-isozaki/teamai_test/tree/masterhttps://github.com/isamu-isozaki/teamai_test/tree/master-usage/index.html.md/index.html.md).

## Make it worthwhile

Another company asked how we managed to work with the handbook because at their company it wasn't working: "There are many occasions where something is documented in the knowledge base, but people don't know about it because they never bothered to read or search. Some people have a strong aversion against what they perceive as a 'wall of text'."

To ensure that people's time is well spend looking at the handbook we should:

1. Keep your handbook pages short and succinct
1. Use present tense and simple words
1. Organize per function so the information architecture is clear
1. Cross-link liberally so users can find relevant other information easily
1. Great search function (we use Algolia/index.html.md)
1. Make it public so you can Google search
1. Have clean urls and allow for deeplinking paragraphs
1. Use automatic tables of content
1. Have lots of headers that give the key message
1. Make key words bold
1. When people ask questions link to the handbook instead of giving the answer
1. Test people on their knowledge during onboarding
1. Avoid duplication, instead just link
1. Give real examples
1. Avoid corporate speak, describe things like you're talking to a friend
1. Use lots of numbered lists, unordered lists, and tables
1. Embed videos to consume the content by watching
1. Add drawings, gifs, cartoons, and graphics to make it interesting and memorable
1. When someone asks something that isn't there, add it to the handbook and respond with a link to the diff
