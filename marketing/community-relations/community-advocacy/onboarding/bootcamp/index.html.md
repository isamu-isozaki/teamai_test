---
layout: markdown_page
title: Community Advocate Bootcamp Checklist
---

## Bootcamp Checklist for Training of New Community Advocates
<a name="checklist"></a>

Your manager should create an issue with this checklist on the [community advocacy issue tracker](https://gitlab.com/gitlab-com/marketing/community-advocacy/general/issues/index.html.md) for you as part of your onboarding.
This list looks strange in this handbook because it is formatted to be copy-pasted into an issue and then render properly there.

The topics are generally ordered by priority in which they need to be tackled,
but feel free to work on later things in the list when you are waiting on something.

```markdown
We need to keep iterating on this checklist so please submit MR's for any improvements
that you can think of. The file is located in
[`sourcehttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/onboarding/checklist/index.html.md`](https://gitlab.com/gitlab-com/www-gitlab-com/tree/master/sourcehttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/onboarding/checklist/index.html.md/index.html.md)
in the [www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com/index.html.md/index.html.md) project. If an item does not start with a role or name of someone else, it's yours to do.

**Goal of this entire checklist:** Set a clear path for Community Advocacy training

### Stage 0: Complete general onboarding to have all necessary accounts and permissions

- [ ] **Done with Stage 0**

_Typically completed within first week_

1. [ ] General expectations: it is expected that you will _start_ to tackle Stages 0, 1, 2, and 3 as early as your first week, but you are not expected to complete all items for some number of weeks. We believe that you often learn best and fastest by diving into (relatively easy/index.html.md) tickets, and learning by doing. However, this has to be balanced with making time to learn some of the tougher topics. The expectation is therefore that you are sufficiently advanced in your onboarding by the end of your first week, that you can answer 2-5 "simple" tickets. Over the following weeks, your manager will set higher targets for the number and difficulty of tickets to be tackled, but you should always have about 2-3 hrs per day to spend on working through this bootcamp. Some days it will be less, some days it will be more, depending on ticket load and how deep "in the zone" you are in either the bootcamp or the tickets you are responding to; but an average of 2-3 hrs per day should allow you to complete everything through to the end of Stage 6 within about four weeks.
1. [ ] General Onboarding Checklist: this should have been created for you on [the People Ops Employment issue tracker](https://gitlab.com/gitlab-com/people-ops/employment/issues/index.html.md/index.html.md) as an issue by PeopleOps when you were hired.
   1. [ ] Finish every item on that list starting with `New team member:` until you are waiting for someone to answer a question or do something before you can continue that list.
   1. [ ] Start with Stage 1 here, but also with the first steps in Stage 2 and Stage 3.
   1. [ ] Check back daily on what was blocking you on your General Onboarding Checklist until that list is completely done, then focus on this one.

### Stage 1: Become familiar with `git` and GitLab basics

- [ ] **Done with Stage 1**

_Typically started in first week, completed by end of second week_

If you are already comfortable with using Git and GitLab and you will be able to
retain a good amount of information by just reading and watching through, that is
okay. But if you see a topic that is completely new to you, stop the video and try
it out for yourself before continuing.

1. [ ] Just quickly check on your Zendesk account to make sure that is ready for you when you need it.
1. [ ] Add a [profile picture](https://support.zendesk.com/hc/en-us/articles/203690996-Updating-your-user-profile-and-password#topic_rgk_2z2_kh/index.html.md) to your Zendesk account
1. [ ] Let your manager know if for some reason you were not able to create an account on Zendesk.
1. [ ] Under your profile on Zendesk, it should read `Agent`. If it reads `Light Agent`, inform your manager.

Cover these topics on the [GitLab University](https://docs.gitlab.com/ee/university/index.html.md/index.html.md):

1. [ ] Under the topic of Git
  1. [ ] [About Version Control](https://docs.google.com/presentation/d/16sX7hUrCZyOFbpvnrAFrg6tVO5_yT98IgdAqOmXwBho/edit#slide=id.gd69537a19_0_14/index.html.md)
  1. [ ] [Try Git](https://www.codeschool.com/account/courses/try-git/index.html.md)
1. [ ] Under the topic of GitLab Basics
  1. [ ] All the [GitLab Basics](http://docs.gitlab.com/ee/gitlab-basics/README.html/index.html.md) that you don't feel comfortable with. If you get stuck, see the linked videos under GLB in GitLab University
  1. [ ] [GitLab Flow](https://www.youtube.com/watch?v=UGotqAUACZA/index.html.md)
  1. [ ] Take a look at how the different GitLab versions [compare](/features/#compare/index.html.md)
1. [ ] Any of these that you don't feel comfortable with in the [user training](https://gitlab.com/gitlab-org/gitlab-ee/tree/master/doc/university/training/index.html.md) we use for our customers.
  1. [ ] `env_setup.md`
  1. [ ] `feature_branching.md`
  1. [ ] `explore_gitlab.md`
  1. [ ] `stash.md`
  1. [ ] `git_log.md`
  1. [ ] For the rest of the topics in `user training`, just do a quick read over the file names so you start remembering where to find them.
1. [ ] Get familiar with the services GitLab offers
  1. [ ] The differences between [CE and EE](/pricing/index.html.md/index.html.md)
  1. [ ] [GitHost](/gitlab-hosted/index.html.md/index.html.md)
    * Note that we're currently not accepting any new customers

### Stage 2: Installation and Administration basics

- [ ] **Done with Stage 2**

_Typically started in first week, completed by end of third week_

#### Goals

- Be prepared to reproduce issues that our users encounter.
- Be comfortable with the different installation options of GitLab.
- Have an installation available for reproducing customer bug reports.

1. [ ] Check back on your Zendesk account if you are not yet an `Agent`.

#### Installations

You will keep one installation continually updated on Digital Ocean (managed through terraform/index.html.md), just like many of our clients.

Installation from source is not common but will give you a greater understanding of the components that we employ and how everything fits together.

1. [ ] Manager: Add new team member to the [dev-resources](https://gitlab.com/gitlab-com/dev-resources/index.html.md) project.
1. [ ] Use terraform to create a new test instance.
    1. [ ] Clone the dev-resources project.
    1. [ ] Read up on [how to create a new instance](https://gitlab.com/gitlab-com/dev-resources/blob/master/dev-resources/README.md/index.html.md).
    1. [ ] Create a new file and name it `<your-full-name>.tf` in a new branch. You can copy another team member's file and modify it or you can create your own from scratch. If you have any issues or questions ask in the #support channel.
    1. [ ] After you've created it, open up a merge request and if the tests pass then merge it.
1. [ ] Set up your test environment
  1. [ ] Create a non-root user
  1. [ ] Add your public SSH key to `authorized_keys` for the created user
  1. [ ] Optional: Disable password login
  1. [ ] Optional: Disable root SSH login
1. [ ] Install GitLab via [Omnibus](https://gitlab.com/gitlab-org/omnibus-gitlab/index.html.md/index.html.md)
  1. [ ] Populate with some test data: User account, Project, Issue
  1. [ ] Backup using our [Backup rake task](http://docs.gitlab.com/ee/raketasks/backup_restore.html#create-a-backup-of-the-gitlab-system/index.html.md)
  1. [ ] Delete the test data
  1. [ ] Restore backup using our [Restore rake task](http://docs.gitlab.com/ee/raketasks/backup_restore.html#restore-a-previously-created-backup/index.html.md)
  1. [ ] Keep this installation up-to-date as patch and version releases become available, just like our customers would.
1. [ ] Ask as many questions as you can think of on the `#devrel` chat channel

### Stage 3. Community Interaction

- [ ] **Done with Stage 3**

_Typically started in first week, and completed by the end of the fourth week_

#### Goals

- Have a good understanding of ticket flow through Zendesk and how to interact with our various channels
- See some common issues that our customers are facing and how to resolve them.
- Learn about the community advocacy process at GitLab.

#### Initial Zendesk training

1. [ ] Complete Zendesk Agent training (allow 40 minutes for completion/index.html.md)
  1. Navigate to [Zendesk university](http://training.zendesk.com/checkout/3djt0nv8i5y5r/index.html.md) and register. You'll receive an email with information on accessing the Zendesk course
  1. Proceed to complete the **"Quick Tips: Agent"** course
1. [ ] Review additional Zendesk resources
  1. [ ] [UI Overview](https://support.zendesk.com/hc/en-us/articles/203661806-Introduction-to-the-Zendesk-agent-interface/index.html.md)
  1. [ ] [Updating Tickets](https://support.zendesk.com/hc/en-us/articles/212530318-Updating-and-solving-tickets/index.html.md)
  1. [ ] [Working w/ Tickets](https://support.zendesk.com/hc/en-us/articles/203690856-Working-with-tickets/index.html.md) *Read: avoiding agent collision.*
  
*Congratulations. You now have your Zendesk Wings*

From now on you can spend most of your work time answering tickets on Zendesk, try to set aside 2 hours per day to make it through **Stage 4-6** of this list. Never hesitate to ask as many questions as you can think of on the `#devrel` chat channel

#### Learn about raising issues and fielding feature proposals

1. [ ] Understand what's in the pipeline and proposed features at GitLab: [Direction Page](/direction/index.html.md/index.html.md)
1. [ ] Practice searching issues and filtering using [labels](https://gitlab.com/gitlab-org/gitlab-ce/labels/index.html.md) to find existing feature proposals and bugs
1. [ ] If raising a new issue always provide a relevant label and a link to the relevant ticket in Zendesk
1. [ ] Add [customer labels](https://gitlab.com/gitlab-org/gitlab-ce/issues?label_name%5B%5D=customer/index.html.md) for those issues relevant to our subscribers
1. [ ] Take a look at the [existing issue templates](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#issue-tracker/index.html.md) to see what is expected
1. [ ] Raise issues for bugs in a manner that would make the issue easily reproducible. A Developer or a contributor may work on your issue.
1. [ ] Schedule a 45 minute call with your trainer where you share your screen
with them while you answer tickets on Zendesk, they give you feedback and answer
your questions. The goal with this call is for your trainer to pass on tactical
knowledge about the ticket handling process. Repeat this step a few times if that seems useful.

#### Learn about the Community Advocacy process

Zendesk is our Community Advocacy Centre and our main communication line with our customers. We communicate with customers through several other channels too.

1. [ ] Ask different people in your team if they would be willing to do a 45 minute screen share with you as they answer tickets on Zendesk, thinking out loud as much as they can and answering your questions. Continue with the rest of the list while you wait for these to get scheduled.
  1. [ ] call with ___
  1. [ ] call with ___
  1. [ ] call with ___
1. [ ] Dive into our ZenDesk support process by reading how to [handle tickets](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#zendesk-workflow/index.html.md)
1. [ ] Start getting real world experience by handling real tickets, all the while gaining further experience with the Product.
  1. [ ] First, learn about our support channels that are handled by the [Community Advocacy team](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/index.html.md)
  1. [ ] Start with [Twitter](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#twitter/index.html.md)
  1. [ ] Continue on to [Disqus](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#disqus/index.html.md)
  1. [ ] Continue on to the [community@](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#community-email/index.html.md) email
  1. [ ] Continue on to [facebook](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#facebook/index.html.md)
  1. [ ] Continue on to the [GitLab forum](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#gitlab-forum/index.html.md)
  1. [ ] Read about the [other channels](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#specific-channels/index.html.md) the Community Advocacy team supports
1. [ ] Check out your colleagues' responses
   1. [ ] Read through about 20 old tickets that your colleagues have worked on and their responses
1. [ ] Take a look at the [GitLab.com Team page](/team/index.html.md/index.html.md) to find the resident experts in their fields
1. [ ] Learn about our [mentions-of-gitlab](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#mentions/index.html.md) Slack channel
  * This tracks all channels that are not routed through ZenDesk
  * HackerNews is routed through this channel - This is the top priority channel
- [ ] Block off your calendar to anticipate for release posts
  - They occur regularly every 22nd in the month, just like each GitLab release.
- [ ] Order, expense, and read the Art of Community by Jono Bacon ([Amazon Link](https://www.amazon.com/Art-Community-Building-New-Participation/dp/1449312063/index.html.md)/index.html.md)

#### Learn about handling our diversity sponsorship program

1. [ ] Read about our [Diversity Sponsorship Program](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#diversity-sponsorship/index.html.md)
1. [ ] Take a look at the [Diversity Sponsorship applications] (https://docs.google.com/spreadsheets/d/1FQM7rZ0wdpdZZ4Z7Yk3URjDvHripDRkkiiu0a9usQhk/edit?usp=drive_web&ouid=112392573724280886461/index.html.md)
1. [ ] Discuss with your trainer what qualifies an event for the diversity sponsorship program
1. [ ] Memorize our sponsorship acceptance/declination [email templates](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#email-templates/index.html.md)

#### Learn about handling swag at GitLab

We use Shopify for [our storefront](https://shop.gitlab.com/index.html.md) and [Printfection](http://www.printfection.com/index.html.md/index.html.md) for sourcing swag.

1. [ ] Learn about our [MVP appreciation gifts](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#mvp-appreciation-gifts/index.html.md)
1. [ ] Learn about our [`#swag` channel](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/developer-relations/community-advocacy/#handling-the-swag-channel/index.html.md)

### Stage 4. Gathering Diagnostics

- [ ] **Done with Stage 4**

_Typically do this around the third week._

**Goal** Understand the gathering of diagnostics for GitLab instances

1. [ ] Learn about the GitLab checks that are available
    1. [ ] [Environment Information and maintenance checks](http://docs.gitlab.com/ee/raketasks/maintenance.html/index.html.md)
    1. [ ] [GitLab check](http://docs.gitlab.com/ee/raketasks/check.html/index.html.md)
    1. [ ] Omnibus commands
        1. [ ] [Status](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/maintenance/README.md#get-service-status/index.html.md)
        1. [ ] [Starting and stopping services](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/maintenance/README.md#starting-and-stopping/index.html.md)
        1. [ ] [Starting a rails console](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/maintenance/README.md#invoking-rake-tasks/index.html.md)

### Stage 5. Optional Advanced GitLab Topics

Discuss with your training manager if you should stop here and close your issue
or continue. Also discuss which of the advanced topics should be followed. Do
not just do all of them as they might not be relevant to what customers need
right now and can be a significant time investment.

These are some of GitLab's more advanced features. You can make use of
GitLab.com to understand the features from an end-user perspective and then use
your own instance to understand setup and configuration of the feature from an
Administrative perspective

- [ ] Set up and try [Git LFS](https://docs.gitlab.com/ee/workflow/lfs/manage_large_binaries_with_git_lfs.html/index.html.md)
- [ ] Get to know the [GitLab API](https://docs.gitlab.com/ee/api/README.html/index.html.md), its capabilities and shortcomings
- [ ] Learn how to [migrate from SVN to Git](https://docs.gitlab.com/ee/workflow/importing/migrating_from_svn.html/index.html.md)
- [ ] Set up [GitLab CI](https://docs.gitlab.com/ee/ci/quick_start/README.html/index.html.md)
- [ ] Create your first [GitLab Page](https://docs.gitlab.com/ee/pages/administration.html/index.html.md)
- [ ] Set up a [GitLab Development Kit](https://gitlab.com/gitlab-org/gitlab-development-kit/index.html.md) instance
- [ ] Get familiar with the GitLab source code by finding the differences
between the [EE codebase](https://gitlab.com/gitlab-org/gitlab-ee/index.html.md) and the [CE codebase](https://gitlab.com/gitlab-org/gitlab-ce/index.html.md)
```
