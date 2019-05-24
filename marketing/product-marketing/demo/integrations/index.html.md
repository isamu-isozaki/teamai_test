---
layout: markdown_page
title: "Integration Demos"
---

# On this page
{:.no_toc}

- TOC
{:toc}

In some cases, GitLab must be used with existing systems. The most common systems requested include Atlassian Jira for issue management, Jenkins for pipeline execution or GitHub for source code management. Jira to GitLab workflow, GitHub to GitLab CI/CD linkage or GiLab to Jenkins connections can be arranged quickly on a per-project basis using available integrations from GitLab.

The below demonstration highlights a simple flow of work between Jira issues and GitLab source code management, as well as between GitLab merge requests and Jenkins pipelines.

<figure class="video_container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/Jn-_fyra7xQ" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</figure>

The below demonstration highlights a simple flow of work between GitHub pull requests and GitLab CI/CD.

<figure class="video_container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/qgl3F2j-1cI" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</figure>

# Jira Integration Demo

* Log into Jira via the `Jira Integration Demo Login` in 1Password.
* Select the `spring-integrations` project in Jira and go to the issue board.
* Create a new Jira issue. Note the ID or copy it to the clipboard.
* Log into GitLab `spring-integrations` project on `demo.tanuki.cloud` via 1Password.
* Create a branch from Repository>Branches. Include your new Jira issue ID in branch name and description (such as _fixes SI-X_, where _X_ is the issue number/index.html.md).
* Create a merge request with _SI-X_ in the name and _Resolves SI-X_ in the description.
* Edit any non-essential code within the repository, then enter a commit message mentioning _SI-X_ again.
* Go to Jira again via the link in the GitLab menu.
* Manually sync GitLab and Jira for the commit and branch data to show up. It takes 60 minutes by default between syncs. Manually refresh the spring-integrations DVCS account in Jira by navigating to `System/Applications/DVCS` and clicking the circular icon next to the last activity date.
* Navigate to the Jira issue board and select the _SI-X_ issue in the `spring-integrations` project. Note the GitLab content now present in the Comments area, as well as the commit and branch information displayed in the Development panel on the right side.

# Jenkins Integration Demo

* Login to Jenkins using `Jenkins.Taunki.Cloud Login` in 1Password.
* Log into GitLab `spring-integrations` project on `demo.tanuki.cloud` via 1Password.
* Create a branch from Repository>Branches.
* Create a merge request.
* Edit any non-essential code within the repository and enter a generic commit message.
* Go to the created merge request and click on the pipeline to bring up the graphical view.
* Note the pipeline actually ran a Jenkins job in an `external` stage.
* Click on Jenkins job, noting that it takes you to the Jenkins console output.
* Return to the GitLab repository and highlight the Jenkinsfile maintained alongside the repo for consistency and versioning.

# Bamboo CI Integration Demo

* Log into GitLab using your credentials
* Create a new project from any template
* Delete `.gitlab-ci.yml`
* Login to Bamboo using `Bamboo Tanuki Cloud` in 1Password.
* Create a new plan by selecting `create -> create plan`
* Select an existing project or create a new project
* Specify a `plan name`
* Choose an existing repo or link to a new repository (credentials may be required when linking to a new repository/index.html.md)
* Keep `isolate build` set to `Agent Environment`
* Select `source code checkout` and enable `force clean build`
* Save the changes and drag the task into `final tasks`
* Select `Save and continue`
* Select triggers tab
* Delete default trigger and add a new `remote trigger`
* Specify the IP addresses associated with your demo GitLab instance (Keep in mind you will need to provide load balancing IPs/index.html.md)
* Make sure the plan is enabled
* Select `Run -> Run plan` to confirm the plan can build from GitLab
* Return to the GitLab project and select `settings -> integrations`
* Select `Atlassian Bamboo CI`
* Fill out all fields and make sure to set the integration to active
* If you are having trouble finding the build key, you can find it within the URL of the plan page within Bamboo
* Save changes and edit README.md to make a quick commit
* Check Bamboo dashboard to see build triggered
* Create new branch off of master
* Within the Bamboo plan configuration page `home page -> select plan -> 'actions > configure plan'`, select `create plan branch`
* Follow dialog and add new branch
* Edit README.md in new branch and commit the change
* Check Bamboo to confirm the change has been picked up by Bamboo

# OpenLDAP Integration Demo (Adding Users/index.html.md)

* Log into the OpenLDAP GUI (details can be found in the SA vault/index.html.md)
* In the left navigation panel, expand the LDAP tree
* Click on the `ou=users` organization unit
* In the main panel, click `Create a child entry`
* Select `Generic User Account` from the available templates a new user form will appear
* Enter the new users information in the provided form, ensuring all required fields are populated
* Click `Create Object`, you will be presented with the opportunity to check and finally `Commit`
* Commit the new user to LDAP by clicking the `Commit` button
* You will then be taken to the newly created user account
* Navigate to the GitLab login screen, here you will see the option to login using LDAP.
* Enter the user id and password used when creating your new user within OpenLDAP
* Click `Sign In`
* Newly created users will be taken to their profile page to update their `Email` field and confirm their Email address.

# GitHub Integration Demo

* Navigate to GitHub.com/signin and login using `GitHub Demo Login` in 1Password.
* Navigate to GitLab.com and login using `GitHub Demo Login (GitLab/index.html.md)` in 1Password.
* Begin the demo by showing how to create a GitLab project linked to a GitHub repo. Click on the `+` icon to create a new project in GitLab.
* Select the `CI/CD for external repo` tab and highlight that you’d use an access token from GitHub to access GitHub repos within GitLab. Don’t create a new project at this point (cancel/index.html.md).
* Switch to GitHub. Click into the `spring-boot-test` project repo.
* Create a new branch using the `Branch:master` button.
* Click into the `src/main/java/hello/HelloController.java` file and make a minor change to the screen message.
* Add a commit message and click the `Commit Changes` button.
* Click on the `Pull Requests` tab and click the `New pull request` button.
* Compare changes using `base:master` and `compare:yourbranch`.
* Click `Create pull request`.
* Scroll down a bit and note the amber wording `Some checks haven’t completed yet`.
* There is a GitLab logo when this check is expanded. Click the `Details` hyperlink inline with the GitLab logo.
* Note that you are taken directly to GitLab’s pipeline page in the associated project. This pipeline can take up to 10 minutes to run, but once complete, the pipeline status is returned to GitHub.
* While we wait for the pipeline to complete, note that the complete history is available for the pipelines run in GitLab.
* Also note that the repo and branches are mirroring from GitHub dynamically, but issue management and merge request options have bene removed from the GitLab UI since the GitHub issues and pull requests are used instead.
* After time has elapsed, return to the GitHub pull request to show the pass/fail status displayed in GitHub.
* Optional: Other existing pull requests may be used to show the linkage without committing changes or creating new pull requests.

# Conclusion

GitLab, leveraging built-in integrations, can work with existing Jira, GitHub or Jenkins systems, flowing work and updating status bi-directionally between those tools and GitLab.
