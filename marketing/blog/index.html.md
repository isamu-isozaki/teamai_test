---
layout: markdown_page
title: "Blog Handbook"
---

----

The [GitLab blog](https://www.about.gitlab.com/blog/index.html.md) is managed by the [Managing Editor](/job-families/marketing/content-editor/index.html.md/index.html.md).

## Communication
- [Public issue board](https://gitlab.com/gitlab-com/www-gitlab-com/boards/804552?&label_name[]=blog%20post/index.html.md); to propose a blog post, create a new issue and label it `blog post`.
- Chat channels; use `#content` for questions, `#blog` for updates on most recently published articles.
- Content Office Hours; each Monday at 9:30am PT the content marketing team holds an open Zoom call, for
for 30 minutes, for all team members to pitch blog posts, get writing help, ask questions, make suggestions, and offer feedback. Check the GitLab Team Meetings calendar for the Zoom link.

## On this page
{:.no_toc}

- TOC
{:toc}

----

## Other related pages
- [Editorial style guide](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/corporate-marketing/#general-editorial-style-guidelines/index.html.md)
- [Editorial calendar](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/corporate-marketing/content/editorial-calendar/index.html.md/index.html.md)
- [Content Hack Day](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/corporate-marketing/content/content-hack-day/index.html.md/index.html.md)
- [Monthly release post](/release-posts/index.html.md/index.html.md)

## Objectives

1. Build credibility and authority.
1. Increase awareness of GitLab the company, product, and community.
1. Increase organic search rankings and traffic.
1. Contribute to lead generation and revenue.

## Scope
**Mission statement:** Increase awareness of the benefits of a single application for the entire DevOps lifecycle.

The blog is not the permanent place for tutorials, which should live in the docs and should be linked to when relevant.

### Definitions

1. **Content marketing:** Examples, education, reporting, storytelling, thought leadership, and use cases.
1. **Corporate:** Company news, announcements, and community updates (ex: issue bash, contributor profiles/index.html.md).
1. **Product:** Release posts, critical updates, and partnership announcements.

## Workflow

We follow the [GitLab Workflow](/gitlab-flow/index.html.md/index.html.md). At GitLab, everyone can contribute, and we encourage anyone to submit a blog post idea or write your own. Below are instructions on how to contribute to the GitLab blog.

1. Any new blog post should start as an issue in the `https://gitlab.com/gitlab-com/www-gitlab-com` project and be labeled [`blog post`](https://gitlab.com/gitlab-com/www-gitlab-com/issues?label_name%5B%5D=blog+post/index.html.md).
1. Writing your own post: You do not need approval to write for the GitLab blog. Assign the issue and associated merge request to yourself and apply the appropriate labels based on what stage of creation you are on. Once it's ready for editorial review, assign to @rebecca.
1. Submitting an idea: if you have a blog post idea but do not intend to write it yourself, simply label the issue `blog post` and the content team will review during triage.
1. Time-sensitive posts: if you have a blog idea or post that is time sensitive, please apply the `high priority` label and ping @rebecca.

Blog post ideas and proposals for [Content Hack Day](https://about.gitlab.comhttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/corporate-marketing/content/content-hack-day/index.html.md/index.html.md) should be created in the [Content Hack Day project](https://gitlab.com/gitlab-com/content-hack-day/index.html.md). We keep these issues in a separate project because not all ideas and proposals that come from Hack Day will be worked on.

### Issue triaging

The Content Marketing team is responsible for triaging blog post issues and reviews the `blog post` backlog every Monday morning.

- Issues that are labeled `priority` will be added to the top of the planning list.
- If issues that have an assigned writer have not been active for three months, the Content Marketing team will evaluate if the post is likely to draw high traffic, and may work with the writer or take the post over to get it finished.
- Content Hack Day issues that have a committed, assigned writer will be moved to the www-gitlab-com project â€ these issues should move directly to the `In progress` stage as they should already have a draft started

### Labels

- `blog post`: every blog post idea, proposal, draft, etc. **MUST** have this label
- `priority`: blog posts that should be worked on immediately
- `Planning`: blog posts that have an assigned writer and will be started within two weeks
- `In progress`: blog posts that have a draft started â€ any issue with this label should have an attached merge request
- `Review`: blog posts that are ready for an editorial review
- `Guest/Partner post`: blog posts that are authored and submitted from a contributor outside of GitLab
- `customer story`: blog posts that include a customer interview
- `CEO interview`: blog posts submitted by the GitLab CEO and require their subject matter expertise
- `Content hack day`: blog posts that have been accepted from the Content Hack Day project.

## Editorial reviews
Editorial reviews are mandatory for every merge request. Please familiarize yourself with our [editorial style guide](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/corporate-marketing/#style-guide-and-tone-of-voice/index.html.md/index.html.md). Before you assign your merge request to a content editor, please ensure you've removed the WIP label, and include the following in the description:

- the direct link to your blog post's review app
- close `#number of your issue` so your issue closes automatically when the MR is merged.

All GitLab content editors can perform an editorial review on blog-post merge requests of colleagues and community contributors. You can find someone to review your own blog-post merge requests by looking on the team page. Merging blog posts is restricted to the managing editor and management.

### Checklist before merging

Reviewer â€ check these before you publish:

- Check if the post follows the [editorial style guide](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/corporate-marketing/#style-guide-and-tone-of-voice/index.html.md/index.html.md)
- Make sure [frontmatter](https://github.com/isamu-isozaki/teamai_test/tree/master/marketing/blog#frontmatter/index.html.md) is filled out correctly
- Check all links
- Check the file extension `.html.md.erb` and that the newsletter sign-up form is included in the post
- Check the date on the file name â€ if you need to update the date, do it in a separate commit, otherwise Git will add a new file and you won't be able to compare diffs if other changes were made
- Check the image(s/index.html.md) is(are/index.html.md) crunched down
- Check the blog appears good locally
- Has the post been optimized for SEO? Ping @srice for SEO review

When you have double checked, you can assign to @rebecca to merge. If Rebecca is OOO, assign to @erica.

## Publishing natively on LinkedIn and Medium
Occasionally, some blog posts are better suited to publishing natively by the author on LinkedIn, or on [Medium](https://medium.com/@gitlab/index.html.md). We reach slightly different audiences on these channels, and some content will get better exposure and reach if published there. If you submit a blog post and the content team decides it's a better fit for one of these, we will let you know. For now, we will treat this segmentation as an experiment, monitor the performance of different types of content on different channels, and apply our learnings. We may then be able to start planning content for specific outlets and commission stories accordingly.

## Third-party posts
If you are a partner or industry-adjacent third party who wants to write for our blog, please contact the [Partner Marketing](/product-marketing/#partner-marketing/index.html.md) team before proceeding.

Blog posts concerning third parties or partners, whether they are to be published on the GitLab blog or externally, should be proposed to the blog editorial team before agreeing.

As a rule, any blog post, regardless of the author, should offer some informational, educational, or entertainment value to the reader. We do not publish material that is exclusively promotional in nature.

### Guest posts by GitLab partners

Official [GitLab partners](/resellers/index.html.md) may use our [CTA button](#call-to-action/index.html.md) and include promotional copy, however the blog post must still serve a function (informational or educational/index.html.md) other than simply promoting something.

For either type of guest post, the process and guidelines for publishing are as follows:

1. Create an issue in the [www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com/issues/index.html.md) project and label it `blog-post` and `guest/partner post`.
2. If technical input is required, we will ask for instructions from the third party; otherwise it is at the discretion of the blog editorial and technical writing teams whether or not to go forward.

### Guest posts by non-partners

If the author of a guest post is not an official GitLab partner, they may link back to their website or own content with inline links, but may not include a [CTA button](#cta/index.html.md) or promotional copy.

## Formatting guidelines

All posts are written in Markdown. Please read through the [Markdown guide](https://github.com/isamu-isozaki/teamai_test/tree/master/product/technical-writing/markdown-guide/index.html.md/index.html.md) for reference.

It takes about 15-30 minutes for the blog post to appear as published after merged. As soon as it's live, check the post for broken links using this tool (or similar/index.html.md): <http://www.deadlinkchecker.com/>. Fix anything _before_ sharing in any communication channel or social media network.

### Create a new post

Every blog post should start as an issue in the [www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com/index.html.md) project and labeled `blog-post`. Start a merge request when you are ready to start drafting.

You can create a new post however you prefer: adding a new file to `/source/posts/`, duplicating an existing post, or using the command line, which is the safest way to do so. Just type into your terminal (opened in your local project directory/index.html.md):

```sh
rake new_post
```

Hit **enter** or **return**, then you'll be prompted to enter the post title. Type in the title exactly as you want it, for example "Hello World â€ I'm a new post" and rake will take care of the file name for you. Then you just open the file, fill in with your name, Twitter handle, and the post category, then you'll be good to start writing.

### Media embeds
We limit media embeds to the following providers:
- **YouTube** for video
- **CodePen** for code samples
- **Google Docs** for collaborative text
- **Google Sheets** for sharing spreadsheets
- **Google Slides** for sharing slides

### Newsletter sign-up form

We can now embed a CTA for readers to sign up for our newsletter directly from the blog post page. There are two different designs. Use the following:

```
<%= partial "includes/blog/content-newsletter-cta", locals: { variant: "a" } %>
```

  Result:

  ![Newsletter sign-up CTA variant A](/imageshttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/newsletter-cta-a.png/index.html.md){: .shadow}

  OR

  ```
<%= partial "includes/blog/content-newsletter-cta", locals: { variant: "b" } %>
  ```

  Result:

  ![Newsletter sign-up CTA variant B](/imageshttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/newsletter-cta-b.png/index.html.md){: .shadow}

  Note: this only works for blog post files with the extension `.html.md.erb`.

### Frontmatter

The post **frontmatter** is the first part of any post. It is standard and cannot be changed, so please make
sure to provide the correct information, and do not add nor remove anything from the default template:

```yaml
---
title: "This is the post title"
author: Firstname Lastname # if name includes special characters use double quotes "First Last"
author_gitlab: GitLab.com username # ex: johndoe
author_twitter: Twitter username or gitlab # ex: johndoe
categories: company
image_title: '/images/blogimages/post-cover-image.jpg'
description: "Short description for the blog post"
tags: tag1, tag2, tag3
cta_button_text: 'Watch the <strong>XXX release webcast</strong> live!' # optional
cta_button_link: 'https://page.gitlab.com/xxx.html' # optional
guest: true # required when the author is not a GitLab Team Member
ee_cta: false # required only if you do not want to display the EE-trial banner
install_cta: false # required only if you do not want to display the 'Install GitLab' banner
twitter_text: "Text to tweet" # optional;  If no text is provided it will use post's title.
featured: yes # reviewer should set
---
```

#### Cover image

For the cover, [create an image](#artwork-and-editable-image-files/index.html.md) or choose one from any public domain resource. [Unsplash](https://unsplash.com/index.html.md/index.html.md) is our preferred
resource for public domain images.

The cover image has the following proportions:

- On the [blog landing page][blog]: 1275px x 750px w/h = 1.7
- On blog post page (widescreen/index.html.md): 1920px x 550px w/h = 3.5

Try to have them harmonically aligned with the title, which overlays the background image in both cases. To crop the image, use the size of 1275x750 px. If you want to align the background image with the title overlay, use the widescreen proportion.

In the absence of a custom cover image, you can use one of these:

- GitLab Default: `'/images/default-blog-image.png'` (purple background and the Tanuki logo/index.html.md)
- Blog Default: `'/images/blogimages/gitlab-blog-cover.png'` (purple background, the Tanuki logo and "GitLab"/index.html.md)

Please only use the default images where there is genuinely no other option.

Please [add a reference](#image-a/index.html.md) to the cover image source, owner, and license at the end of the blog post, even if it doesn't require attribution.

#### Featured

Add `featured: yes` to the frontmatter of a post to create a featured post. The two most recent featured posts will be shown at the top of the blog in the featured section (even if more are tagged/index.html.md). To remove a post from being featured, remove the `featured: yes` line from the frontmatter.

#### Categories

Use only **one** of the following categories per post.
**Do not** change the capitalization, spelling, or anything else,
otherwise you'll create another category, which is something we don't want to do accidentally.

- `releases` â€ release posts, security updates, patch releases, etc.
- `engineering` â€ technical, actionable content. Anything covering how to do something, use something, or solve a problem should fall under this category
- `open source` â€ stories from or about our community, users, or the wider open source community
- `culture` â€ posts about remote work, working together, or GitLab culture
- `insights` â€ industry, data, newsjacking, developer survey, etc.
- `company` â€ company or product announcements, policy changes, events, etc.

We're working on improving category pages and tagging, but for now you can find posts under the same category by navigating to
`https://about.gitlab.com/blog/categories/category-name/`. Dashes will be automatically added
to multi-word categories and all of them will be lowercased in the URL. For example, the
category "company" will be available under `https://about.gitlab.com/blog/categories/company/`.

Note that there's a CI test that checks for wrong or missing categories. If one of
the above should change or a new category is added, don't forget to edit the
following files:

1. [`Rakefile`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/Rakefile/index.html.md) (search for `CATEGORIES`/index.html.md) - responsible for the CI test
1. [`source/includes/blog/category-nav.html.haml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/source/includes/blog/category-nav.html.haml/index.html.md) - responsible for the categories navbar
1. [`sourcehttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/blog/index.html.md`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/sourcehttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/blog/index.html.md/index.html.md) - the handbook which you're currently reading
1. If a category changes, you need to replace it in all posts. Here's a one-liner command you can run:

    ```sh
    find ./source/posts -type f -exec sed -i 's/categories: old/categories: new/' {} \;
    ```

    where `old` is the old category and `new` is the new one.
1. In case of a category change, a redirect should be added in <https://gitlab.com/gitlab-cookbooks/cookbook-about-gitlab-com> (internal/index.html.md).
   This is the last step after all the above are merged into `master` and deployed. Ask a production engineer to help you.

#### Description
The [`description`](https://moz.com/learn/seo/meta-description/index.html.md) meta tag [is important][description-tag]
for SEO, and is what appears on the [blog index page](/blog/index.html.md). It is also part of [Facebook Sharing][og] and [Twitter Cards]. We set it up in the
[post frontmatter](#frontmatter/index.html.md), as a short summary of what the post is about. Description is limited to 150, otherwise the text will be cut off on the index page.

It is mandatory for all the new posts, and it [has been included][MR-description] in the default post
frontmatter generated by [the command `rake new_post`](#create-a-new-post/index.html.md).

#### Tags
These are included to help readers find similar posts if they are interested in a particular subject. Tags appear at the bottom of each blog post, and clicking on a tag takes you to [/blog/tags](/blog/tags.html/index.html.md) where you can view all tagged posts and browse by tag.

You can include as many tags as you like, separated by commas. Please only include tags from the following list, and note that they are case sensitive. If you think a tag should exist that isn't on this list, please leave a comment for the reviewer on your MR saying which tag you'd like to use and why it should be included.

- agile
- careers
- CI
- cloud native
- collaboration
- community
- demo
- design
- developer survey
- DevOps
- events
- features
- frontend
- functional group updates
- git
- GKE
- google
- inside GitLab
- integrations
- kubernetes
- news
- open source
- patch releases
- performance
- [pick your brain](https://github.com/isamu-isozaki/teamai_test/tree/master/ea/#pick-your-brain-meetings/index.html.md)
- production
- releases
- remote work
- security
- startups
- testing
- UI
- user stories
- UX
- webcast
- workflow

#### Call to action
The CTA entry is optional; if you don't need to add any CTA to the hero, just omit both entries, leaving the frontmatter without them. Do not include any UTM parameters in the link. Always wrap their values with quotes.

The final result is a red button over the cover image of the post.

![Hero CTA preview](/imageshttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/hero-cta.png/index.html.md){:.shadow}

#### EE trial banner
To not display the EE trial banner on the blog post, set `ee_cta` to `false` in the frontmatter. It is set to true by default, so there's no need to add `ee_cta: true` to the frontmatter. Only set to false on the rare occasion you have a strong reason to not display the banner (usually in the case of posts that are for developers and our open source community/index.html.md).

#### Comments

Comments are present in all posts by default. Set it to false only if you have a strong reason to
do so (`comments: false`/index.html.md). They are our best source of feedback on posts.

### Images and illustration

Blog images are stored in the `source/images/blogimages/` directory. If your post contains many images, create a sub-directory for your post: `source/images/blogimages/name-of-post/`.

Illustrate your examples, with code blocks or screenshots. Be consistent along your examples. E.g., if you are using a generic URL
to exemplify your steps `domain.com`, be consistent and keep it `domain.com`, throughout the post.

- Static images should be used to illustrate concepts, provide diagrams, elements of the UI or orient the reader.
- Images should not be used to render commands or configuration which would prevent someone being able to copy and paste.
- Animated GIFs can be used sparingly where you need to show a process or some event happening over the course of time or several actions, though they should not replace text descriptions or instructions.
- Use screenshots to identify and localize specific parts of the screen. There are great tools for doing so. For example, Nimbus Screenshot (browser extension/index.html.md), Mac screenshot,Snipping Tool for Windows, and Screenshot Tool for Ubuntu.

**Important security point:** Do not expose your personal details by using your real tokens or security credentials. Use placeholders such as `[project's CI token]` stub instead. Or blur them if displayed on screenshots.

#### Preparing images

- Images should be cropped in a 1.7 width/height pixel *proportion* (ideally 1275px x 750px/index.html.md). This includes the cover image.
- All images should be less than 1MB. JPEGs tend to be smaller than PNGs so use JPEGs when possible. You can compress images using [TinyPNG.com][https://tinypng.com/] or any other image editor.
- Keep all the images the same width.

#### Image attribution

The only images accepted for about.GitLab.com are public domain images and screenshots. Whenever you choose an image which is not a screenshot, add a link to the original image to the merge request description and as an HTML comment:

```html
<!-- image: image-url -->
```

Do the same for [cover images](#cover-image/index.html.md), adding a link to the original image to the end of the post as a comment and to the MR description:

```md
----

Cover image: ["Image title"](link-to-original-image/index.html.md) by [owner name and surname](link/index.html.md), licensed under [CC X](link-to-licence/index.html.md).
{: .note}
```

If the image does not have a title, default to the following format:

```md
----

[Cover image](link-to-original-image/index.html.md) by [owner name and surname](link/index.html.md), licensed under [CC X](link-to-licence/index.html.md).
{: .note}
```

#### Inline images

To add an image inline, insert the following into your markdown file, where you want the image to appear:

```md
![Alt text for your image](/images/blogimages/your-image-filename.jpg/index.html.md){: .shadow}
```

The alt text for your images should describe the content and function of your image for visitors using a screen reader.

#### Sizing and aligning images

There are new classes for sizing and positioning blog post images. They should be added to blog post images similar to how the `shadow` class is added already:

``` md
![Your image alt text](/images/blogimages/your-image-filename.jpg/index.html.md){: .shadow.small.left.wrap-text}
```

The new classes are grouped into:

**Size**

- `.medium`: Display image 75 percent of page width
- `.small`: Display image 50 percent of page width

**Position**

- `.left`: aligned left (default/index.html.md)
- `.center`: centered
- `.right`: aligned right

**Effect**

`.wrap-text`: Only applies to images that are positioned left or right. Makes text wrap around the image.

These classes are only applied for screens 992px wide and and wider.

If a Position class is used without an Effect class then there will simply be empty space where the image isn't. Similarly, using a Position class without a Size class will have little-to-no effect.

#### Image captions

Insert the following beneath an inline image to include a caption:

```md
  *<small>Insert caption text here</small>*
```

#### Creating GIFs

Animated GIFs are very useful to illustrate short dynamic processes, which might be easier to understand with this kind of resource.
There are a few ways to create animated GIFs, one of them is using [Giphy Capture], a light-weight app for Mac.

Avoid GIFs with a huge file size, they will be difficult to load for users with bad internet connection. In those cases, you can either cut the GIFs in smaller pieces, or record a video, or use a sequential image.

Read more on Making Gifs in the Product Handbook.

#### Artwork and editable image files

If you have used a bitmap or vector editing software to create illustrations,
diagrams, or any other kind of images for your blog post, save the editable
files in the [General Marketing](https://gitlab.com/gitlab-com/marketing/general/index.html.md/index.html.md)
project. To do that, create a directory under [`/design/web-design/about-gitlab-com/blog/images/`](https://gitlab.com/gitlab-com/marketing/general/tree/master/design/web-design/about-gitlab-com/blog/images/index.html.md)
using the same naming logic from [Naming images](#naming-images/index.html.md) and place your
files there.

### Click to tweet

Consider adding pull quotes as click-to-tweet boxes, to encourage and make it easier for readers to share key points from your blog post. This only works for blog post files with the extension `.html.md.erb`.

To add a click-to-tweet box, copy the below partial and enter the `text` and `author` fields. If the author doesn't have a Twitter account you can use `gitlab` instead.

`<%= partial "includes/blog/tweet", locals: { text: '', author: '' } %>`

Example:

```
<%= partial "includes/blog/tweet", locals: { text: 'The Operations experience then should really just be that I go to work in the morning and see an email summary of what has happened, without me having to do anything', author: 'MarkPundsack' } %>
```

Renders:

  ![Click to tweet](/imageshttps://github.com/isamu-isozaki/teamai_test/tree/master/marketing/click-to-tweet.png/index.html.md){: .shadow}

---
