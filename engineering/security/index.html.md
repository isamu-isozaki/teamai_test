---
layout: markdown_page
title: "Security"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Security Vision

We enhance the security posture of our company, products, and client-facing services. The security team works cross-functionally inside and outside GitLab to meet these goals. The security team does not work directly on security-centric features of our platform—these are handled by the development teams. The specialty areas of our team reflect the major areas of information security.

## Security Department

### Security Automation

Security Automation specialists help us scale by creating tools that perform common tasks automatically. Examples include building automated security issue triage and management, proactive vulnerability scanning, and defining security metrics for executive review. Initiatives for this specialty also include:

 *  Assist other security specialty teams in their automation efforts
 *  Assess security tools and integrate tools as needed
 *  Define and own metrics and KPIs to determine the effectiveness of security programs
 *  Define, implement, and monitor security measures to protect GitLab.com and company assets

### Application Security

Application Security specialists work closely with development, product security PMs, and third-party groups (including paid bug bounty programs/index.html.md) to ensure pre and post deployment assessments are completed. Initiatives for this specialty also include:

 *  Pre and post deployment security assessments/tests
 *  Capture of flaws in software environment configuration
 *  Malicious code detection
 *  Patch/upgrade
 *  IP filtering
 *  Lock down executables
 *  Monitoring of programs at runtime to enforce the software use policy
 *  Developing and implementing a Secure Software Development Lifecycle (S-SDLC/index.html.md)
 *  Training and coaching developers on current security best practices

### Security Operations

Security Operations specialists respond to incidents. This is often a fast-paced and stressful environment, where responding quickly and maintaining ones composure is critical. Initiatives for this specialty also include:

 *  Focus on detection and incident response, as well as implement preventative mechanisms
 *  Coordinate company-wide responses to security incidents
 *  Incorporate current security trends, advisories, publications, and academic research
 *  Engineer CND technologies to monitor and analyze _e.g._
   *  IDSes
   *  Data collection tools
 * Conduct vulnerability management
   * Identify and mitigate complex security vulnerabilities before an attacker exploits them
   * Determine level of effort required to compromise sensitive data
   * Triage and manage vulnerabilities identified through scanning

### Abuse Operations

Abuse Operations specialists investigate malicious use of our systems. Initiatives for this specialty include:

 * Three main types of abuse
   * Continuous Integration
   * Copyright violations
   * Port scanning
 * Also investigate reports such as spam email, DoS, etc.
 * Take action on abusive/non-responsive customers
 * Verify proper classification of incoming abuse reports
 * Execute messaging to customers on best practices
 * Escalate to other stakeholders while continuing to monitor
 * Monitor logs and queues for trends
 * Research and prevent trending abuse methodologies

### Compliance

Compliance specialists enables Sales by achieving standard as required by our customers. This includes SaaS, on-prem, and open source instances. Initiatives for this specialty also include:

 * Develop roadmap based on customer needs _e.g._
   * GDPR
   * SOC 2
   * FIPS 140-2
 * Align other security specialist activities with the compliance roadmap
 * Develop relationships with key government personnel and policy makers
 * Assist work of internal and external auditors or advisors as needed

### Threat Intelligence

Threat intelligence specialists research and provide information about specific threats to help us protect from the types of attacks that could cause the most damage. Initiatives for this specialty also include:

*  Collect and analyze threat intelligence reports covering new threats, vulnerabilities, products, and research
*  Author threat intelligence reports, driven by our security operations team's own incidents, analysis, and adversary engagements
*  Evolve monitoring operations by extracting data from threat intelligence and create new content, signatures, and understanding of adversary TTPs
*  Analyze event feeds and collected malware over long term to trend and correlate

### Strategic Security

Strategic security specialists focus on holistic changes to policy, architecture, and processes to reduce entire categories of future security issues. Initiatives for this specialty also include:

*  Cluster related historical security issues and examine them as a larger set
*  Identify and generate trends associated with each set
*  Propose actionable changes to GitLab architecture, processes, and infrastructure to mitigate future issues within each set
*  Generate metrics which measure the effectiveness of each mitigation implemented

