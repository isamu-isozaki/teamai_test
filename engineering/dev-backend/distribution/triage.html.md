---
layout: markdown_page
title: "Distribution Team Triage"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Common links

* [Engineering Team Triage](/handbook/engineering/issue-triage/)

## Triaging Issues

### Terminologies

* Triaging: Triaging issues involves investigating and applying labels and milestones to issues.
* Partially Triaged issues: Issues are considered **partially** triaged if they have been assigned `for scheduling` or `awaiting feedback` labels.
* Fully Triaged issues: Issues are **fully** triaged when they have been assigned a Milestone, even if it is `Backlog`

Note: An issue that has been assigned to a user, but has no milestone, is not triaged, but is considered the responsibility of that user, and is not part of our triage queue at this time.

#### Issue severity

See the [CE documentation](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#severity-labels) for an explanation of the severity labels.

#### Label glossary

| Label | What it means | How to handle it |
| - | - | - |
| awaiting feedback | Information has been requested from the user | If no reply has been received in two weeks, the issue can be closed. |

### Resources

Issues for triaging can be identified using the following criteria:
  - They have no milestone
  - They have no assignee
  - They do **not** have either of the following labels applied:
    * `awaiting feedback`
    * `for scheduling`

Such issues can be listed using the [issues filter](https://gitlab.com/gitlab-org/omnibus-gitlab/issues?assignee_id=0&milestone_title=No+Milestone&scope=all&sort=created_date&state=opened)

### Process

Distribution team implements issue triaging on a rotating schedule, where each
person in the team gets assigned to do it for one week. This is done in the
order of joining the company. The process which one follows while on issue
triage duty can be summarized as follows

1. The previous team member on triage duty should have created and assigned the
   weekly meta issue to you at the end of their week. The issue title should be
   `Issue triage rotation week of <starting date>`
1. We follow the policy of closing an issue if it has been 14 days since
   `awaiting feedback` label was added and no response was received from
   submitter. Check out the issue list with `awaiting feedback` label for such
   issues and close them with the ["for issues with no reply"
   response](#for-issues-with-no-reply).
1. Check out the issues to be triaged and assign appropriate labels to them.
   While it is normal for some issues to demand a bit of research to get to the
   bottom, do keep in mind issue triaging need not end up in issue resolution.
   Triaging is intended only to identify and classify issues so that appropriate
   action can be taken on them, based on priority.
1. If an issue doesn't fall directly under the domain of omnibus-gitlab (for
   example, needs changes to gitlab-rails application), move the issue to the
   appropriate issue tracker and add the team label which may be the most
   appropriate. If you can't identify which project's tracker should the issue
   reside or which team's label should be applied, you can ask for Quality
   team's help for doing it by mentioning `@gitlab-org/issue-triage` in the
   comments.
1. If an issue doesn't deal with the code base or work flow of omnibus-gitlab
   project, but is more of a request for help for
   installing/configuring/troubleshooting a GitLab instance, close the issue
   using the ["problems not related to package installation and
   configuration" response](#for-problems-not-related-to-package-installation-and-configuration).
1. If an issue doesn't have all necessary information to successfully triage the
   issue, request the information using the ["issues that lack enough
   information" response](#for-issues-that-lack-enough-information) and
   add the `awaiting feedback` label.
1. If an issue couldn't be triaged in reasonable time, add the `needs investigation`
   label to it.
1. If an issue is identified as a valid one, make it partially triaged by
   assigning `For Scheduling` label so that it gets scheduled for one of the
   upcoming milestones (or even `Backlog` milestone). Also apply the severity
   labels as applicable.
1. Once an issue is triaged, either partially or fully, add the link to that
   issue as a comment to the meta issue. Preferably in the format of
   `<action> <url>` where `<action>` can be moved, closed, triaged, resolved or
   marked as needs investigation. This helps in keeping track of the issue
   triaged per week. Related issues feature of GitLab should not be used for
   this purpose as it generates an incorrect association between the issues.
1. Use the `/spend` quick action feature of GitLab to track the time you spent in
   triaging issues. There are no hard limits for this, but a reasonable amount
   of time would be 3 to 5 hours a week.
1. Since issues piling up is almost inevitable in any software project, we
   should try to bring down the issue count as much as possible. This mainly
   involves tackling existing backlog of untriaged issues. However, since
   untriaged issues of today will easily turn to be backlog for tomorrow, a
   reasonable ratio of old to new issues would be 60:40. This means, 60% of the
   issues that are triaged should be from the old pile while remaining 40%
   should be of the ones opened last week. This will help us keep volume of
   untriaged issues at bay.
1. During the next weekly meeting, inform the team about the triage week - link
   to the meta issue, number of issues triaged and time spent. And discuss if
   you think something should be changed regarding the process. Also, create a
   similar header for the next presenter as an agenda item for the next week's
   meeting in the meeting doc.
1. Close the meta issue.
1. Create a new meta issue for the next team member on triage duty, and assign
   them to it. The issue title should be `Issue triage rotation week of <starting
   date>`. Use the `Triage` template to fill in the description.

#### Response templates

Copy and paste into issues where appropriate

##### For problems not related to package installation and configuration

If someone is asking for support in the omnibus-gitlab project, point them to the correct place to look

```
Provided description seems to point to this issue not being related to this project. This can be the case when installation and `gitlab-ctl reconfigure` run went without issues, but your GitLab instance is still giving 500 error page with an error in the log.

For this reason, I will close this issue and you can check on how to find further help at the [GitLab website](/getting-help/).

/close
```

##### For issues that lack enough information

If someone opened a ticket without enough information, make sure they use the `Bug` template, and fill it in

```
We can't reproduce the issue with the information you provided here.

Can you please use our `Bug` template to help gather more details?

1. Click on the pencil icon near the issue title to edit the description
1. From the **Choose a template** drop down, select the **Bug** template
1. Read the template, and provide as much information as you can that we ask for
1. Click on the **Save changes** button to apply your changes.
1. Add a comment mentioning you updated the description.

/label ~"awaiting feedback"
```

##### For issues with no reply

If an issue has been labeled `awaiting feedback` for two weeks, and we haven't received a response, it can be closed

```
We haven't heard back from you, so we're going to go ahead and close the issue.

If you're still experiencing the problem, please re-open the issue and provide the requested information.

/close
```
