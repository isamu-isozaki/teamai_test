---
layout: markdown_page
title: "Job Families"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Job Families

For each job family at GitLab, there should be one position description as it is the single source of truth. A job family has the url /job-families/department/title and contains the following paragraphs:

- Overview
- Levels (i.e. junior, intermediate, senior, staff, etc.) which describe the requirements for each level. If no level is specified in the Job Family, then that is representing the intermediate level.
- [Specializations](/job-families/specialist) (e.g. CI/CD, distributed systems, Gitaly) relevant to that job family. Note that "specialist" job families may be created if their area of expertise and/or job responsibilities do not fit under any other, more general job families (e.g. the [candidate experience specialist job family](/job-families/people-ops/candidate-experience-specialist/)).
- Hiring process
- Apply
- About GitLab
- Compensation

The job family does not contain:

- Locations (EMEA, Americas, APEC)
- [Expertises](/team/structure/#expert) since these are free form.

The position description will be used _both_ for the [Vacancy Creation Process](/handbook/hiring/vacancies/#vacancy-creation-process), as well as serving as the requirements that team members and managers alike use in conversations around career development and performance management.

## Leads and Managers

If you're working with a team lead or management job family, you should be aware of how GitLab defines these terms. Typically, team leads are individuals who oversee a specific project or area of expertise, but they *do not* manage people, which means they are not directly responsible for hiring, promoting, performance management of, or terminating employees.

Manager job families are those responsible for directly managing other GitLabbers. They *do* hire, promote, and terminate employees, and performance management is one of their key functions.

## New Job Family Creation

If a hiring manager is creating a new job family within the organization, the hiring manager will need to create the job family. If this is a job family that already exists (for example, Gitaly Developer would use the Developer position description), update the current position description to stay DRY. If the compensation for the job family is the same as one already in `roles.yml`, you should just update the specialty, do not create a new job family.

1. Create the relevant page in `/job-families/[department]/[name-of-job-family]`, being sure to use only lower case in naming your directory if it doesn't already exist, and add it to the correct department subdirectory.
1. The file type should be `index.html.md`.
1. Add each paragraph to the position description, for an example see the [developer job family](/job-families/engineering/developer)
1. Assign the Merge Request to your manager, executive leadership, and finally the CEO to merge. Also, cc `@gl-peopleops` for a compensation review.
1. Once the merge request has been merged, the People Ops Analyst will reach out to the HR Business Partner who supports the function to understand the job description and job family requirements in determining the appropriate compensation benchmark.  
2. Compensation Benchmark data will be sourced from Comptryx, AdvancedHR, LinkedIn, Glassdoor, Paysa, Payscale and when applicable Cybercoders to determine the 50th percentile for the job family.  For benchmarking we are only looking at the intermediate level in San Francisco.
3. In Comptrxy, look at each position description by hovering over the title to make sure it aligns to our position description.  For a history of mapping, take a look at the "comptryx Benchmarks SF" tab in the "Comp Data Analysis and Modeling "google sheet.
4. The level in Comptryx that aligns with intermediate is "proficiency,"except for in special cases (see the history of mapping for those cases).
5. Create a google document that includes the compensation data and determine the median for the benchmark, share the document with the CEO, CCO and CFO. Document should be titled Job title Comp Benchmark.
6. Create a merge request to add the benchmarks to the [job familys](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/roles.yml) file in GitLab and assign it to the CEO.  In the merge request refer to the job family title in the Google document that shows the compensation data sources and the proposed benchmark add the CCO, CFO and CEO to the MR for benchmark approval. Slack the CEO the MR for the new benchmark for review and approval.  The CEO will review the document and approvals in the MR and then will make the final decison to merge the new benchmark. Once the CEO approves the MR will add the benchmark to the `roles.yml` file which will automatically cause the [Compensation Calculator](/handbook/people-operations/global-compensation) to show at the bottom of the position description page.
7. Also add the benchmark to the "SF Benchmark" tab in the "Comp Data Analysis and Modeling" Google sheet, and document how you mapped this data in "Comptryx Benchmarks SF" tab if Comptryx was used.
