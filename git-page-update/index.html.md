---
layout: markdown_page
title: "Edit this website locally"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Introduction

This is a guide on what you'll need to install and run on your machine so you can make edits locally. This is quicker than in the web interface and allows you a better overview and preview when making complex changes.

## 1. Help is available for team members

If you work for GitLab Inc. we don't expect you to figure this out by yourself.
If you have questions ask anyone for help, you're more likely to have success with:

- People that have been here longer than 3 months, the [team page](/team/) lists people in order of how long they have been here.
- People that have engineer in their title.
- We encourage you to meet someone new by asking someone you don't know for help. You can also ask for help in #questions or #peopleops by posting 'Who can do a video call with me to help me work on the website locally /handbook/git-page-update/ ?'. If the other options don't work for you please ask your buddy.

## 2. Start using GitLab

1. Here's where you can find step-by-step guides on the [basics of working with Git and GitLab](https://docs.gitlab.com/ee/gitlab-basics/README.html). You'll need those later.
1. Create your [SSH Keys](https://docs.gitlab.com/ee/gitlab-basics/create-your-ssh-keys.html).
1. For more information about using Git and GitLab see [GitLab University](https://docs.gitlab.com/ee/university/).

## 3. Install Git

1. Open a terminal.
1. Check your Git version by executing: `git --version`.
1. If Git is not installed, you should be prompted to install it. Follow this [guide](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html) to installing Git and
linking your account to Git.

## 4. Install RVM

1. Visit [https://rvm.io](https://rvm.io/).
1. In a terminal, execute: `curl -sSL https://get.rvm.io | bash -s stable`.
1. Close terminal.
1. Open a new terminal to load the new environment.

## 5. Install Ruby and Bundler

1. In a terminal, execute: `rvm install 2.4.4` to install Ruby
   (enter your system password if prompted).
1. Execute: `rvm use 2.4.4 --default` to set your default Ruby to `2.4.4`.
1. Execute: `ruby --version` to verify Ruby is installed. You should see:
   `ruby 2.4.4p296 (2018-03-28 revision 63013)`.
1. Execute: `gem install bundler` to install [Bundler](http://bundler.io/).

## 6. Clone the source of the website and install its dependencies

1. If you set up SSH keys previously, in terminal execute: `git clone git@gitlab.com:gitlab-com/www-gitlab-com.git` to clone the website. If you prefer using https, then execute: `git clone https://gitlab.com/gitlab-com/www-gitlab-com.git`, but note that if you've activated 2FA on your GitLab.com account, you'll need to take some additional steps to set up [personal access tokens](https://gitlab.com/profile/personal_access_tokens). If you ever want to switch between SSH and https, execute `git remote remove origin`, followed by `git remote add origin [..]` where the `[..]` is the part that starts with `git@` for SSH, or with `https:` for https.
1. Execute: `cd www-gitlab-com` to change to the `www-gitlab-com` directory.
1. Execute: `bundle install` to install all gem dependencies.

## 7. Prevent newlines from causing all following lines in a file to be tagged as changed

This is especially a problem for anyone running a Mac OSX operating system. The
command to 'tame' git is `git config --global core.autocrlf input` - execute it.

## 8. Preview website changes locally

1. In a terminal, execute: `bundle exec middleman`.
1. Visit [http://localhost:4567/](http://localhost:4567/) in your browser.
1. You will need to install a text editor to edit the site locally. We recommend
   [Sublime Text 3](http://www.sublimetext.com/3) or [Atom](https://atom.io/). Use command / ctrl P to quickly open the file you need.
1. Refresh your browser to see your changes.

## 9. Test if all URL links in a page are valid

Until this is automated in CI, a quick way to see if there are any invalid
links inside a page is the following.

1. Install the [check-my-links](https://chrome.google.com/webstore/detail/check-my-links/ojkcdipcgfaekbeaelaapakgnjflfglf/) extension in Chrome (no other browsers
   support unfortunately).
1. Open the page you wish to preview (see previous step).
1. Click the newly installed extension in the upper right corner of Chrome.

A pop-up window will open and tell you how many links, if any, are invalid.
Fix any invalid links and ideally any warnings, commit and push your changes,
and test again.

All internal links (links leading to other parts of the website) should be relative.

## 10. Start contributing

Most pages that you might want to edit are written in markdown [Kramdown](http://kramdown.gettalong.org/).
Read through our [Markdown Guide](/handbook/product/technical-writing/markdown-guide/) to understand its syntax and create new content.

Instructions on how to update the website are in the
[readme of www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/README.md).

## 11. Add yourself to the Team Page

We are happy to have you join our company and to include you in our [team page](/team/). Please follow the instructions and links below that will guide you through each step. There are instructions for both the web interface and locally, depending on your familiarity with git. Feel free to ask anyone at the company questions along the way.

### Add on GitLab.com (Web IDE)

  1. You should have received an invitation to the [www-gitLab-com project](https://gitlab.com/gitlab-com/www-gitlab-com) at your GitLab email account. After creating your account, take note of your username and password, because you will need them throughout these steps.
  2.  Find the picture that you'd like to add to our team page, change the picture's name to the following format: `yournameinlowercase.jpg` or `yournameinlowercase.png`. (There should be no space between first and last names e.g. firstlast.jpg or firstlast.png) Ensure the picture size is around 400x400 (*it must be square*) and the format is JPEG or PNG. You can resize your picture using a photo editor like [GIMP](http://www.gimp.org/) (cross-platform) or online by searching for "image resize". Any picture that you provide will be made black-and-white automatically after you add it to the team page.
  3. Go to the [GitLab.com / www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com/) project.
  4. On the project page, click on the button labeled `Web IDE` near the middle of the page next to History and Find File buttons.
  5. In the file browser, navigate to `source/images/team`.
  6. Click the `⋁` icon next to the `team` directory and choose upload file and choose the photo you prepared in step 2.
  7. Next, navigate to in the file browser `data/team.yml` and click on it to open the editor.
  8. Your information should already be added towards the bottom of this file. Search the page for your name or initials if you are new. If your name is not listed, copy the last employee’s markdown text and paste it immediately after their bio to create a new bio.
  9. Update the initials to be your `Firstname 'Nickname' Lastname`. Verify that your title is entered correctly.
  10. If your manager is not filled in the `reports_to` field, then look for your manager's name and fill in that field with the `slug` for their name.
  11. Add the filename of the picture that you uploaded previously, and be sure to remove the "../" before the name of the file.
  12. Enter your Twitter and GitLab handle (without starting with an @) and write a story about yourself. Don't forget you can use other team members' information as a reference and to respect the spaces between lines. Please don't use "tab" because it will break the page format.
  13. Once you have finished this, click the `Commit` button in the bottom left. It should say something like `2 unstaged and 0 staged changes`. This will bring up a sidebar with an `Unstaged` and `Staged` area.
  14. Check the file to ensure your updates are what you expect. If they are, click the check mark next to the filename to "stage" these changes.
  15. Once you have verified all of the edits, enter a short commit message including what you've changed. Choose `Create a new branch and merge request`. Choose a branch name of your choosing, usually in the format of `<initials>-team-page` or similar. Then click commit once more. 
  16. Fill out the merge request details and assign it to People Ops for review (the recommended assignee would be the Talent Operations Specialist who helped you with onboarding).

### Add on GitLab.com (web interface)

  1. You should have received an invitation to the [www-gitLab-com project](https://gitlab.com/gitlab-com/www-gitlab-com) at your GitLab email account. After creating your account, take note of your username and password, because you will need them throughout these steps.
  2.  Find the picture that you'd like to add to our team page, change the picture's name to the following format: `yournameinlowercase.jpg` or `yournameinlowercase.png`. (There should be no space between first and last names e.g. firstlast.jpg or firstlast.png) Ensure the picture size is around 400x400 (*it must be square*) and the format is JPEG or PNG. You can resize your picture using a photo editor like [GIMP](http://www.gimp.org/) (cross-platform) or online by searching for "image resize". Any picture that you provide will be made black-and-white automatically after you add it to the team page.
  3. In [GitLab.com](https://gitlab.com/), select the GitLab.com/www-gitlab-com project.
  4. Click on "Files" (under "Repository" on the left-hand side menu).
  5. Select Source, Images, then Team.
  6. At the top of the page select “+” and upload the file. Note that your team page picture should be added to `www-gitlab-com/source/images/team/NAME-OF-PERSON-IN-LOWERCASE.jpg`.
  7. Commit these changes with a specific commit message “add NAME to team page” and a unique branch. Remember the branch name as you will use it in the following steps.
  8. [Create a merge request](https://docs.gitlab.com/ee/gitlab-basics/add-merge-request.html) in [GitLab.com](https://gitlab.com/) with the branch that you created with your picture.
  9. Go back to the GitLab.com project. Find the branch dropdown menu at the top of your screen (default value is "master") and find the branch that you previously created to add your picture (they are in alphabetical order).
  10. Information displayed on Team page is pulled from a data file. You can find it by clicking on each of the following items: Files, `data/`, and then `team.yml`.
  11. When you are in `team.yml`, click on “edit” on the top right side of your screen.
  12. Your information should already be added towards the bottom of this file. You can use `cmd + F` to search the page for your name or initials if you are new. If it’s not, copy the last employee’s markdown text and paste it immediately after their bio to create a new bio. Update the initials to be your `Firstname 'Nickname' Lastname`. Verify that your title is entered correctly. Add the filename of the picture that you uploaded previously, and be sure to remove the "../" before the name of the file. Enter your Twitter and GitLab handle (without starting with an @). Write a story about yourself. Don't forget to use other team members' information as a reference and to respect the spaces between lines. Please don't use "tab" because it will break the page format.
  13. After you added your information, add a comment to your commit and click on “Commit Changes”.
  14. Go to the Merge Request that you previously created with the branch that you are using. Assign it to People Ops for review (the recommended assignee would be the Talent Operations Specialist who helped you with onboarding).

### Add Locally (using the terminal)

  1. You should have received an invitation to the [www-gitLab-com project](https://gitlab.com/gitlab-com/www-gitlab-com) at your GitLab email account. After creating your account, take note of your username and password, because you will need them throughout these steps.
  2. Download Git, following the [start using git documentation](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html). Don't forget to add your Git username and to set your email.
  3. Follow the steps to create and add your [SSH keys](https://docs.gitlab.com/ee/gitlab-basics/create-your-ssh-keys.html). Note: in some of these steps, your [shell](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html) will require you to add your GitLab.com username and password.
  4. Clone the www-gitlab-com project through your shell, following the [command line commands documentation](https://docs.gitlab.com/ee/gitlab-basics/command-line-commands.html).
  5. Create and checkout a new branch for the changes you will be making.
  6. Find the picture that you’d like to add to our team page, change the picture's name to the following format: `yournameinlowercase.jpg` or `yournameinlowercase.png` (There should be no space between first and last names e.g. firstlast.jpg or firstlast.png) and then add it to the `source/images/team/` directory. Follow the "[how to add an image](https://docs.gitlab.com/ee/gitlab-basics/add-image.html)" steps. Ensure the picture size is around 400x400 (it must be square) and the format is JPEG or PNG. You can resize your picture using a photo editor like [GIMP](http://www.gimp.org/) (cross-platform) or online by searching for "image resize". Any picture that you provide will be made black-and-white automatically after you add it to the team page.
  7. Add the picture so it is staged for commit.
  8. Information displayed on the Team page is pulled from `data/team.yml`.
  9. Your information should already be added towards the bottom of this file. If it’s not, copy the last employee’s markdown text and paste it immediately after their bio to create a new profile. Update the initials to be your `Firstname 'Nickname' Lastname`. Verify that your title is entered correctly. Add the file name of the picture that you uploaded previously. Enter your twitter and GitLab handle. Write a story about yourself. Don't forget to use other team members' information as a reference and to respect the spaces between lines. Please don't use "tab" because it will break the page format.
  10. After you added your information and saved your changes, add the file to be staged for commit.
  11. To see your changes locally, follow the directions in `README.md`.
  12. After validating your changes, commit your changes with a comment and push your branch.
  13. [Create a Merge Request](https://docs.gitlab.com/ee/gitlab-basics/add-merge-request.html) in [GitLab.com](https://gitlab.com/) with the branch that you created. Assign it to People Ops for review (the recommended assignee would be the Talent Operations Specialist who helped you with onboarding).

### Add your pet(s) to the Team Pets Page

  Using what you learned in the [steps above](git-pages-update/#11-add-yourself-to-the-team-page), consider adding your pet to the [Team Pets page](https://about.gitlab.com/team-pets/). You can follow these instructions for adding them via the Web IDE.

  1. Again, find the picture that you'd like to add to the team pets page, and update the picture's name to the following format: `petname.jpg` or `petname.png`. Ensure the picture size is around 400x400 (*it must be square*).
  1. Go to the [GitLab.com / www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com/) project.
  1. On the project page, you will see a Web IDE button near the middle of the page next to History and Find File buttons.
  1. In the file browser, navigate to `source/images/team/pets`.
  1. Click the `+` icon next to the `team` directory and choose upload file and choose the photo you prepared in step 1.
  1. Next, navigate to in the file browser `data/pets.yml` and click on it to open the editor.
  1. Add your pet by following the format of the existing pets on the page (you can copy and paste their lines of code, even). Ensure that you include your pet's name, your name, and the image you uploaded in step 1.
  1. Once you have finished this, click the `Commit` button in the bottom left. It should say something like `2 unstaged and 0 staged changes`. This will bring up a sidebar with an `Unstaged` and `Staged` area.
  1. Check the file to ensure your updates are what you expect. If they are, click the check mark next to the filename to "stage" these changes.
  1. Once you have verified all of the edits, click commit once more. Here, enter a short commit message including what you've changed. Choose `Create a new branch and merge request`. Choose a branch name of your choosing.
  1. Fill out the merge request details and assign it to People Ops for review (the recommended assignee would be the Talent Operations Specialist who helped you with onboarding).

## 12. Edit the Handbook

### WebIDE, using the browser
The Web Integrated Development Environment (IDE) is used to make changes within the browser. This method requires no setup.

1. Find the handbook page to edit.
1. Click on the `Edit this page` button at the bottom of the page.
1. On the page, you should see the relevant file in the repository displayed. Click on the `Web IDE` button on the right side.
1. Edit the page using [MarkDown](/handbook/product/technical-writing/markdown-guide/). You can preview your changes (but links will not work).
    * Note: You can edit other pages by browsing through the filelist on the left side in the Web IDE.
1. When done, click on the `Commit...` button on the bottom left. You will see the differences between the original file and your changes.
1. Add a commit message. The message should be as brief as possible, since it has a character limit. You can add more detail in the description in a subsequent step.
1. Choose the option to create a new branch and create merge request. For your branch, use a descriptive name with hyphens, so that you can find it again later, but it's temporary so don't worry too much about the exact name. 
1. Submit and you will be taken to the merge request (MR) page.
1. Feel free to add a more detailed message in the description box. For the options, check `Remove source branch` and `squash commits`.
1. Assign the MR to the Handbook Content Manager (or as instructed) for general handbook changes. If the content changes are specific to your team, assign the MR to your manager.

### Locally, using the terminal

  1. If you haven't already, follow steps 1-5 in the "Add yourself to the Team Page"'s "Add Locally (using the terminal)" section above.  (This step is necessary as the handbook lives in the same repository as the rest of GitLab.com).  If you're following this guide in order and have already added yourself to the team page, instead go back to the main branch (via `git checkout master`) and there create a new branch for your handbook edits.
  2. The handbook lives under `source/handbook`.  For the most part, you can locate the specific item to edit via that item's URL.  For instance, this page is /handbook/git-page-update/ and its source lives in `source/handbook/git-page-update/index.html.md`.
  3. Edit away!  See the "Start Contributing" section, above, for details about the Markdown that most pages are written in.
  4. Preview your changes locally by following the directions in `README.md`.  Keep in mind that the local server won't auto-reload when you change a page, so you'll need to restart it to see what you've done.
  5. Once you've made your changes and verified they appear the way you want them to, commit them with a comment and push your branch.
  6. As above, [Create a Merge Request](https://docs.gitlab.com/ee/gitlab-basics/add-merge-request.html) in the [www-gitlab-com project](https://gitlab.com/gitlab-com/www-gitlab-com).  If you're onboarding, don't forget to assign it to your manager.

## Example video

<iframe width="560" height="315" src="https://www.youtube.com/embed/v6QbZMUpF28" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Where should content go?
GitLab has a lot of places you can put web content including the [website](/handbook/marketing/website/), [blog](/handbook/marketing/blog/), [docs](https://docs.gitlab.com/ee/development/documentation/index.html), and the [handbook](/handbook/handbook-usage/). Here's an overview of where you should create a merge request to add content.
1. **[blog](/handbook/marketing/blog/)**: The blog is a great place to start. If you don't know where to put content, then write a blog post! Great blogs can always be then copied or modified for the website, docs, and handbook later. Blog posts are especially good for news, annoucements, and current trends because blog posts are tied to a specific date.
1. **[website](/handbook/marketing/website/)**: This is the main marketing site for GitLab and where folks will tend to go first to find out information about GitLab (the product and the company). The website contains a broad set of content from [product pages](/product) to [customer case studies](/customers). The website is the best place for [evergreen](https://www.wordstream.com/blog/ws/2012/10/16/guide-to-evergreen-content-marketing) articles such as [topic](/handbook/marketing/website/#topics) and [solution](https://about.gitlab.com/handbook/marketing/website/#solutions) pages since it's not tied to specific date.
1. **[docs](https://docs.gitlab.com/ee/development/documentation/index.html)**: The docs are where are all technical information about GitLab self-managed and GitLab.com belongs. If the intended audience for the content is a user of GitLab then it should be in the docs. The docs are great place for both refernce docs (what are the configurable settings for a feature, e.g. [what can you do with issues](https://docs.gitlab.com/ee/user/project/issues/index.html)) and narrative docs (how to do x with y, e.g. how to set up [HA on AWS](https://docs.gitlab.com/ee/university/high-availability/aws/README.html#doc-nav)).
1. **[handbook](/handbook/handbook-usage/)**: The handbook is for any content that needs to be [used by GitLabbers to do thier job](https://about.gitlab.com/handbook/handbook-usage/). If you put content on the blog, website, and docs, but you think it would be helpful for GitLabbers to do thier job then link to the content from the handbook.  

Sometimes the lines are blurry and it can seem as though there are multiple places that would be a good fit. For example, "how to" articles make great blog posts, but could be more discoverable to users if they are in the docs. Just pick one. It's better to create content somehwere than nowhere. When in doubt, start with the blog.
