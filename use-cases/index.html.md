---
layout: markdown_page
title: "Customer Use-Cases"
---
**Customer Use Cases:**
A customer use case is:
* A problem or initiative that a customer needs to solve.  
* These are discrete problems that we believe GitLab can solve (hence which we should seek out in prospects/index.html.md)

**Specific Use Cases**
* **Portfolio Management:** The goal of portfolio management is to determine the optimal resource mix for delivery and to schedule activities to best achieve an organization’s operational and financial goals, while honoring constraints imposed by customers, strategic objectives, or external real-world factors. Examples in GitLab include epics, roadmaps, and milestones.
* **Project Management:** Project management is the practice of initiating, planning, executing, controlling, and closing the work of a team to achieve specific goals and meet specific success criteria at the specified time. Examples in Gitlab include Issues, Issue Boards, Issue Weights, Labels, Milestones, and burndown charts.
* **Source Code Management:** Source code management is the management of changes to documents, computer programs, large web sites, and other collections of information. Examples in GitLab include Branches, Merge Requests, WebIDE, and files.
* **Continuous Integration (CI/index.html.md):** Continuous Integration automates the build and testing processes to implement continuous processes of applying quality control in general � small pieces of effort, applied frequently. In addition to running the unit and integration tests, such processes run additional static and dynamic tests, measure and profile performance, extract and format documentation from the source code and facilitate manual QA processes. Examples in GitLab include Pipeline, CI Runner, Jobs, Scheduled Jobs, Testing, Security Scanning (SAST/index.html.md), and Code Quality.
* **Continuous Delivery:** Continuous Delivery automates the packaging, configuration and deployment of applications to a target environment.  Examples in GitLab include: CI Runner, Container Repository, Deploy Boards, Canary Deploys, Partial Deploys, Manual Deploys, Environments.
* **Safer Deployments:** Being able to deliver changes to production while minimizing risk to production systems.  A subset of Continuous Delivery.  Examples in GitLab include: Canary Deploys, Partial Deploys, and Feature Flags.
* **Dynamic Environments for SDLC:** The ability to create non production environments in support of the development process.  Examples in GitLab include Review Apps, containers and kubernetes integration.
* **Application Security:** Evaluating the risk and security exposure of an a code change. Application security is in the form of static and dynamic scanning to identify sources of risk within the application.  In GitLab, SAST, DAST, Dependency Scanning, and Container Scanning.
* **Application Configuration Management:**  Application configuration use case includes the desire to configure the application environment and the application itself during and after deployment. Examples are the need to scale up an application’s resources, or turning on and off various features by using feature flag configuration.
* **Application Monitoring:** Monitoring application performance and feedback is a most critical step in the DevOps lifecycle.  Product teams need to understand how their changes impact the business value of their applications.  Examples in GitLab include Application Performance monitoring, server monitoring, Kubernetes Cluster Monitoring, and Kubernetes pod log review.
* **End to End DevOps:** GitLab is designed to manage the entire DevOps lifecycle in a single application.  Beginning with managing ideas and projects through the full SDLC and to production.  In GitLab, this would mean using Epics, Issue Boards, Source Code Management, CI, CD, Security Scans and Monitoring from GitLab.
* **Value Stream Management:**  Value streams help you visualize and manage the flow of new innovation from ideas to customers. In GitLab, cycle analytics is a key elements of managing the value stream.
* **Integration - Planning:** Integrations with Project Planning tools like: VersionOne, Rally, Jira, Trello, Monday, Workfront, and Basecamp.  Or integrations with Portfolio Planning tools like Clarity, MicroFocus PPM, or others.
* **Integration - SCM(GitHub/index.html.md):** The most common SCM integration is with GitHub
* **Integration - CI:**  Integrations with Jenkins, Circle CI, Bamboo or other CI servers.
* **Integration - CD:** Integrations with common CD tools such as Puppet, Chef, Ansible, Jenkins and others.

**Non-Use Cases:**
* To be filled in based on FANUC (frequently asked non-use cases/index.html.md)

**Specific Examples**

1. Using JIRA with GitLab EE
    * A company in the healthcare space had been using EE for about a year now,
    and the number one reason they decided they could make the move to GitLab EE
    was because it works well with JIRA. They had been using JIRA for years, so
    any interruption to this workflow would not be easy for them. Because GitLab
    works well with JIRA, they were able to move over quickly and found features
    like referencing JIRA issues in GitLab merge requests, issues, and commits,
    as well as the ability to close JIRA issues with GitLab commits to be easy
    for them.
    * Placeholder to add another story
1. Using Jenkins with GitLab EE, then trying GitLab Integrated CI
    * Like the case above, another company had been using Jenkins as their CI
    tool for a long time. As they were evaluating GitLab and found we had a
    Jenkins CI integration, this allowed them to make the move to GitLab EE
    without disrupting what their team was already use to. Being able to
    display merge request status for builds on Jenkins CI within GitLab was the
    number one reason they decided to make the move to EE. They also became
    aware of GitLab's recently implemented Integrated CI, which their users have
    started to test and are finding it may be a solution that ends up working
    better for them.
    * Placeholder to add another story
1. Moving from CE to EE
    * A long time CE user decided to move their company to EE as they grew from
    10 users to 120 in 2 years. Their needs changed, so features like LDAP
    Group Sync that allowed the Admin. to manage group's and their permission
    levels easier, were essential. Another key feature in EE that they now
    needed was Git Hooks. They wanted to prevent git tag removal from their
    users, so implementing a Git Hook allowed them to now do this. On top of
    these features, they were happy to discover how easy it was to upgrade to EE
    from CE simply by using the Omnibus package.
    * Placeholder to add another story
1. Using High Availability with GitLab
    * A current Standard Subscriber decided they wanted to move from having a
    single instance on GitLab EE, to having an HA setup. GitLab offered them
    multiple HA solutions, and after speaking with our Support Engineer's, they
    decided that using two machines with one being a single slave server was
    their best option. What was important to them was each machine had all of
    their GitLab repositories, configuration, and the database. With the slave
    server being a copy of the master, they used DRBD to ensure their data from
    the master is being replicated to the slave server in a timely manner. This
    of course made everyone feel better :/index.html.md)
    * Placeholder to add another story
1. Access to your server and security
    * A customer in the banking industry had security as their number one
    concern. An on-premises solution like GitLab EE is exactly what they needed
    as it allowed them to have access to their own server, view log files, and
    they could also install additional software like intrusion detection. Since
    GitLab EE also comes with Audit Events, they could have a history and view
    changes made within the GitLab server which was of extreme importance to
    them.
    * Placeholder to add another story
1. Importing repos and files from GitHub
    * Placeholder to add story
    * Placeholder to add another story
1. Migrating from SVN to Git
    * Placeholder to add story
    * Placeholder to add another story
1. Protected Branches
    * The customer had been using Bitbucket and was not able to limit developer
      permissions to specific branches and repositories.  They had an ongoing
      problem with developers accidentally pushing branches to the wrong project
      or without proper code review. They decided to switch to GitLab because
      we offer protected branches with more of a fine grained level of
      permissions at the Master level.
    * Placeholder to add another story
