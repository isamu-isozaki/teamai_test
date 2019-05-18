---
layout: markdown_page
title: "GitLab Communication"
extra_js:
  - libs/moment.min.js
  - libs/moment-timezone-with-data.min.js
  - team-call.js
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Introduction

We're a **distributed**, **all-remote** company where people work remotely without missing out.
For this, we use **asynchronous communication** and are as open as we can be by communicating through public issues, [chat channels](/handbook/communication/chat),
and placing an emphasis on ensuring that conclusions of offline conversations are written down.
These communication guidelines are meant to facilitate smooth communication in an ever-growing, all-remote company.

## External communication

Please see our [social media guidelines](/handbook/marketing/social-media-guidelines/).

## Everything starts with an issue

1. Always **create** an issue for things you work on. If it is worth spending time on, it is worth creating an issue since that enables other people to learn and help. You can always edit the description or close it when the problem changed to something different or was solved.
1. If a user suggests an enhancement, try and find an existing issue that addresses their concern, or create a new one. Ask if they'd like to elaborate on their idea in one of these issues.
1. **Double link** issues with related conversations. E.g. if there’s a ZenDesk ticket that causes you to open a GitLab.com issue, make sure to document the issue link in the ZenDesk ticket and vice versa. And when closing the issue, include reason or response from ZenDesk. Another example is to add "Report: " lines to the issue description with links to relevant issues and feature requests. When done add a comment to relevant issues (and close them if you are responsible for reporting back, or re-assign if you are not). This prevents internal confusion and us failing to report back to the reporters.
1. If two issues are related, **crosslink** them (a link from each issue to the other one). Put the link at the top of each issue's description with a short mention of the relationship (Report, etc.). If there are more than 2 issues, use one issue as the central one and crosslink all issues to this one. Please, also crosslink between ZenDesk and GitLab issues.
1. After a discussion about a feature **update the issue description** with the consensus or final conclusions. This makes it much easier to see the current state of an issue for everyone involved in the implementation and prevents confusion and discussion later on.
1. Submit the **smallest** item of work that makes sense. When creating an issue describe the smallest fix possible, put suggestions for enhancements in separate issues and link them. If you're new to GitLab and are writing documentation or instructions, submit your first merge request for at most 20 lines.
1. Do not leave issues open for a long time, issues should be **actionable** and realistic. If you are assigned to an issue but don't have time to work on it, assign it to someone else.
1. Make a conscious effort to **prioritize** your work. The priority of items depends on multiple factors: Is someone waiting for the answer? What is the impact if you delay it? How many people does it affect, etc.? This is detailed in [Engineering Workflow](/handbook/engineering/workflow).
1. Use the public issue trackers on GitLab.com for everything since [we work out in the open](/2015/08/03/almost-everything-we-do-is-now-open/). Issue trackers that can be found on the relevant page in the handbook and in the projects under [the gitlab-com group](https://gitlab.com/gitlab-com/).
1. Pick issues from the current [milestone](https://gitlab.com/groups/gitlab-org/milestones).
1. We try not to assign issues to people but to have people **pick issues** in a milestone themselves.
1. Assign an issue to yourself as soon as you start to work on it, but not before that time. If you complete part of an issue and need someone else to take the next step, **re-assign** the issue to that person.
1. When re-assigning an issue, make sure that the issue description contains the latest information. The issue description should be the **single source of truth**.
1. When working on an issue, **ask for feedback** from your peers. For example, if you're a designer and you propose a design, ping a fellow designer to review your work. If they approve, you can move it to the next step. If they suggest changes, you get the opportunity to improve your design. This promotes collaboration and advances everyone's skills.
1. We keep our **promises** and do not make external promises without internal agreement.
1. Do not close an issue until it is [**done**](https://docs.gitlab.com/ee/development/contributing/merge_request_workflow.html#definition-of-done).
1. When **closing** an issue leave a comment explaining why you are closing the issue.

## Implement it with a merge request

Merge request guidelines for all contributors are described in our [Contribution
guide](https://docs.gitlab.com/ee/development/contributing/merge_request_workflow.html#merge-request-guidelines).

Code review guidelines for reviewers and maintainers are described in our [Code
Review Guidelines][code-review-guidelines].

Following are additional guidelines for GitLab Inc. team
members:

1. Even when something is not done, share it internally so people can comment
  early and prevent rework. Create a **[Work In
  Progress](/2016/01/08/feature-highlight-wip/)** merge request so it is not merged by accident.
1. If any followup actions are required on the issue after the merge request is
  merged (like reporting back to any customers or writing documentation), avoid
  auto closing it.
1. When _you_ are done with your merge request, remove the "WIP" prefix and
  follow the [Code Review Guidelines][code-review-guidelines].
1. You can still make changes based on feedback of course, but by removing the
  "WIP" prefix it clarifies that the main body of work has been completed.

[code-review-guidelines]: https://docs.gitlab.com/ee/development/code_review.html

## Internal Communication

1. All written communication happens in English, even when sent one on one, because sometimes you need to forward an email or chat.
1. Use **asynchronous communication** when possible (issues and email instead of chat).
1. Issues are preferred over email, email is preferred over chat, announcements happen on the company call agenda, and [people should be able to do their work without getting interrupted by chat](https://m.signalvnoise.com/is-group-chat-making-you-sweat-744659addf7d#.21t7089jk).
1. To use email instead of chat it is OK to send an _internal_ email that contains only a short message, similar as you would use in chat. Save time by not including a salutation like 'Hi Emma,' and first write the subject of the email which you copy and paste into the body. You are not expected to be available all the time. It is perfectly fine not to respond to emails and chat mentions until your planned work hours.
1. Sometimes synchronous communication is the better option, but do not default to it. For example, a video call can clear things up quickly when you are blocked. See the [guidelines on video chats](#video-calls) for more detail.
1. It is very OK to ask as many questions as you have, but ask them so many people can answer them and many people see the answer (so use issues or public chat channels instead of private messages or one-on-one emails) and make sure you  document the answers.
1. If you mention something (a merge request, issue, commit, webpage, comment, etc.) please include a link to it.
1. All company data should be **shareable** by default. Don't use a local text file but rather leave comments on an issue.
1. When someone asks something, give back a deadline or that you did it. Answers like: 'will do', 'OK', 'it is on my todo list' are not helpful. If it is small is better to spend 2 minutes and do the tasks so the other person can mentally forget about it. If it is large you need to figure out when you'll do it, by returning that information the other person might decide to solve it in another way if it takes too long.
1. It is OK to bring an issue to someone's attention with a CC ("cc @user"), but CCs alone are not enough if specific action is needed from someone. The mentioned user may read the issue and take no further action. If you need something, please explicitly communicate your need along with @ mentioning who you need it from.
1. Avoid creating private groups for internal discussions:
    1. It's disturbing (all user in the group get notified for each message).
    1. It's not searchable.
    1. It's not shareable: there is no way to add people in the group (and this often leads to multiple groups creation).
    1. They don't have a subject, so everyone has to remember the topic of each private group based on the participants, or open the group again to read the content.
    1. History is lost when leaving the group.
1. It is perfectly fine to create a channel, even for a single customer meeting. These channels should be named "<customer>-internal" to indicate their "internal" nature (not shared with customers).

## Email

1. Send one email per subject as multiple items in one email will cause delays (have to respond to everything) or misses (forgot one of the items).
1. Always reply to emails by replying to all, even when no action is needed. This lets the other person know that you received it. A thread is done when there is a single word reply, such as OK, thanks, or done.
1. If you forward an email without other comments please add FYI (for your information), FYA (for your action), or FYJ (for your judgment). If you forward an external request with FYJ it just means the person who forwarded it will not follow up on the request and expects you to decide if you should follow up or not.
1. Email forwarding rules are specified in the shared _Email, Slack, and GitLab Groups and Aliases_ Google Doc accessible only to people in the company. If you want to be added or removed from an internal alias (for example, "sales@gitlab.com"), change a rule, or add a forwarding email alias, please [suggest an edit](https://support.google.com/docs/answer/6033474?hl=en) in the doc.
1. Emails are asynchronous, for example, if your manager emails you on a weekend it is fine to reply during the workweek.
1. If an email is or has become **urgent** feel free to ping people via chat referencing the subject of the email.

## Chat

1. If you use chat, please use a public channel and mention the person or group you want to reach. This ensures it is easy for other people to chime in, involve other people if needed, and learn from whatever is discussed.
1. If you use chat and plan to message 3 or more people, we recommend to create a chat channel for customer/issue/project/problem/partnership.
1. If you're only referring to someone, but don't actually need their attention, and want to spare them from getting notified, spell out their name normally without `@` mentioning them.
1. If the subject is of value to the wider community, consider commenting on an existing issue or opening a new [issue](#everything-starts-with-an-issue) instead.
1. Despite the instantaneous nature of chat, it should be considered asynchronous communication. Don't expect an instantaneous response; you have no idea what the other person is doing.
1. If you must send a private message, don't start a conversation with "Hi" or "Hey" as that interrupts their work without communicating anything. If you have a quick question, just ask the question directly and the person will respond asynchronously. If you truly need to have a synchronous communication, then start by asking for that explicitly, while mentioning the subject. e.g. "I'm having trouble understanding issue #x, can we talk about it quickly?".
1. Unless you're in an active chat, don't break up a topic into multiple messages as each one will result in a notification which can be disruptive. Use [threads](https://get.slack.help/hc/en-us/articles/115000769927-Message-threads) if you want to provide extra info to the question/comment you posted. Especially in channels like `#questions` are threads very valuable to keep conversations about a certain question together.
1. Because we work globally, you may receive chat mentions at any time of day. Please consider enabling [Slack's Do not disturb functionality](/handbook/tools-and-tips/#do-not-disturb-hours) so you don't get interrupted, for example, in your evenings.
1. Do not feel obligated to respond to chat messages when you are not working.
1. Feel free to send a colleague a link to these guidelines if the communication in Slack should be done **asynchronously**.
1. If you are having a hard time keeping up with chat messages, you can update your preferences to have Slack email you all notifications. To change the setting, go to `Preferences > Notifications > When I'm not active on desktop...` and "send me email notifications".
1. **Please avoid using @here or @channel unless this is about something urgent and important.** In chat try to keep the use of keywords that mention the whole channel to a minimum. They should only be used for pings that are both urgent and important, not just important. By overusing channel mentions you make it harder to respond to personal mentions in a timely manner since people get pinged too frequently. If something is urgent and important:
   * Use `@here` to notify all currently _active_ members in the room.  Please only use `@here` if the message is important _and_ urgent.
   * Use `@channel` to notify _ALL_ members in the room, irrespective of away status. Please only use `@here` if the message is important _and_ urgent.
1. If something is important but not urgent - like complimenting or encouraging the entire team - use email or post in the channel without `@`-mentioning the team.
1. If you agree in a chat to start a video call (typically by asking "Call?") the person that didn't leave the last comment starts the call. So either respond to the "Call?" request with a video link or say "Yes" and let the other person start it. Don't say "Yes" and start a call 5 seconds later since it is likely you'll both be creating a video call link at the same time.
1. The usage of ChatBots for integrations can sometimes depend upon the name of the chat room. You should consult the room about such integrations before changing the name of commonly used / popular rooms in order to avoid inadvertently breaking integrations.
1. If you are aware that your teammate is on vacation, avoid mentioning them in a high volume channel. It will be difficult to find the information or question when they return. If you need to ensure they refer back to the thread, ensure to send them a link to the relevant Slack message through a direct message.
1. It's not rude to leave a channel. When you're no longer interested in the conversations happening in a channel, feel free to leave it so it won't distract you anymore.
1. Learn about [common channels and channel-naming conventions](/handbook/communication/chat).

## Google Docs

1. Never use a Google Doc / Presentations for something non-confidential that has to end up on the website or the **handbook**. Work on these edits via commits to a merge request. Then link to the merge request or diff to present the change to people. This prevents a duplication of effort and/or an out of date handbook.
1. If you _do_ need a Google Doc, create one with your company G Suite (formerly Google
Apps) account. By default, share it with the whole company using the _Anyone at GitLab can find and access_ link sharing permission
and the _Anyone within GitLab can edit_ access permission (preferred) or the _Anyone within GitLab can comment_ access permission.
Easily do this by creating Google Docs within a Shared Folder in Google Drive.
1. If you have content in a Google doc that is later moved to the website or handbook, [deprecate the Google doc](#how-to-deprecate-a-google-doc).
1. When referring to a Google Doc or folder on the Google Drive in the handbook, refrain from directly linking it. Instead, indicate the name of the doc. If you link the url people from outside the organization can request access, creating workload and the potential for mistakes.
(In the past, linking a Google Doc has led to inadvertently opening the sharing settings beyond what was intended.)
This also helps prevent spam from people outside GitLab requesting access to a doc when clicking its link.
1. If you are having trouble finding a shared Google Doc, make sure you [Search &lt;your domain&gt;](https://support.google.com/a/answer/3187967?hl=en) in Google Drive.
1. In our handbook, if you find yourself wondering whether it is better to provide a public link to a Google Doc vs. writing out the content on the website, use the following guideline: Is this document frequently adapted / customized? If yes, then provide a link, making sure that the document can be _commented on_ by _anyone_ with the link. For instance, this is how we share our employment [contracts](/handbook/contracts/). If the document is rarely customized, then provide the content directly on the site and deprecate the Google Doc.
1. If you want to quickly find where a team member's cursor is in a Google Doc, click their icon at the top of the document and the app will jump you to the current location. This works in Sheets and Presentations as well.

### How to deprecate a Google doc

1. Add 'Deprecated: ' to the start of the title.
1. Remove the content you moved.
1. Add a link to the the new location at the beginning of the doc/first slide/first tab.
1. Add a link to the merge request or commit that moved it (if applicable).

## Presentations

1. All presentations are made in Google Slides using our template named 'GitLab-Deck-Template-Light'.
1. The title of every slide should be the message you want the audience to take away, not the subject matter. So use 'Our revenue more than doubled' instead of 'Revenue growth'.

## Say Thanks

1. Thank people that did a great job in our "Thanks" chat channel. If someone is
a team member just @ mention them. If multiple people were working on something
try mentioning each person by "@name". "Thanks everyone" does not say much.
1. To thank someone who is not a team member, mention your manager, our People Ops Coordinator, the name of the person, a quirky gift
and link to their work. For example, "@manager, @peopleopscoordinator: Joe deserves a lawnmower for _link_".
With your manager's blessing, the People Ops Coordinator will approach the person in question for their address saying we want to send
some swag. We'll ship it in gift wrap with "Thanks for your great work on _link_, love
from @gitlab".
1. Don't thank the CEO or other executives for something that the company paid for, thank GitLab instead.
1. Don't thank people publicly for working outside of their scheduled work hours. We want to minimize the pressure to do so.

## Not sure where to go?

If there is something that you want to discuss, but you do not feel that it is
a reasonable option to discuss with either your manager or CEO, then you can reach
out to any of the other C-level GitLabbers or our board member Bruce Armstrong.

## Company Call

1. Schedule
   * PST: <span id="main-PST"></span>
   * UTC: <span id="main-UTC"></span>
   * <span id="main-abbr"></span>: <span id="main-USER"></span>
1. APAC schedule
   * PST: <span id="apac-PST"></span>
   * UTC: <span id="apac-UTC"></span>
   * <span id="apac-abbr"></span>: <span id="apac-USER"></span>
1. Everyone at GitLab is invited to the company call.
1. We also have a company call for GitLabbers in the APAC region. This call will also be recorded so the rest of the company can see what their colleagues have been up to! Everyone is encouraged to join this call as well, but it is not mandatory.
1. Every last Friday of the month we have an AMA to talk about anything the people at our company are thinking about.
1. We use [Zoom](https://gitlab.zoom.us) for the call since Google Hangouts is capped at 15 people (please be sure to mute your microphone). If using the Zoom web app, you can go to settings and check always mute microphone when joining a meeting.
1. The link is in the calendar invite and also listed at the top of the company call agenda Google Doc called _Company Call Agenda_.
1. The call is recorded automatically, and all calls are transferred every hour to a Google Drive folder called "GitLab Videos". There is a subfolder called "GitLab Company Call", which is accessible to all users with a GitLab.com e-mail account.
1. We start on time and do not wait for people.
1. The person who has the first item on the agenda starts the call.
1. If you are unable to attend just add your name to the company call agenda as "Not attending".
1. We start by discussing the subjects that are on the agenda for today.
   * Everyone is free to add subjects. Please start with your name and be sure to link to an issue, merge request, or commit if it is relevant.
   * When done with a point mention the subject of the next item and hand over to the next person.
   * When someone passes the call to you, no need to say, “Can you hear me?” Just begin talking. If we can’t hear you, we’ll let you know.
1. After the general announcements, attendees share their personal interests by adding their name to the schedule or by discussing in a mixer call. The schedule is as follows:
  * Monday: Any topic
  * Tuesday: [Mixer Calls](/handbook/communication/#mixer-calls), where we split off into smaller groups to discuss what we have been up to. No need to add yourself to the agenda on this day.
  * Wednesday: [Breakout Calls](https://docs.google.com/spreadsheets/d/1M-6NjK8_gAqcU1BehQVkKuDa1Ua2hTGBy8TuEDXHh3g/edit?usp=sharing)
  * Thursday: [Mixer Calls](/handbook/communication/#mixer-calls), where we split off into smaller groups to discuss what we have been up to. No need to add yourself to the agenda on this day.
  * Friday: Any topic
1. Please add your name to the agenda at least 15 minutes before the company call is scheduled to start. We encourage 15-20 people to share an update of about a minute to leave time for all listed on the agenda. If you see that a particular day is congested and you have already shared over the last 2 weeks, please consider moving your name to a later week.
1. It is OK to talk over people or interrupt people to ask questions, cheer for them or show your compassion. This encourages more conversation and feedback in the call. Also see the interruption item in [video calls](#video-calls).
1. Please look if the person you hand over to is present in the participant list so you don't hand over to someone who is not present.
1. The last person wishes everyone a good day.
1. Even if you cannot join the call, consider reviewing the recorded call or at minimum read through the agenda and the links from there. We often use the company call to make announcements or discuss changes in processes, so make sure to catch up on the news if you have missed a company call (or more).
1. If you are scheduling a meeting, avoid scheduling during the company call so that meeting attendees do not need to choose between your meeting and the company call. As a remote workforce, the company call is an important part of our culture.

## Mixer Calls

### Groups

We split into small groups of around eight on Tuesdays and Thursday [Company Call](/handbook/communication/#company-call), using Zoom's [Breakout Rooms](https://support.zoom.us/hc/en-us/articles/115005769646-Participating-in-Breakout-Rooms) feature. The groups are randomly assigned based on the participants in the Company Call.

### Call Structure

These calls are unstructured to allow for natural interaction, but everyone should get a chance to share at least once.

It helps to pause slightly between talking about different topics to allow for discussion.

If you are unsure of who should start or speak next, follow the order listed in Zoom.

Prompts for things you might share:

- Hobbies and interests.
- What you've been up to recently.
- Things you're looking forward to.
- Sports and wellness.
- Cooking, entertaining, and creative projects.
- Travel, kids, family, and pets.
- Music, books, TV & movies, and video/board games.

### Setting up a Mixer Call

The calls take place using the People Ops zoom account, which has Breakout Rooms enabled.

After the announcements, the host will [start the Breakout Rooms](https://support.zoom.us/hc/en-us/articles/206476313-Managing-Video-Breakout-Rooms) from the Zoom interface, choosing a number of rooms that averages 8-9 people per room.

Anyone who joins late or accidentally leaves their Breakout can be manually assigned to a room.

### Breakout Call

On Wednesdays we breakout into smaller [predesignated groups](https://docs.google.com/spreadsheets/d/1M-6NjK8_gAqcU1BehQVkKuDa1Ua2hTGBy8TuEDXHh3g/edit?usp=sharing) to discuss what we have been up to. These calls occur immediately following the standard company call updates. The breakout calls will be held in separate Zoom URLs correlating to the group that each team member is assigned.

## Release Retrospectives and Kickoffs
{: #kickoffs}

After GitLab releases a new version on the 22nd of each month, we have a
30-minute call a few days later reflecting on what could have been
better:

1. What went well this month?
1. What went wrong this month?
1. What could we have done better?

We spend the first part of the retrospective meeting reviewing the action
items from the previous month.

On the 8th of each month (or the next business day), we have a kickoff meeting
for the version that will be released in the following month. The product team and other leads will have already had
discussions on what should be prioritized for that release. The purpose of this kickoff is
to get everyone on the same page and to invite comments.

Both the retrospectives and kickoffs are live streamed (and posted) to the [GitLab YouTube channel](https://www.youtube.com/gitlab).

## Random Chat and Room
{: #random-room}

1. The [#random](https://gitlab.slack.com/archives/random) chat channel is your go-to place to share random ideas, pictures, articles, and more. It's a great channel to check out when you need a mental break.
1. Come hang out any time in the **random room**, an open Google Hangout video chat where anyone with a GitLab email address can come and leave as they please. The link is in the description of the `#random` chat channel; consider bookmarking it. This room is open for all and should be distinct from the [Coffee Break Calls](/culture/remote-only/#coffee-break-calls), which are 1x1 conversations between teammates.

## Scheduling Meetings

1. If you want to ask GitLabbers if they are available for an event please send a calendar invite with Google Calendar with your Google GitLab account to their Google GitLab account. This makes it easier for people to check availability and to put on their calendar. It automatically shows up on calendars even when the email is not opened. It is easier to signal presence and to see the status of everyone. Please respond quickly to invites so people can make plans.
1. Every scheduled meeting should either have a Google Presentation (for example for functional updates that don't require participation) or a Google Doc (for most meetings) linked. If it is a Google Doc it should have an agenda, including any preparation materials (can be a presentation). Put the agenda in a Google Doc that has edits rights for all participants (including people not part of GitLab Inc.). Link the Google Doc from the meeting invite. Take notes of the points and todos during the meeting. Nobody wants to write up a meeting after the fact and this helps to structure the thought process and everyone can contribute. Being able to structure conclusions and follow up actions in realtime makes a video call more effective than an in-person meeting. If it is important enough to schedule a meeting it is important enough to have a Doc linked. If we want to be on the same page we should be looking at that page.
1. If you want to check if a team member is available for an outside meeting, create a calendar appointment and invite the team member only after they respond yes. Then invite outside people.
1. When scheduling a call with multiple people, invite them using a Google Calendar that is your own, or one specific to the people joining, so the calendar item
doesn't unnecessarily appear on other people's calendars.
1. If you want to move a meeting just move the calendar appointment instead of reaching out via other channels. Note the change at the top of the description.
1. Please click 'Guests can modify event' so people can update the time in the calendar instead of having to reach out via other channels. You can configure this to be checked by default under [Event Settings](https://calendar.google.com/calendar/r/settings).)
1. When scheduling a meeting we value people's time and prefer the "speedy meetings" setting in our Google Calendar. This gives us meetings of, for example, 25 or 50  minutes leaving some time to write notes etc before continuing to our next call or meeting. (This setting can be found under the calendar Settings menu at "default event duration")
1. When creating a calendar event that will be used company wide, please place it on the GitLab Team Meetings Calendar. That way the event is easily located by all individuals.
1. When you need to cancel a meeting, make sure to delete/decline the meeting and choose the option **Delete & update guests** to make sure everyone knows you can't attend and don't wait for you.
1. If you want to schedule a meeting with a person not on the team please use [Calendly](handbook/tools-and-tips/#calendly). Use Google Calendar directly if scheduling with a GitLabber.

## Indicating Availability

Indicate your availability by updating your own calendar using Google's ["out of office"](https://www.theverge.com/2018/6/27/17510656/google-calendar-out-of-office-option) feature and include the dates you plan to be away in your automated response. Note that this feature will automatically decline any meeting invitations during the time frame you select.

1. Put your planned away time including holidays, vacation, travel time, and other leave in your own calendar. Please see [Communicating your time off](/handbook/paid-time-off#communicating-your-time-off) for more.
1. Set your working hours in your Google Calendar settings.

## Video Calls

1. Use video calls if you find yourself going back and forth in an issue/via email
or over chat. Rule of thumb: if you have gone back and forth 3 times, it's time
for a video call.
1. Having pets, children, significant others, friends, and family visible during
video chats is encouraged. If they are human, ask them to wave at your remote
team member to say "Hi".
1. We prefer [Zoom](https://gitlab.zoom.us/).
1. For meetings that are scheduled via calendar there is automatically a Google Hangouts URL added. This is the meeting place. Having a URL in advance is much more reliable than trying to call via Hangouts as the meeting start.
1. Google Calendar also has a [Zoom plugin](https://chrome.google.com/webstore/detail/zoom-scheduler/kgjfgplpablkjnlkjmjdecgdpfankdle?hl=en-US) where you can easily add a Zoom link for a video call to the invite
1. For meetings that are scheduled with Zoom:
   1. Make sure to take out the Google Hangouts link to avoid confusion.
   1. If you need more privileges on Zoom (longer meeting times, more people in the meeting, etc.), please contact People Ops as described [specifically for Zoom](/handbook/tools-and-tips/#sts=Zoom).
   1. Note that if you select to record meetings to the cloud (setting within Zoom), they will be automatically placed in the GitLab Videos folder in Google Drive on an hourly basis. You can find these videos in Google Drive by entering in the search bar: `title:"GitLab Videos" source:domain`.
   1. Note also that after a meeting ends, Zoom may take some time to process the recording before it is actually available. The sync to Google Drive happens on the hour mark, so if the recording is not available, it may take another hour to be transferred.
   1. If you are sharing your screen, chat is hidden by default, but you can get it back by clicking on the `...` menu and selecting `Chat`.
1. Use a headset with a microphone, [Apple Earpods](https://www.apple.com/shop/accessories/all-accessories/headphones-speakers) are great. Do not use computer speakers, they cause an echo. Do not use your computer microphone, it accentuates background noise. If you want to use your [Bose headphones](https://www.bose.com/en_us/products/headphones/noise_cancelling_headphones.html) that is fine but please ensure the microphone is active.
1. Consider using a utility to easily mute/unmute yourself, see [Shush](/handbook/tools-and-tips/#shush) in the tools section.
1. In video calls everyone should own a camera and a headset, even when they are in the same room. This helps seeing and hearing the person that is talking. It also allows people to easily talk and mute themselves. Using a headset also prevents echo. You wouldn't share an office seat together, so don't share your virtual seat at the table.
1. Please speak up asap when someone on the call hasn't muted their mic to avoid disturbances to the person speaking.
1. We start on time and do not wait for people. People are expected to join no later than the scheduled minute of the meeting (before :01 if it is scheduled for :00). The question 'is everyone here' is not needed.
1. It feels rude in video calls to interrupt people. This is because the latency causes you to talk over the speaker for longer than during an in-person meeting. We should not be discouraged by this, the questions and context provided by interruptions are valuable. This is a situation where we have to do something counter-intuitive to make all-remote meetings work. In GitLab everyone is encouraged to interrupt the speaker in a video call to ask a question or offer context. We want everyone to contribute instead of a monologue. Just like in-person meetings be cognizant of when, who, and how you interrupt, we don't want [manterrupting](http://time.com/3666135/sheryl-sandberg-talking-while-female-manterruptions/).
1. We end on the scheduled time. It might feel rude to end a meeting, but you're actually allowing all attendees to be on time for their next meeting.

## Google Calendar

We recommend you set your Google calendar access permissions to 'Make available for GitLab - See all event details'. Consider marking the following appointments as 'Private':

- Personal appointments.
- Confidential & sensitive meetings with third-parties outside of GitLab.
- 1-1 performance or evaluation meetings.
- Meetings on organizational changes.

There are several benefits and reasons to sharing your calendar with everyone at GitLab:

1. Transparency is one of our values and sharing what you work on is in line with our message of "be open about as many things as possible".
1. Due to our timezone differences, there are small windows of time where our availabilities overlap. If other members need to schedule a new meeting, seeing the details of recurring meetings (such as 1-1s) will allow for more flexibility in scheduling without needing to wait for a confirmation from the team member. This speaks to our value to be more efficient.

![Google Calendar - make calendar available setting](/images/handbook/tools-and-tips/google-calendar-share.png)

If you add blocks of time spent on recurring tasks to your Google Calendar to remind yourself to do things (e.g. "Check Google Analytics"), consider marking yourself "Free" for those events so that coworkers know they may schedule a meeting during that time if they can't find another convenient time.

## User Communication Guidelines

1. Keep conversations positive, friendly, real, and productive while adding value.
1. If you make a mistake, admit it. Be upfront and be quick with your correction. If you're posting to a blog, you may choose to modify an earlier post. Just make it clear that you have done so.
1. There can be a fine line between healthy debate and incendiary reaction. Try to frame what you write to invite differing points of view without inflaming others. You don’t need to respond to every criticism or barb. Be careful and considerate.
1. Answer questions, thank people even if it’s just a few words. Make it a two way conversation.
1. Appreciate suggestions and feedback.
1. Don't make promises that you can't keep.
1. Guide users who ask for help or give a suggestion and share links. [Improving Open Development for Everyone](/2015/12/16/improving-open-development-for-everyone/), [Types of requests](/2014/12/08/explaining-gitlab-bugs/).
1. When facing negative comment, respond patiently and treat every user as an individual, people with the strongest opinions can turn into [the strongest supporters](/2015/05/20/gitlab-gitorious-free-software/).

## Writing Style Guidelines

1. {: #american-english} At GitLab, we use American English as the standard written language.
1. Do not use rich text, it makes it hard to copy/paste. Use [Markdown](/handbook/product/technical-writing/markdown-guide) for things stored in git. In Google Docs use "Normal text" using the style/heading/formatting dropdown and paste without formatting.
1. Don't use ALL CAPS because if [feels like shouting](http://netiquette.wikia.com/wiki/Rule_number_2_-_Do_not_use_all_caps).
1. We use Unix style (lf) line endings, not Windows style (crlf), please ensure `*.md text eol=lf` is set in the repository's `.gitattributes` and run `git config --global core.autocrlf input` on your client.
1. Do not create links like "here" or "click here". All links should have relevant anchor text that describes what they link to, such as: "GitLab CI source installation documentation". Using [meaningful links](https://www.futurehosting.com/blog/links-should-have-meaningful-anchor-text-heres-why/){:rel="nofollow noindex"} is important to both search engine crawlers (SEO) and people with accessibility issues.
1. Always use [ISO dates](https://en.wikipedia.org/wiki/ISO_8601#Calendar_dates) in all writing and legal documents since other formats [lead to online confusion](http://xkcd.com/1179/). Use `yyyy-mm-dd`, for example 2015-04-13, and never 04-13-2015, 13-04-2015, 2015/04/13, nor April 13, 2015. Even if you use a unambiguous alternative format it is still harder to search for a date, sort on a date, and for other team members to know we use the iso standard. For quarters use 2018-Q3.
1. Remember that not everyone is working in the same timezone; what may be morning for you is evening for someone else. Try to say 3 hours ago or 4 hours from now, or use a timestamp, including a timezone reference.
1. For engineering (for example production postmortems) we use UTC as the timezone. For all other uses we use Pacific time since we are a San Francisco based company. Please refer to time as '9:00 Pacific' and not PST since that is ambiguous during daylight savings.
1. If you have multiple points in a comment or email, please number them to make replies easier.
1. When you reference an issue, merge request, comment, commit, page, doc, etc. and you have the URL available please paste that in.
1. In making URLs, always prefer hyphens to underscores, and always use lowercase.
1. The community includes users, contributors, core team members, customers, people working for GitLab Inc., and friends of GitLab. If you want to refer to "people not working for GitLab Inc." just say that and don't use the word community. If you want to refer to people working for GitLab Inc. you can also use "the GitLab Inc. team" but don't use the "GitLab Inc. employees".
1. When we refer to the GitLab community excluding GitLabbers please say "wider community" instead of "community".
1. All people working for GitLab (the company) are the [GitLab team](/team). We also have the [Core team](/core-team) that consists of volunteers.
1. Please always refer to GitLab Inc. people as GitLabbers, not employees.
1. Use [inclusive and gender-neutral language](https://techwhirl.com/gender-neutral-technical-writing/) in all writing.
1. Always write GitLab with a capitalized G and L, even when writing GitLab.com.
1. Always capitalize the names of GitLab [features](/features).
1. Do not use a hyphen when writing the term "open source."
1. Monetary amounts shouldn't have one digit, so prefer $19.90 to $19.9.
1. If an email needs a response, write the answer at the top of it.
1. Use the future version of words, just like we don't write internet with a capital letter anymore. We write frontend and webhook without a hyphen or space.
1. Our homepage is / (with the `about.` and with `https`).
1. Try to use the [active voice](https://writing.wisc.edu/Handbook/CCS_activevoice.html) whenever possible.
1. Refer to environments that are installed and run "on-premises" by the end-user as "self-managed."
1. If you use headers, properly format them (`##` in Markdown, "Heading 2" in Google docs); start at the second header level because header level 1 is for titles. Do not end headers with a colon.
1. Always use an [Oxford comma](https://en.wikipedia.org/wiki/Serial_comma) in lists of three or more terms.
1. Always use a single space between sentences rather than two.
1. Read our [Documentation Styleguide](https://docs.gitlab.com/ee/development/doc_styleguide.html) for more information when writing documentation.
1. Do not use acronyms when you can avoid it as you can't assume people know what you are talking about. Example: instead of `MR`, write `merge request`.
1. We segment our customers/prospects into 4 segments [Strategic, Large, Mid-Market and Small Medium Business (SMB)](/handbook/business-ops/#segmentation).

## Situation-Complication-Implication-Position-Action-Benefit (SCIPAB)

Mandel Communications refers to SCIPAB at the "surefire, six-step method for starting any conversation or presentation."  When you only have a few minutes to present your case or grab your listeners attention, this six-step process can help you communicate better and faster.

* Situation - Expresses the current state for discussion.
* Complication - Summarizes the critical issues, challenges or opportunities.
* Implication - Provides insight into the consequences that will be a result of if the Complications are not addressed.
* Position - Notes the presenter's opinion on the necessary changes which should be made.
* Action - Defines the expectations of the target audience/listeners.
* Benefit - Clearly concludes how the Position and Action sections will address the Complications.
This method can be used in presentations, emails and everyday conversations.
Example - The Management team asking for time to resolve a problem
* S - The failure rate last year for product X1 was an acceptable 1.5%.
* C - Because of supply shortages in the current fiscal year we are forced to change the material of a key component.
* I - Unfortunately, that resulted in the failure rate doubling this year.
* P - It is critical we address this problem immediately.
* A - Please approve the team 5 days to investigate the specific causes of the increase and establish the necessary next steps.
* B - By doing this we will reduce the failure rate to an acceptable level and develop guidelines for preventing such problems in the future.
More information can be found at [SCIPAB- Six Steps To Reach Your Audience](https://dzone.com/articles/scipab-six-steps-to-reach-your-audience).

## Beamy Guidelines

Beamy is our company conference call robot. It lives in the San Francisco boardroom.
Its main purpose is to allow those outside of the boardroom a view into the space and people.
When you call in to the beam your face will appear on the screen (so make sure your webcam
works) and you can drive the robot around the boardroom. It simulates being in the space without
physically being there. It is really cool and everyone should try it and have fun with it.

* You should have received an invite during onboarding to connect and to download a desktop client. If you did not receive the invite, please request one in the Slack #peopleops channel.
* **Beamy times**: 8am until 6pm Pacific time. [Please check the current time!](https://time.is/San_Francisco) on workdays and during all company events, for other times please @mention Sytse in the Slack #valley channel to see if it is OK. It is on auto connect so you'll beam right in.
* The email invite will come from "Suitable Tech". Once you are sent an invite you can beam in at any time and drive around our beam. Don’t forget to park it back on the charger when you are done. You can do so by driving up to the charger, when you see a green outline press AND HOLD 'p' until it's parked. Make sure it is charging, otherwise try again.
* If you don't use headphones be careful about your volume and microphone placement, it might start singing, if so immediately mute your microphone and switch to headphones.
* More info about Beam can be found at [Suitable Tech](https://suitabletech.com).
* Please report any questions or issues you have about the beam in the Slack #peopleops channel.

## Company phone number
{: #phone-number}

If you need to provide the details of GitLab's contact information you can take the [address from the visiting page](/visiting) for reference; or the [mailing address](/handbook/people-operations/#addresses) of the office in the Netherlands if that is more applicable.

If a phone number is required, leave this field empty by default. If that is not possible, then use
the general number (+1-415-761-1791), but be aware that this number simply guides to a voice message that refers the caller back to contacting us via email.

## Organization code names

* Listed in Google Sheet under 'Organization code names'
* To make it easier to recognize code names we base them on classic car models.

There are two types of code names:

* **Don't mention publicly** We can use code names anywhere we regularly share items in that medium with people outside the company: issue trackers, functional group updates, etc. For these we don't have to use code names in things that are never published: salesforce, zuora, zendesk, verbal conversations.
* **Don't write down** there are organizations that we shouldn't write down anywhere.

## Ubiquitous language

At GitLab we use ubiquitous language to increase communication efficiency.
This is defined in [Domain-driven design](https://en.wikipedia.org/wiki/Domain-driven_design) as: "A language structured around the domain model and used by all team members to connect all the activities of the team with the software.".
We use it for activities in GitLab, even ones not implemented in software.
By having ubiquitous words to identify concepts we prevent confusion over what is meant, for example we refer to [parts of our organization](/team/structure/) as a function, department, or group depending on exactly what is meant.
Make sure that domains don't overlap, for example [organization size](/handbook/sales/#organization-size) and [deal size](/handbook/sales/#deal-sizes) don't reuse words to prevent overlap.
If a term is ambiguous don't use it, for example our [hiring definitons](/handbook/hiring/#definitions) have roles and vacancies but avoid the ambiguous word job.
Make sure that people can infer as much as possible from the word, for example our [subscription options](/handbook/marketing/product-marketing/#tiers) allow you to know if someone if using self-managed or GitLab.com.
Make sure terms don't overlap without clearly defining how and why, for example see our [tier definitions](/handbook/marketing/product-marketing/#definitions).
Keep terms to one or at most two words to prevent people from introducing ambiguity by shortening a term. When using two words make the first word unique because people tend to drop the second word more often.

## YouTube

### Live streaming

If you are hosting a meeting that would be interesting, please livestream using Google Hangouts. Please use GitLab's YouTube account to livestream. If you need to request access, instructions are in 1Password.

1. Notify participants the meeting is being livestreamed before, and at the start of, the meeting.
1. Login to YouTube and click on the Tanuki in the upper right corner. Choose "Creator Studio"  (read the secure note in 1Password called "YouTube" for instructions on how to get access).
1. Choose "Live Streaming", then "Events" from the left side menu, and click on "New live event" in the upper right corner.
1. Give your event a title, description, and keep the privacy dropdown on the default `Public` setting.
1. Set the time of the livestream, and set the "Type" to 'Quick'. If you want to go live immediately, keep the default `Now` setting and choose "Go live now". This will place you in a Google Hangout but will not automatically begin the livestream.
1. To schedule the live event for later, choose the day and time from the drop downs, and click "Create event" to save.
1. To start your scheduled live stream event, navigate to the "Events" page in YouTube, find your event, and choose "Start Hangout On Air". This will place you in a Google Hangout but will not automatically begin the livestream.
1. Up to 50 participants can join the Google Hangout. To invite participants, click on the `Invite People` icon from menu in the top center of screen. You can either share the permanent link, or invite individuals.
1. Once capacity is met, anyone else can participate via the YouTube Watch page.
1. When you are ready to broadcast, choose the green "Start Broadcast button" at the bottom of the Google Hangout console. You will see a "LIVE" message once streaming.

### Upload conversations to YouTube

1. If you have a conversation that might be interesting please hit "record" (unless the [meeting is being livestreamed](/handbook/communication/#live-streaming) already).
1. Log in to the [Zoom](https://zoom.us/) account of the meeting and go to the menu on the right and choose "My Recordings" (it can take up to 30 minutes before the recording is available to be shared).
1. Select the meeting and download the recording to your computer (if you can't find the recording because it was a while ago check "Trash" in the menu on the top left and "Recover" the recording).
1. Go to the [YouTube upload page](https://www.youtube.com/upload) and log in to the GitLab account (read the secure note in 1Password called "YouTube" for instructions on how to get access).
1. Drag and drop your recording into the window to upload it. Keep the privacy dropdown on the default 'Public' setting (unless there is confidential material).
1. While it's uploading, edit the title and description. Place "Confidential:" at the beginning of the video's title if the video will be kept unlisted on our YouTube channel.
1. Be sure to include relevant links (for example a handbook page or presentation) in the description, and add the video to any relevant playlists.
1. When it is done uploading, press publish, then click on the Embed tab and copy the code, and insert that in the relevant part of the handbook or documentation.

### Don't worry about the quality

1. There is no minimum quality, so please share it on our [GitLab Youtube channel](https://www.youtube.com/channel/UCnMGQ8QHMAnVIsI3xJrihhg), as long as there is nothing inappropriate or confidential.
1. Everyone at the company probably has at least one conversation every week that is relevant to more people, so please share it.
1. We always list videos publicly instead of having them unlisted, unless there is confidential material. This allows more people to find the content.
1. Don't worry about whether or not it will be interesting to absolutely everyone. Just give it a descriptive title so people know what it is about, and let _them_ decide whether or not they should watch it.
1. Make sure that all participants are aware that you're recording.
1. You don't have to be sure it is interesting and OK to share when you start recording; you can make that decision after the fact.
1. If you record an in-person conversation with your mobile phone please hold your phone in landscape (horizontal) mode.

### Why livestream?

1. Allows more people to participate in real-time.
1. The recording is automatically uploaded to YouTube.

### Why record?

1. Allows more people to benefit from the content.
1. Allows the original participants to review the content later.
1. You can link to it instead of repeating yourself.

### Why Youtube and not Google Drive?

Always use YouTube and never use Google Drive, because YouTube videos:

1. are streamed [more reliably](https://peering.google.com/#/infrastructure).
1. have mouse-over thumbnails.
1. can be played at a higher speed.
1. can be fast forwarded and rewound in 10-second blocks.
1. can be timeshifted by adding them to a watch later list.
1. can be embedded, for example in the handbook.
1. restart at the right spot after being reloaded.
1. can be easily viewed on other devices, like TVs or streaming devices, with YouTube support.
1. allow links to a [specific time in the video](https://www.h3xed.com/web-and-internet/link-to-a-specific-time-in-a-youtube-video).
1. can have subtitles added automatically.
1. are [zero rated by some mobile providers](https://www.t-mobile.com/offer/binge-on-streaming-video.html)
1. will be served to people when it is relevant, automatically, since YouTube is a distribution channel.
1. allows anyone to contribute by leaving comments.

## When to record and publish to Youtube

<iframe width="560" height="315" src="https://www.youtube.com/embed/RB8OC70RAfo?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
