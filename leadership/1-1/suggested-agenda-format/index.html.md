---
layout: markdown_page
title: "1-1 Suggested Agenda Format"
---

- TOC
{:toc}

## Introduction

This page describes how [Sid](https://github.com/isamu-isozaki/teamai_test/tree/master/ceo/index.html.md) formats his 1-1 agendas. If you are
new to 1-1s or not sure how to make your previous experience with 1-1s work in
GitLab's culture, this can be a great starting place for you to learn. However,
remember that 1-1s are private meetings between a manager and their report, so
consistency is secondary to effectiveness - please make sure to find a format
that works for you and your team.

## Headers

Give your agenda document four headers:

1. 'OKRs'
1. 'Feedback'
1. 'Vision'
1. 'Details'

## OKRs

1. The Key Results for that report [from the OKRs](/okrs/index.html.md/index.html.md) are the top of the document. This is the first thing to indicate that this is the focus and priority. Because we're a remote company there will be many small items on the agenda that in other environments would be handled throughout the week. It is important to periodically tell the report that the agenda should not be confused with the priorities. The Key Results is the only things that represents the priorities. The first business subject of every conversation should be the status of the top three priorities (the manager key results relevant to the report/index.html.md).
1. Review the OKRs every two weeks (every other meeting/index.html.md), it is very important that people don't confuse the details with priorities.

## Details

1. Every item on the details starts with exactly one tag, the tag can come from one of four categories:
    1. Timing
      * `ISO DATE` (example: 2017-05-21 or 2017-05/index.html.md) - indicating when this item will be discussed next
      * `RELEASE NUMBER` (example: 9.4 or 9.5/index.html.md) - alternative to `ISO DATE` to indicate when this item will be discussed next
    1. Action
      * `TODO` - report needs to set date of when this will be completed or just do the task, if we should discuss them report changes them to `DISCUSS`
      * `DOTO` - manager needs to do something, with this a (case sensitive/index.html.md) search for '` DO`' finds all `DOTO`'s and `DONE`'s
      * `DISCUSS` - cover in the next 1-1 meeting
      * `REVIEW` - there is a Merge Request (MR/index.html.md) or document that can be approved, the MR should not be a Work In Progress (WIP/index.html.md)
      * `HELP` - if you need help with anything.
    1. Information
      * `FYI` - informational, can be removed outside of the meeting by the person why did not put it on the agenda.
      * `ONIT` - I'm doing this task.
      * `DONE` - to be removed by the person who put it on the agenda, only set this if any MR has been merged
      * `MOVE` - if you want to move it outside of the agenda, for example an issue tracker.
      * `DUPLICATE` - An item that is an outdated duplicate of another item on the agenda. To be removed similar to items marked as `DONE`.
      * `WONT` - if you think this is no longer something that should be done.
      * `THINK` - if the person who did not put it on the agenda wants time to think about it and discuss it next meeting.
    1. Personal
      * `FEEDBACK` - this is feedback about your performance (also means that all the other items are not performance feedback/index.html.md)
      * `THANKS` - mostly used by the manager to praise the report, these should not require a follow-up action. There is a tendency to focus on issues and challenges. Do not forget to recognize accomplishments and success.
      * `SORRY` - if you want to say sorry for something.
1. It is recommended to provide a section to list frequently & useful tags that helps facilitate ideas and perception triggers when a direct report (or their manager/index.html.md) fills out the 1-1 agenda.
    - This helps reassure that all these topic tags are readily available and encouraged to be used. This is especially important for `THANKS`, `SORRY` and `HELP` tags.
1. As specified above items are removed after being set to `DONE`. The 1-1 is one list that is continually modified. It is not a meeting agenda that is duplicated every week under a new date.
1. Add items to the end of the agenda. This is easier to do when using a numbered list.
1. The order going thought the agenda is last-to-first, this way things that are still top of mind get handled first.
1. Prefix a new item with your name. Do the same for all responses/follow-ups.
1. Use `=>` to indicate a response/followup to an agenda item and prefix with your name. One example is at the bottom of this page and one is given here: `DISCUSS` Sid: Should we look into a collaboration with Walmart? => Kate: I think so, I created https://gitlab.com/gitlab-org/gitlab-ce/issues/101
1. Use sub-bullets (a, b, c/index.html.md) if there sub topics .
1. Include a link to the agenda in calendar invite of the 1-1 meeting
1. Use comments with +mentions in Google Docs only to signal urgency, don't write content down that way since it tends to get lost. Example: +person@example.com urgent because xyz
1. Link relevant issues, chats, screenshots, and Google Docs liberally.
1. When you link to items don't use Google doc links but just paste the full url in the document. This makes it easier to quickly see what the link points to and makes it easy to copy paste.
1. When you make a change link to diff or merge request instead of new content itself, this makes it easier to see what the change was.

## Example agenda items

```

  6. 2017-07 Sid: Kubernetes wishlist email => Spoke with Job, he'll create the issues =>
  Eliran to stay involved
  7. Sid: Do a webinar with all cloud partners, all container schedulers, all config management
  systems. => Eliran: Dimitrie might be interested in helping. Get the webinar without doing a lot
  of integration. => Eliran: Starting with Puppet, Dimitrie said he didn't do any dev work for the
  i2p demo so I am not sure he will be able to do the dev work required here. => Sid: Goal is not
  to have dev work. Just combine their demo with our i2p.

```