### Security Research

Security research specialists conduct internal testing against GitLab assets, and against FOSS that is critical to GitLab products and operations. Initiatives for this specialty also include:

*  Conduct vulnerability research against all GitLab and GitLab.com assets
*  Research FOSS tools that are integrated with GitLab
*  Develop proof-of-concept code to be included in security findings
*  Report findings to tool developers and track mitigation process
*  Follow responsible disclosure policies for community disclosure
*  Author blog posts on vulnerabilities discovered

## Security Team Collaborators

### Secure Team

The Security team will collaborate with development and product management for security-related features in GitLab.
The [Secure team]( ../ops-backend/secure/index.html.md) must not be mistaken with the Security Team.

*  Develop real-world security use cases
*  Ideation of compelling security features and products
*  Test and provide product feedback

### External Security Firms

We work closely with bounty programs, as well as security assessment and penetration testing firms to ensure external review of our security posture.

*  One security assessment firm is rotated periodically to gain new perspectives
*  One security assessment firm is engaged every quarter to build expertise in GitLab
*  We maintain public and private bug bounty programs via [HackerOne](https://hackerone.com/gitlab/index.html.md)
   * Private program paid bounties will increase over time and at some point we want to do public bounties

## Common Links

- Security crosses many teams in the company, but most often security related
issues are posted in the [public (!/index.html.md) security issue tracker](https://gitlab.com/gitlab-com/security/issues/index.html.md/index.html.md),
but they also appear in the [infrastructure issue tracker](https://gitlab.com/gitlab-com/infrastructure/issues/index.html.md/index.html.md),
or [gitlab-ce](https://gitlab.com/gitlab-org/gitlab-ce/issues/index.html.md/index.html.md), or even
[organization](https://gitlab.com/gitlab-com/organization/issues/index.html.md/index.html.md) trackers
with the `~security` label. Please use confidential issues for topics that
should only be visible to team members at GitLab.
- [Chat channel](https://gitlab.slack.com/archives/security/index.html.md); please use the `#security` chat channel for questions that don't seem appropriate to use the issue tracker or the internal email address for.
- [Frequently asked questions about Security of GitLab](/security/index.html.md) _the application_  as well as GitLab _the organization_  are documented on the top-level [security page](/security/index.html.md).
- [Security Best Practices](https://github.com/isamu-isozaki/teamai_test/tree/master/security/index.html.md), using 1Password and similar tools, are documented on their own [security best practices page](https://github.com/isamu-isozaki/teamai_test/tree/master/security/index.html.md).
- GitLab.com and GitLab Hosted [data breach notification policy](/security/#data-breach-notification-policy/index.html.md).
- For GitLab.com, we have developed a [Google Cloud Platform (GCP/index.html.md) Security Guidelines Policy](https://docs.google.com/document/d/1BBTWC5OpIqrva7DqH4nkjYUmNZ3UFbc6erqV89P_N-o/edit?usp=sharing/index.html.md) document, which outlines recommended best practices, and is enforced through our security automation initiatives.

## Security Topics

At a high level, the topic of security encompasses keeping GitLab.com safe, from the perspective of the application, the infrastructure, and the organization.

We track progress on tackling security related issues across the spectrum through an ["always WIP Risk Assessment"](#risk-assessment/index.html.md), and its associated (confidential/index.html.md) meta issue that is kept up to date to [list the top 10 actions](https://gitlab.com/gitlab-com/infrastructure/issues/1851/index.html.md) the team is working on.

## Security Releases

The definitions, processes and checklists for security releases are described
in the
[release/docs](https://gitlab.com/gitlab-org/release/docs/blob/master/general/security/process.md/index.html.md)
project.

The policies for backporting changes follow [Security Releases](https://docs.gitlab.com/ee/policy/maintenance.html#security-releases/index.html.md)
for Gitlab EE.

For critical security releases, refer to [Critical Security Releases](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/critical-release-process/index.html.md) in the handbook for a high level description of communication, and the [critical release checklist](https://gitlab.com/gitlab-org/release/docs/blob/master/general/security/critical.md/index.html.md) in `release/docs`.

## Issue Triage

The Security team needs to be able to communicate the priorities of security related issues to the Product, Development, and Infrastructure teams. Here's how the team can set priorities internally for subsequent communication (inspired in part by how the [support team does this](https://github.com/isamu-isozaki/teamai_test/tree/master/support/workflows/support_workflows/issue_escalations.html.md/index.html.md)/index.html.md).

### Creating New Security Issues

New security issue should follow these guidelines when being created on `GitLab.com`:

 * Create new issues as `confidential` if unsure whether issue a potential
   vulnerability or not.  It is easier to make an issue that should have been
   public open than to remediate an issue that should have been confidential.
   Consider adding the `/confidential` quick action to a project issue template.
 * Always label as `~security` at a minimum.
 * Add any additional labels you know apply.  Additional labels will be applied
   by the security team and other engineering personnel, but it will help with
   the triage process:
   * `~bug` or `~feature proposal` if appropriate
   * Team or devops lifecycle labels
   * `~customer` if issue is a result of a customer report     
 * Issues that contain customer specific data, such as private repository contents,
   should be assigned `~keep confidential`. If possible avoid this by linking
   resources only available to GitLab employess, for example, the originating
   Zendesk ticket.  Label the link with `(GitLab internal/index.html.md)` for clarity.

If necesary, a sanitized issue may need to be created with more general
discussion and examples appropriate for public disclosure prior to release.

For more immediate attention, mention `@gl-security` with a request in the issue
and use `@sec-team` in Slack.

### Severity and Priority Labels on `~security` Issues

The presence of `~security` modifies the standard [severity labels](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#severity-impact-guidance/index.html.md)(`~S1`, `~S2`, `~S3`, `~S4`/index.html.md)
by additionally taking into account
likelihood as described [below](#security-severity-labels/index.html.md), as well as any
other mitigating or exacerbating factors. The priority of addressing
`~security` issues is also driven by impact, so in most cases, the priority label
assigned by the security team will match the severity label.
Exceptions must be noted in issue description or comments.

The intent of tying `~S/~P` labels to release schedules is to measure and improve GitLab's
response time to security issues to consistently meet or exceed industry
standard timelines for responsible disclosure.  For non-release based resources
like infrastructure changes or other artifacts that do not have to follow the
monthly release schedule,

| Severity  | Priority  | Target Release   | Time to remediate (non-release resources/index.html.md) |
|-----------|-----------|------------------|-------------------------------------------|
| `~S1`     | `~P1`     | Critical Release | Immediate |
| `~S2`     | `~P2`     | Next Monthly Security Release | 30 days |
| `~S3`     | `~P3`     | Next 1-3 Releases | 90 days |

Security issues which are not at least `~S3`, are most likely `~feature
proposal`s that should be triaged and prioritized by a product manager. This
includes suggestions without a well-defined path for implementation or
requiring complex changes to the application or architecture to address.
`~S4/~P4` may be used for `~feature proposal`s as assigned by a product
manager and do not need assignment to a release.

#### Transferring from Security to Engineering

The security engineer will add team labels (`~Create`, `~Deploy`, etc./index.html.md) and any
additional labels as appropriate to the issue.  The engineering team lead should
be @ mentioned and followed up as necessary as noted below for different severity levels.

**Note that issues are not scheduled for a particular release unless the team leads add them to a release milestone *and* they are assigned to a developer.**

Issues with an `S1` or `S2` rating should be immediately brought to the
attention of the relevant engineering team leads and product managers by
tagging them in the issue and/or escalating via chat and email if they are
unresponsive.

Issues with an `S1` rating have priority over all other issues and should be
considered for a critical security release.

Issues with an `S2` rating should be scheduled for the next scheduled
security release, which may be days or weeks ahead depending on severity and
other issues that are waiting for patches. An `S2` rating is not a guarantee
that a patch will be ready prior to the next security release, but that
should be the goal.

Issues with an `S3` rating have a lower sense of urgency and are assigned a
target of the next minor version.  If a low-risk or low-impact vulnerability
is reported that would normally be rated `S3` but the reporter has
provided a 30 day time window (or less/index.html.md) for disclosure the issue may be
escalated to ensure that it is patched before disclosure.

### Security Severity Labels

Many factors affect the severity ratings of security isssues, but the
following guideline can can used as a starting point.  For this, consider
_severity_ as a combination of the _likelihood_ and _impact_ of a security
incident that could result from this issue not being resolved.

- **Likelihood:**  _For example: If left unresolved, can we expect to see an incident within a release cycle?_
  - L1 - Wide open gap easily found, or perhaps even ways for the incident to be triggered _accidentally_ .
  - L2
  - L3 - Unlikely an incident would occur (hard to find vulnerability, super
    edge cases/index.html.md).
- **Impact:** _For example: Can data be lost or compromised as a result?_
  - I1 - Any data loss. Or data exposed of many users.
  - I2
  - I3 - Meta data exposed (e.g. number of merge requests pushed/index.html.md) of some users

| **Likelihood \ Impact**          | **I1 - High** | **I2 - Medium**  | **I3 - Low**   |
|-------------------------------|---------------|------------------|----------------|
| **L1 - High**                 | `S1`         | `S1`            | `S2`          |
| **L2 - Medium**               | `S1`         | `S2`            | `S3`          |
| **L3 - Low**                  | `S2`         | `S3`            | `S3`          |

`S4` may be used for issues not requiring mitigations, but may need to be
triaged as `~feature proposal`s as described under [labels](#labels-and-confidentiality/index.html.md).

#### More Risk Rating Examples

`S1`:
* Remote Code Execution (RCE/index.html.md)
* SQL Injection (SQLi/index.html.md)
* Authentication Bypass
* Authorization vulnerabilities that expose critical data (password hashes, repositories, tokens/index.html.md)
* While the above are possible examples of `S1`, the final determination for `S1` is determined by the impact to our users ( > 50% impacted/index.html.md)

`S2`:
* Cross-site Scripting (XSS/index.html.md)
* Authorization vulnerabilities that do not expose critical data
* Resource exhaustion denial-of-service (DoS/index.html.md)
* Cross-site Request Forgery (CSRF/index.html.md)
* While the above are possible examples of `S2`, the final determination for `S2` is determined by the impact to our users (between 25-50% impacted/index.html.md)

`S3`:
* Tab nabbing
* Race conditions that do not put user data in jeopardy
* Path disclosure
* While the above are possible examples of `S3`, the final determination for `S3` is determined by the impact to our users (up to 25% impacted/index.html.md)

`S4`:
* Implement new security feature
* Remove support for deprecated protocol
* While the above are possible examples of `S4`, the final determination for `S4` is determined by the impact to our users (zero impact to users/index.html.md)

## Internal Application Security Reviews

For systems built (or significantly modified/index.html.md) by functional groups that house customer and other sensitive data, the Security Team should perform applicable application security reviews to ensure the systems are hardened.

### Process

The current [process](https://gitlab.com/gitlab-com/security/issues/16/index.html.md) for requesting an internal application security review is:

1. Requestor creates an issue in the security tracker and adds the app sec review label.
1. Requestor submits a [triage questionnaire form](https://docs.google.com/forms/d/e/1FAIpQLScIpq-vmfRTN3ClvETGP1B68C91FDXoiYhkSSzIpN7IFiGlWQ/viewform?usp=sf_link/index.html.md) for the app.
1. Security team reviews the triage form and determines its next steps (design, testing, no test, etc./index.html.md).
1. If sent to design phase, requestor submits [design questionnaire](https://docs.google.com/forms/d/e/1FAIpQLSf1WlPkjWJp1RkOblxedNrznQX_1sQhZ7EwuVAfRs73xfuvkQ/viewform?usp=sf_link/index.html.md). An optional call can be arranged to discuss the architecture further. At the end of this phase, the security team will scope it for X amount of days of testing. It will now be sent to the testing phase.
1. The requestor submits a [testing questionnaire](https://docs.google.com/forms/d/e/1FAIpQLSc_ckVUuF__gXOX2scw2W15H5M2uhCEeV7qEBQYfQ-Lvotm1A/viewform?usp=sf_link/index.html.md) with the test environment information. The scheduled testing window will also be determined.
1. The security team performs the assessment during the testing window and documents any findings in the app's associated component in GitLab. Once testing is finished, it will be sent to the remediation phase.
1. All findings will be remediated by the appropriate teams and validated by the security engineer who tested it.
1. Once all findings have been closed, the review can be considered complete.

As part of the app sec review process, a security issue is created to track the progress of the review. In those issues, labels and milestones can be added. It's important to note here that application security reviews are not a one-and-done, but can be ongoing as the application under review evolves.


## Fighting Spam

The security team plays a large role in defining procedures for defending against and dealing with spam. Common targets for spam are public snippets, projects, issues, merge requests, and comments. Advanced techniques for dealing with these types of spam are detailed in the [Spam Fighting runbook](https://docs.google.com/document/d/1V0X2aYiNTZE1npzeqDvq-dhNFZsEPsL__FqKOMXOjE8/index.html.md).

## Always "WIP" Risk Assessment
{: #risk-assessment}

GitLab has an "always WIP" Risk Assessment and all team members are encouraged to participate. The Risk Assessment consists of a list of all risks or threats to the GitLab infrastructure and GitLab as a company, their likelihood of occurring, the impact should they occur, and what actions can be taken to prevent these risks from damaging the company or mitigate the damage should they be realized.

The risk assessment is stored as a Google Sheet (search Google Drive for "Risk Assessment"; make sure you are searching for spreadsheets shared with GitLab.com/index.html.md) and is available to all team members. It should not be shared with people outside of the company without permission.

The format of the Risk Assessment may seem intimidating at first. If you do not know what values to use for risk ratings, impact ratings, likelihoods or any other value leave them blank and reach out to the Security Team to help you determine appropriate values. It is more important to have all risks documented than it is to have all values completed when adding new risks. Guidelines and instructions for how to add a risk and how to calculate each rating or score are included on the "Instructions" tab.

## Vulnerability Reports and HackerOne

GitLab receives vulnerability reports by various pathways, including:
- HackerOne bug bounty program
- `security@gitlab.com`
- Reports or questions come in from customers through Zendesk.
- Issues opened on the public issue trackers.  The security team can not review
  all new issues and relies on everyone in the company to identify and label
  issues as `~security` and @-mention `@gl-security` on issues.

For **any** reported vulnerability:

- Open a confidential issue in the appropriate issue tracker as soon as a report
  is verified. If the vulnerability was reported via a public issue, make the issue confidential.
  If triage is delayed due to team availability, the delay should be communicated.
- An initial determination should be made as to severity and impact. Never **dismiss** a security report outright. Instead, follow up with the reporter, asking clarifying questions.
- For next steps, see the process as it is detailed below for HackerOne reports, and adhere to the guidelines there for vulnerabilities reported in other ways as well in terms of frequency of communication and so forth.
- Remember to prepare patches, blog posts, email templates, etc. on `dev` or in other non-public ways even if there is a reason to believe that the vulnerability is already out in the public domain (e.g. the original report was made in a public issue that was later made confidential/index.html.md).

### HackerOne Process

GitLab utilizes [HackerOne](https://www.hackerone.com/index.html.md) for its bug bounty program. Security researchers can report vulnerabilities in GitLab applications or the GitLab infrastructure via the HackerOne website. Team members authorized to respond to HackerOne reports use procedures outlined here.

- If team availability has increased response times beyond 48 hours, a security
  team member should `Add comment` using the `Week to respond` template.
- When beginning work on a report, the security team member should assign the
  report to the themselves.
- Conduct initial communication with the reporter and investigation, using the
  following guidelines as necessary:
  - [Request clarification](#if-a-report-is-unclear/index.html.md)
  - Attempt to verify the report and triage the vulnerability.
- Potential, non-bounty outcomes:
  - Report is out-of-scope.  If actionable, issues may still be created, but
    further process may not be followed see [violating the rules](#if-a-report-violates-the-rules/index.html.md).
  - Report is a `~feature proposal` as defined above and would not need to be
    made confidential or scheduled for remediation.  An issue can be created, or
    requested that the reporter creates one if desired, but the report can be
    closed as "Informational".
  - Report is invalid.  For example, we've gotten a number of reports for
    [inline HTML in markdown](https://docs.gitlab.com/ee/user/markdown.html#inline-html/index.html.md)
    that do not exceed the capabilities of markdown itself.
- If the report is valid, in-scope, and requires action or further investigation by
  the responsible engineering team:
  - Complete all steps of [Creating a new security issue](#creating-a-new-security-issue/index.html.md) as
    above.
    - HackerOne provides an "export" option that simplifies copying data from the HackerOne issue to GitLab. Export the data in markdown format and paste it into the new issue.
    - Always add the `~HackerOne` label to these issues, for later reporting and tracking.
    - @ mention engineering managers of appropriate teams, based on the [current organization chart](/team/chart/index.html.md).
    - As applicable, notify relevant team members via the issue, chat, and email, depending on the chosen security level.
  - Change the state of the report to "Triaged" in HackerOne and include a link to the issue as the reference.
    - Fill in the comment using the `Traiged-Escalated to engineering` Common
      response as a template.
    - In the comment, include link to the confidential issue
- Continue to update the report in HackerOne when the issue is scheduled for a
  security release.
- Discussion and remediation of vulnerabilities can sometimes take longer than we would prefer. Even so, frequent communication with reporters is far better than leaving reporters in the dark, even if our progress is slow. Therefore:
    - For vulnerabilities where patches are actively being worked on, reporters should be updated at least **weekly**.
    - In the case where fixes are not as clear or discussion is still on-going as to whether a patch will be created at all, reporters should be notified of updates at least **monthly**.
    - In any case, no report should go "stale" where updates are not provided within the last month.

#### If a Report is Unclear

If a report is unclear, or the reviewer has any questions about the validity of the finding or how it can be exploited, now is the time to ask. Move the report to the "Needs More Info" state until the researcher has provided all the information necessary to determine the validity and impact of the finding. Use your best judgement to determine whether it makes sense to open a confidential issue anyway, noting in it that you are seeking more information from the reporter. When in doubt, err on the side of opening the issue.

One the report has been clarified, follow the "regular flow" described above.

#### If a Report Violates the Rules

If a report violates the rules of GitLab's bug bounty program use good judgement in deciding how to proceed. For instance, if a researcher has tested a vulnerability against GitLab production systems (a violation/index.html.md), but the vulnerability has not placed GitLab user data at risk, notify them that they have violated the terms of the bounty program but you are still taking the report seriously and will treat it normally. If the researcher has acted in a dangerous or malicious way, inform them that they have violated the terms of the bug bounty program and will not receive credit. Then continue with the "regular flow" as you normally would.

#### If the Report is Invalid

If the report is invalid (in your determination/index.html.md) or does not pose a security risk to GitLab or GitLab users it can be closed without opening an issue on GitLab.com. When this happens inform the researcher why it is not a vulnerability and close the issue as "Informational". HackerOne offers the option to close an issue as "Not Applicable" or "Spam". Both of these categories result in damage to the researcher's reputation and should only be used in obvious cases of abuse.

### When a Patch is Ready

When a patch has been developed, tested, approved, merged into the security branch, and a new security release is being prepared it is time to inform the researcher via HackerOne. Post a comment on the HackerOne issue to all parties informing them that a patch is ready and will be included with the next security release. Provide release dates, if available, but try not to promise a release on a specific date if you are unsure.

This is also a good time to ask if they would like public credit in our release blog post and on our vulnerability acknowledgements page for the finding. We will link their name or alias to their HackerOne profile, Twitter handle, Facebook profile, company website, or URL of their choosing. Also ask if they would like the HackerOne report to be made public upon release. It is always preferable to publicly disclose reports unless the researcher has an objection.

#### CVE IDs

We use CVE IDs to uniquely identify and publicly define vulnerabilities in our products. Since we publicly disclose all security vulnerabilities 30 days after a patch is released, CVE IDs must be obtained for each vulnerability to be fixed. The earlier obtained the better, and it should be requested either during or immediately after a fix is prepared.

We currently request CVEs either through the HackerOne team or directly through MITRE's [webform](https://cveform.mitre.org/index.html.md/index.html.md). Keep in mind that some of our security releases contain *security related* enhancements which may not have an associated [CWE](https://cwe.mitre.org/index.html.md/index.html.md) or vulnerability. These particular issues are not required to obtain a CVE since there's no associated vulnerability.

### On Release Day

On the day of the security release several things happen in order:

* The new GitLab packages are published.
* All security patches are pushed to the public repository.
* The public is notified via the GitLab blog release post, security alerts email, and Twitter.
* The vulnerability acknowledgements page is updated with appropriate credits to the reporting researchers.

Once all of these things have happened notify the HackerOne researcher that the vulnerability and patch are now public. The GitLab issue should be closed and the HackerOne report should be closed as "Resolved". Public disclosure should be requested if they have not objected to doing so. Any sensitive information contained in the HackerOne report should be sanitized before disclosure.

### Swag for Reports

GitLab awards swag codes for free GitLab swag to any reports that result in a security patch. Limit: 1 per reporter. When a report is closed, ask the reporter if they would like a swag code for free GitLab clothing or accessories. Swag codes are available by request from the marketing team.

## Security Questionnaires for Customers

Some customers, to keep up with regulations that impact their business, need to understand the security implications of installing any software - including software like GitLab.

### Process

The current process for responding to customer requests is:

1. Refer a customer to our public statements on security here: /security/
1. If a customer still has questions that need to be discussed, you can [engage a Solutions Architect](handbook/customer-success/solutions-architects/#when-and-how-to-engage-a-solutions-architect/index.html.md) in that discussion.
1. If the customer still needs a specific questionnaire filled out, create a [confidential issue](https://gitlab.com/gitlab-com/customer-success/sa-service-desk/issues/index.html.md) with the label `Security` and `SA Backlog` for the completion of that document
1. The SA team will take the first pass at the questionnaire using /security/ and [this folder](https://drive.google.com/drive/folders/0B6GNv2pwhtCxWVJWdEZCTUEwbXc/index.html.md) as a reference.
1. Once the SA team has completed what they can, the questionnaire will go to the security team for additional answers.
1. Once the questionnaire is complete, it will need to be approved by the [Director of Security](/job-families/engineering/security-management/index.html.md/index.html.md) for release to the customer.
1. File the completed questionnaire in the example folder for future reference.

## Vulnerability Scanning

GitLab maintains a custom vulnerability scanner that is used to regularly scan all GitLab assets for common vulnerabilities as well as previously patched GitLab vulnerabilities and to ensure that no GitLab security-sensitive services are accidentally exposed.

Details on this scanner and how it is configured are available to all team members in a Google Doc entitled "Vulnerability Scanner Config".

## Package Signing
{: #package-signing}

The packages we ship are signed with GPG keys, as described in the [omnibus documentation](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/package-information/signed_packages.md/index.html.md). The process around how to make and store the key pair in a secure manner is described in [the runbooks](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/manage-package-signing-keys.md/index.html.md). Those runbooks also point out that the management of the keys is handled by the Security team and not the Build team. For more details that are specific to key locations and access at GitLab, find the internal google doc titled "Package Signing Keys at GitLab" on Google Drive.
