---
layout: markdown_page
title: "Technical Writing"
---

### Welcome to the Technical Writing Handbook!
{:.no_toc}

## On this page
{:.no_toc}

* Will be replaced with the ToC, excluding the "On this page" header
{:toc}

## Other pages related to Technical Writing
{:.no_toc}

* [Workflow][technical writing workflow]
* [Markdown Guide](/handbook/product/technical-writing/markdown-guide/)
* [Community writers](/community-writers/)
* [Release posts](/handbook/marketing/blog/release-posts/)

## Technical Writing

> _Technical writing is sometimes defined as simplifying the complex. In a concise and deceptively simple definition, it is a whole range of skills and characteristics that address nearly every field of human endeavor at some level._ ([techwhirl.com](http://techwhirl.com/what-is-technical-writing/))

At GitLab, tech writers are the folks who take care of writing and maintaining technical content, while keeping it clear, concise, consistent, professional, and up-to-date.

[Technical Writers] are part of the Product Team. Their mission is to help
GitLab by:

- keeping all features well documented
- ensuring the information regarding GitLab CE/EE/CI and its particularities are up to date
- writing guides, recipes, and blog content
- assisting the team with documentation and non-documentation tasks
- reviewing all technical content published in the channels we use

[Documentation] helps the GitLab community to:

- set up and manage their accounts
- set up and update GitLab instances
- use any tool or feature
- handle integrations and services

Docs are written technically, methodically, programmatically, clearly,
and practically.

[Blog posts][blog] have the same goal of assisting the GitLab community as
documentation, but with a more natural and reader-friendly language. Also,
besides technical content, posts can be informative, tell use-case stories,
relay customer experiences, and present a much more diverse selection of
content, since they are designed to be interesting to our audience.

Whenever we write for GitLab, it's necessary to keep in mind that we are writing
_on GitLab's behalf_. We are representing the company. Therefore, it's important
to keep our personal opinions, biases, and points of view separate, and always
be clear, direct, concise, and above all professional. This is detailed below,
in [Professional Writing Techniques]. Make sure to read this through before
writing for GitLab.

Also, our content is written in markdown Kramdown. Be sure to read the [Markdown
Style Guide] before venturing into writing for our website [about.GitLab.com] or
our [Blog], which are our "faces to the world".

On the [GitLab Blog Handbook][marketing-blog], you'll find out more about the
GitLab Blog directive, and the [Blog Style Guidelines][blog-style-guidelines]

## Workflow

In order to be organized and provide timely documentation with every feature
release, a standard workflow (process) is required.

[Read how the Docs team flows.][technical writing workflow]

## Markdown Style Guide for about.GitLab.com

Check out our [Markdown Style Guide] for the markup used throughout [about.GitLab.com], including any markdown page or blog post. You'll
find useful information there, some [Kramdown] magic, and it might save you a lot of typing.

## Professional Writing Techniques

When writing professionally, it's important to understand and follow some standards, for the purpose of achieving high quality work in an optimal time frame.

Technical papers have the characteristic of being less casual and more formal; they're not the right place to express opinions, nor to give advice. Accuracy is what matters most. For scientific papers, the rules are even more restrictive and the language is strictly formal.

For blog posts, we need to find a middle ground. Be clear, precise, and professional, but be empathetic and "reader-friendly". A discrete and occasional touch of humor is also welcome.

When writing non-technical blog posts, we can be less formal and more casual, depending on the subject we are writing about. Regardless, we need to continue being professional. This means we can be friendly and personal, but we need to focus on the point. The methods suggested in this document are valid for both technical and non-technical topics in regards to the process of writing, not to the content itself.

Before writing on behalf of GitLab, make sure you've read through this [guide][marketing-blog].

### Technical Blog Posts

[Technical][tech-writing-wiki] posts include: tutorials, guides, overviews, techniques, methods, processes, and anything else which requires some sort of technical knowledge or standard procedure. For these cases, follow all the steps described in the [writing method](#writing-method).

### Non-Technical Blog Posts

For non-technical posts, we don't need to do every step in the [writing method](#writing-method) below. Check which category matches best with the subject you'll be working on to know how to proceed.

- **Personal Experience**
   - _Personal content_: user stories, user experience, opinion-based overviews or comparisons, etc.
   - _Inside GitLab_

    Steps that can be skipped: [4th (Research)](#4th-research) and [7th (Test)](#7th-test).

- **Information** (If the content is not a tutorial or a guide, but it has an informative purpose)
   - _Feature overviews_
   - _Product comparisons_
   - _Case studies_

    Steps that can be skipped: [7th (Test)](#7th-test)  
    Note: For the [4th (Research)](#4th-research) step, provide links to corroborate your information.

- **Quick Announcements**
   - _Release announcements_
   - _Feature highlights_

    Steps that can be skipped: [2nd (Brainstorm)](#2nd-Brainstorm), [3rd (Plan)](#3rd-Plan), [4th (Research)](#4th-research), [5th (Draft)](#5th-draft), [7th (Test)](#7th-test).  
    Note: **Do Not Skip** 1st, 6th, 8th, 9th, or 10th steps.

- **Other**

    If your chosen subject doesn't match any previous category, read through the method below and try to adapt it accordingly. Feel free to ask for help if needed.

### Writing Method

The following method suggests steps to take in order to create high quality written productions. This approach is recommended, but flexible. Feel free to adapt it to your needs.

#### 1st. Subject, Audience, Requirements

The first step is to define the subject, the audience, the knowledge level, and the requirements.

- Choose a subject you are very familiar with and that you are comfortable explaining in deep detail.
- Create a title for your article, based on the previous step. A good title is short and accurate.
- Choose the audience:
   - Who might have an interest in this subject? Which instance of GitLab is involved? GitLab EE, CE?
   - What is the technical expertise level necessary to follow your steps? Does the user need to be simply familiar with the subject, fairly comfortable with it, or an expert?
   - What is required to make it work locally for the user? Specify the Operating System and any necessary software or hardware configuration.
- Add this information to a new issue on the [blog posts issue tracker][blog-tracker]
- Keep in mind that you'll need to include an introductory sentence for the beginning of the article with this information. It can be explicit or subjective.
  For example, for a tutorial for Android: _"We assume you know the process of creating an Android App, you already have projects running locally, and you are familiar with the GitLab UI"_. This would tell the reader that they need to be an intermediate/advanced app developer, have the software necessary to run an Android application installed locally, and have used GitLab before.


#### 2nd. Brainstorm

Think about everything regarding the subject you want to write about. Write down every piece of information, every detail, every cool thing that can be achieved, every scheme, key process, or knowledge that could be included in an article about your topic. Don't worry about the order, if it's important or not, or if it makes perfect sense or not. Free your brain and let it work with no boundaries. Here, creativity and originality matters most.

#### 3rd. Plan
<!-- Is this "Perfect" necessary? -->
Perfect. Now you should have a lot of ideas to organize. In this stage you will filter out the important things from your brainstorming notes, arrange them in a logical order, and cut out what's not necessary. You'll do that by creating the _outlines_ for your article. Organize the sections with titles, subtitles, bullet points, brief descriptions, and include important [(key)words] that came out in the brainstorming that you want to include in your article.

Keep in mind the audience you chose before. Do not complicate things if you are writing for beginners, or simplify too much if you're targeting experts.

#### 4th. Research

Now that you know what you want to include in your article, it's time to find reliable sources to support it. You may know the process, but you still need to include sources for technical information.

For example, let's consider a post about Android Apps. If you write that you need an emulator to preview your Android app locally, you should provide a link to the [official Android documentation][android-doc] where it's explained that an emulator is needed, and also add a link to the [emulator][android-emulator] itself.

Search for the sources you already know you'll need. Copy and paste the links to key information into a text document or bookmark them, however you prefer. Gather the links in such a way that you can find them easily, to include them while you draft.

Be aware that this step will end only when your post is published. You will need to come back and search for sources again and again, until the end.

A _reliable source_ is officially documented information, as well as content described in books, newspaper articles, scientific papers, etc.
<!-- some ideas to make a better sentence here?  -->

#### 5th. Draft

Now that you have a skeleton for your article, and some links to guide you, you can start to write, filling in the gaps following the structure you planned in step 3.

Never make a statement without providing the source for that information, unless it is your own conclusion and you have the expertise to defend it. This way of writing will avoid mistrust and loss of credibility. Follow the [Writing Tips](#writing-tips) below.

It's much quicker to write with a clear plan. Contiinue and write everything you need. Don't try to review every sentence or think too much before writing it down. You'll review afterwards.

#### 6th. Improve

After you finished step 5, read everything again, and make sure you're not repeating yourself, and that there is no unnecessary information. Cut out everything non-essential. This is the first review.

After your first review, try to do other things to intentionally deviate your attention from the text. Preferably, close the file and only open it the next day, after some sleep. This will help you clear your head, which will help you find mistakes you wouldn't have caught even after several hours working on the same thing.
<!-- End of last sentence unclear -->

Now, during your second review, it's time to look for typos and grammar mistakes. Check that the text is clear, easy to understand and that it's not boring. Make any necessary adjustments, then do another review.

#### 7th. Test

If you wrote a tutorial or about any procedure that can be tested, test it. Go over your steps **exactly as you described them**, and check if you succeed following your own steps. Testing in as many conditions as possible is preferred: different Operational Systems, configurations, versions, or whatever applies to your case. If you have someone close to you that could contribute by testing it for you too, that's even better. After testing, go through steps 4 to 6 again, if necessary.

#### 8th. Submit

When you're happy with your draft, submit it in a [WIP][WIP MR] (Work In Progress) merge request.

#### 9th. Review

Be aware that your reviewers will probably request changes, ask difficult questions, insist on some points. Do not be discouraged by the review. It will only help you to improve it even more, and enhance the quality of your work.

If you don't agree with the reviewer about something, just say it (respectfully). Discuss your matter and defend your point of view, until you both agree or find a compromise.

#### 10th. Publish

After you adjust the post according to the reviewers' requests, it will get published and everybody will be happy for you!

### Writing Tips

This is a simple list, for things to do and avoid when writing. It's not an exact science, though. Try to find a balance between what's best and what's possible. Be yourself and use your own judgement.

- Be original: do not repeat yourself, nor repeat other posts or documentation
- Be concise: say what you need to say. Not more, nor less
- Be attentive: do not repeat the same word, use [synonyms]
- Be smart: try to predict questions, and answer them in the text
- Be professional: do not make any statement if you don't have a reliable source or the expertise to defend it
- Be clear: everything may seem logical to the person doing the writing, but not necessarily to those reading
- Be organized: in tutorials, do not jump over a step presuming the audience knows what to do. It may ruin the logic and impacts audience attention.
- Be consistent: try to adopt regular patterns to facilitate comprehension
- Be precise: prefer "it is" over "I think"
- Be inclusive: use "we" rather than "you" or "I", and "they" instead of "he/she"
- Be creative: think _out-of-the-box_ and explore things _out-of-the-blue_

## Staying up to date

You are not expected to know everything, but it is essential to stay on top of
things. Collaborating with the other groups is very important for learning about
what features will be released and what resources are needed from your side.

Some tips:

- Take part in the kickoff and retrospective meetings. During the kickoff
  meeting you will get a general idea of what is about to be shipped and
  potentially calculate how much of your time you will have to allocate on new
  documentation. If something in the process has gone wrong during the release
  cycle, make sure to mention it in the retrospective meeting. We can always do
  better 😊
- Directly participate in the regular meetings each group has. That way you will
  establish a connection between yourself and engineering, UX, QA, etc.
- Attend the FGU of each group in engineering since it may contain valuable
  information on the upcoming features you need to know about.

<!-- Identifiers, in alphabetical order -->

[about.GitLab.com]: /
[android-doc]: http://developer.android.com/intl/pt-br/tools/help/emulator.html
[android-emulator]: http://developer.android.com/intl/pt-br/tools/devices/emulator.html
[blog]: /blog
[blog-style-guidelines]: /handbook/marketing/blog/#blog-style-guidelines
[blog-tracker]: https://gitlab.com/gitlab-com/blog-posts/issues
[bundler]: http://bundler.io/
[documentation]: http://docs.gitlab.com/
[git]: https://git-scm.com/
[issue-docs]: https://gitlab.com/gitlab-org/gitlab-ce/issues/
[(key)words]: http://www.wordstream.com/seo-keyword
[Kramdown]: http://kramdown.gettalong.org
[Mac screenshot]: https://support.apple.com/en-us/HT201361
[Markdown Style Guide]: markdown-guide/
[marketing-blog]: /handbook/marketing/blog/
[middleman]: https://middlemanapp.com/basics/install/
[Nimbus Screenshot]: http://nimbus.everhelper.me/screenshot.php
[Professional Writing Techniques]: #professional-writing-techniques
[Screenshot Tool]: https://help.ubuntu.com/lts/ubuntu-help/screen-shot-record.html
[Snipping Tool]: https://support.microsoft.com/en-us/help/13776/windows-use-snipping-tool-to-capture-screenshots
[synonyms]: http://www.thesaurus.com/
[technical writers]: /job-families/product/technical-writer/
[technical writing workflow]: /handbook/product/technical-writing/workflow/
[tech-writing-wiki]: https://en.wikipedia.org/wiki/Technical_writing
[tinypng]: https://tinypng.com/
[unsplash]: https://unsplash.com/
[WIP MR]: http://docs.gitlab.com/ee/workflow/wip_merge_requests.html "Work In Progress Merge Request"
[www-gitlab-com]: https://gitlab.com/gitlab-com/www-gitlab-com/
