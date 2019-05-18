---
layout: markdown_page
title: "Frontend Department"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Teams

There are two teams within the Frontend group: General and UI Components.

- General team is primarily focused on delivering product features (Discussion, CI/CD, Platform, Monitoring, Marketing)
- UI Components team is primarily focused on building our reusable Components for GitLab

[Find the product manager mapping to engineering teams in the product handbook](/handbook/product)

### Frontend domain experts

You have a question concerning the frontend for a product area? As a product manager you want to run a new idea by a frontend engineer? You want to learn more about how the current implementation works? You have specific frontend technology questions or have some idea/inputs?

**Wait no more, here are our frontend domain experts who can help you out**
- CI/CD + Security product - [Filipa Lacerda](/team/#FilipaLacerda)
- Discussion + MR View - [Fatih Acet](/team/#fatihacet)
- Portfolio Management + Geo - [Kushal Pandya](/team/#Kushal_Pandya)
- Web IDE - [Phil Hughes](/team/#iamphill)

Technical:
- Security - [Filipa Lacerda](/team/#FilipaLacerda)
- Testing - [Winnie Hellmann](/team/#winh)
- UI Components - [Clement Ho](/team/#ClemMakesApps)
- Webpack + Tooling - [Mike Greiling](/team/#mikegreiling)

**They are responsible for**
- Person to contact about a specific topic
- Analysing and Estimation off Deliverables
- Active Deliverable Creation (especially technical topics)
- Analysis of topics in that area (by example Research Linters for Security Checks)
- Active Bug tracking of bugs in that area

### Frontend team calls

The frontend team has scheduled weekly calls every Tuesday, before the company call. During this call, team members are encouraged to share
information that may be relevant to share with other members synchronously (Eg. new documentation change, new breaking changes added to `master`).

#### Frontend release kickoff

At the beginning of each release cycle also a frontend specific kickoff will be done in the team call. The idea is to share with your team members your tasks, find overlapping issues, share knowledge about implementations and have a global sense what we want to achieve this month as a team.

**Every frontend team member should prepare for this meeting:**
- Before the call - Check your deliverables in the planning sheet
  - Is it also assigned to you in the issue
  - Is the weight estimation correct?
  - Is the issue ready to get started? Anything missing in the description (default behaviour / error cases / etc)?
- Share your screen so everyone sees about which issue you are currently talking and can see also the issue content like screenshots,etc.
- Tell everyone in 2-3 sentences about your currently assigned deliverables, the task, the challenges behind it and your plan of implementation

### Frontend themed call

We started in January 2018, with adding a monthly theme to the first call of each month. The purpose of these themes is to add some
fun and quirkiness to our team calls (so that we can learn more about each other) but it shouldn't distract or derail into too much off-topic conversation.

**How does it work**
- Winner of the previous theme will determine the theme of the next month
- Theme will be announced a few weeks before the next month
- Everyone in the call should write down who they think is the winner on a piece of paper and reveal it all at once (to prevent voting bias) during the voting

| Date | Theme | Winner |
|---|---|---|
| 2018-01-09 | Most interesting hat | Jose Ivan Vargas |
| 2018-02-13 | Most interesting shirt/t-shirt (No GitLab swag) | Winnie |
| 2018-03-06 | Most interesting sunglasses | André |
| 2018-04-03 | Most peculiar trip souvenir | Eric Eastwood |
| 2018-05-08 | Grow the best grass or plant (preferably grass) | Lukas |
| 2018-06-04 | Most interesting sculpture from one piece of paper (maximum size Letter/A4) | Sam |
| 2018-07-10 | Ornament/Trinket/Thing-that-you-have, that says the most about you | Sam |
| 2018-08-07 | Most creative Tanuki in any medium | Eric Eastwood |
| 2018-09-04 | Best animal sketch/drawing | Winnie's wife |
| 2018-10-02 | Favorite mythical creature of your home country | ? |

### Frontend calendar

The frontend google calendar was created as a means of unifying and including team members on frontend related discussions.
Frontend meetings should be listed on the calendar unless there is a good reason not to.
Frontend engineers have the calendar permissions to create events on this calendar while GitLab team members have the permissions to add the frontend calendar to their calendar.

> Note: Due to a bug on Google calendar, team members are unable to find the calendar by searching.
Team members are recommended to go to the [frontend calendar link](https://calendar.google.com/calendar/b/1?cid=Z2l0bGFiLmNvbV83dHQ0bDA1NWg1MGRndWNpZDBidGg1ZGZsOEBncm91cC5jYWxlbmRhci5nb29nbGUuY29t)
on their browser to add this calendar to their calendar. This calendar is currently only available within GitLab and is not publicly accessible.

### Choosing something to work on

Prior starting your work on your `Deliverable` labeled issues take a look at the [`Next Patch Release ` issue list].

[`Next Patch Release ` issue list]: https://gitlab.com/groups/gitlab-org/issues?label_name[]=Next%20Patch%20Release&label_name[]=frontend

### Release planning

A few days after the 4th of each month, the Frontend manager goes through all the `frontend` labeled issues that have been assigned to the next milestone by the Product Manager and that have the `Deliverable` or `Stretch` label.

- Issues will be estimated by frontend managers and/or [domain experts](Frontend domain experts) with weights from 1-9 (see [table below](#weights))
- Then they will be assigned to frontend team members who will take ownership of the issue and are responsible for finishing the work in this cycle and also move it forward (by example show when things are blocked or review comments are going beyond the actual scope)

If, for any reason, an issue cannot be scheduled, a note should be added to inform everyone about that.
Obviously, when choosing which issue has to be rejected, the Frontend Engineering Manager can ask for more details to both the Product Manager that are responsible for the specific issue.

#### Weights

| Weight | Criteria | Examples |
| --- | --- | --- |
| 1 | 5 minute change, like changing a color, typo, etc. | [#41269] |
| 4 | Multiple Vue components need to be written or updated, communication with UX and backend team is necessary | [#41174], [#25388] |
| 9 | A feature that will take the whole month and needs full attention from the person doing it. | [#3559] |

[#41269]: https://gitlab.com/gitlab-org/gitlab-ce/issues/41269
[#3559]: https://gitlab.com/gitlab-org/gitlab-ee/issues/3559
[#25388]: https://gitlab.com/gitlab-org/gitlab-ce/issues/25388
[#41174]: https://gitlab.com/gitlab-org/gitlab-ce/issues/41174

### Frontend Marketing
{: #marketing}

The Frontend team is also responsible to support the marketing team with their activities on our website at [about.gitlab.com](/).
