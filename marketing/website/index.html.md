---
layout: markdown_page
title: "Website Handbook"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Objectives

Serve the needs and interests of our key audiences:

1. Users of GitLab: software developers and IT operations practitioners.
2. Buyers of GitLab: IT management, software architects, development leads.
3. Users of and contributors to OSS on gitlab.com.

Generate demand for GitLab by:

1. Showcasing the benefits of the most important GitLab features and how they can save time and money.
2. Compare GitLab vs competing products.
3. Provide customer case studies which illustrate 1 and 2.

## Scope

The GitLab marketing webiste, or simply the "GitLab Website" refers to all of the content on `https://about.gitlab.com` except the [blog](/handbook/marketing/blog/) and [handbook](/handbook/).

The website does not include
  - The Docs: `docs.gitlab.com`
  - The GitLab.com product: `gitlab.com`
  - The Handbook: `about.gitlab.com/handbook`
  - The blog: `about.gitlab.com/blog`

See [Where should content go?](https://about.gitlab.com/handbook/git-page-update/#where-should-content-go) to learn which web property is the most appropriate place to put different types of content. To learn what section of the website different content belogs see [definitions](#definitions).

## Definitions

### Topics

A topic is an industry trend, theme, or technology related to GitLab and our customers. For example, DevOps, GDPR, Containers, etc. Topic pages on our website educate the reader about the topic and share GitLab’s point of view while providing additional links to resources related to that topic. These pages are intended to attract search traffic.

Topic pages should exist at the root level of the website without being nested inside of another directory. e.g. `/continuous-integration`

Examples of other companies who have topic pages:
- [https://www.redhat.com/en/topics/containers](https://www.redhat.com/en/topics/containers)
- [https://pivotal.io/containers](https://pivotal.io/containers)
- [https://pivotal.io/topics](https://www.redhat.com/en/topics/containers)

### Solutions

A solution is a combination of products and services that solve a business problem. For example, accelerating software delivery, enabling remote teams, ensuring compliance, etc. Solution pages on our website show the application of GitLab capabilities and services to address a business problem while providing additional links to resources related to that solution.

Solution pages should be nested inside of the solutions directory. e.g. `/solutions/continuous-integration`

Examples of other companies who have solutions pages:
- [https://www.redhat.com/en/challenges](https://www.redhat.com/en/challenges)

### Product section

The product section of our website has pages that describe what GitLab does and the value provided. The functionality of GitLab is ordered in a hierarchy with 4 levels: Stage, Categories, Capabilities, and Features. You can find details on the [Product Categories Handbook](/handbook/product/categories/)

- Stages relevant to users are listed on the [product overview page](/product) with details about the stage on the [stages page](https://gitlab.com/gitlab-com/www-gitlab-com/issues/2428).
- Categories relevant to users are listed on the [product overview page](/product).
- Capabilities are listed on the category page they belong to. Capabilities may also have their own landing page.
- Features are listed in many places on the website: on the features page, the capabilities page they belong to, the pricing page, comparison pages, and the ROI calculator.

Category pages should be nested inside of the product directory. e.g. `/product/continuous-integration`

Examples of companies who have product/features pages:
[https://mailchimp.com/features/](https://mailchimp.com/features/)
[https://www.groovehq.com/features](https://www.groovehq.com/features)

### Overlap

Similiar content can appear as a topic, solution, and in the product section with different emphases on each page. For example continuous integration:

- A topic page: `/continuous-integration` would talk about what CI is at a functional level.
- A solutions: `/solutions/continuous-integration`. would talk about why CI is important for businesses to adopt.
- A category page `/product/continuous-integration` would talk about the capabilities and features that are part of GitLab's CI functionality and the value it has.

## Ownership and responsibilities

Everyone can [contribute to the marketing website](#updating-the-marketing-website). While the [Product Marketing](https://about.gitlab.com/handbook/marketing/product-marketing/) and [Pipe-to-Spend](https://about.gitlab.com/handbook/marketing/marketing-sales-development/online-marketing/) teams have primary responsibility over the website, the goal of these teams is to build systems, structures, and processes and empower everyone to contribute. Below is a breakdown of the ownership between Product Marketing and Pipe-to-Spend.

### Product Marketing

- Responsible for all of the content on the website.
- The website team (part of product marketing) is responsible for the design and development of the website.

### Pipe-to-Spend

- CTAs (Calls to action): The growth team owns all buttons on the website including which pages get CTAS, the text used and where they link to. (Note: the website team still owns the design and styles of the buttons to ensure they are consistent and on brand.)
  - Any buttons tracked from the growth team should have a unique class used for tracking like `.free-trial-homepage-button`, rather than use a class that also distinguishes a buttons style e.g. `.btn`, `.cta-btn`, `.accent` etc. Using unique class names to track can also accompany classes that give the proper style. Classes on buttons we track should look something like this: `.btn.cta-btn.accent.free-trial-homepage-button`.
- Build and implement online growth strategy:
  - Search Engine Optimization
  - Paid search and social
  - Conversion Rate Optimization (CRO) and a/b and multivariate testing
      - CRO Process: Not all changes to pages need to be tested, only pages that we want to optimize for conversion activities. These pages/elements are often being tested
          - Homepage
          - Top navigation
          - Pricing page
          - Free trial
          - Contact sales
      - Please check [A/B test issue board](https://gitlab.com/gitlab-com/marketing/online-growth/boards?=&label_name[]=a%2Fb%20test) for pages you plan to update. The URL will be the first word or `HP` for the homepage.  If you have an update to any of the pages in the `Doing` column contact @lbanks. More details on CRO and testing in the [Online Growth Handbook section](/handbook/marketing/marketing-sales-development/online-marketing/)
-  Web analytics, tracking, and reporting
-  User journey optimization

## Updating the Marketing Website

### Minimum Viable Change

Use [MVCs](https://about.gitlab.com/handbook/values/#iteration) to update the website. Create new pages and add the minimal amount of viable content. You can add images and more content in iterative steps.

We have 10-20 seconds to tell visitors why they should stay on our pages. Tell visitors what value the page will give them. Start with a high-level summary opening the page. This could be as simple as a single sentence, but we shouldn’t put the burden of discovering the value of the page on visitors.

The page title and URL should include keywords visitors might use to discover the page you’re creating. If you’re not sure what terms a visitor might use, ask the Online Growth team for suggestions in your Merge Request. We have a list of high priority topics and recommended keywords to use.

### Creating a new page

To create a new page you for follow these steps:
1. Create an issue in the [website repo](https://gitlab.com/gitlab-com/www-gitlab-com/issues) **Note**: Don't branch from other repos like the marketing repo.
2. Create an MR from the issue by clicking on the "Create Merge Request" button. This will create a new branch for you and link it to your issue and label the the MR as `WIP:`.
3. Click on the name of your branch after "Request to Merge" to open that branch in the repository file view.
4. Open the `source` folder. This is where webpages are stored.
5. Click on the directory where you want your webpage to be. For example, if you put a page in the `source` folder it will show up at the "root" level, if you create the new directory inside of another directory it will will appear at that path.
5. Click to add a `New directory` from the plus sign drop down.
6. Name the directory in all lowercase with dashes-between-words for what you want the path of your page to be. For example if you want to create a page at [about.gitlab.com/solutions/cloud-native](/solutions/cloud-native) then click on the `solutions` directory and inside the `solutions` directory create a new directory called `cloud-native`.
7. Click to add a `New file` from the plus sign drop down
8. Name the file `index.html.md`
9. Add this code to the top of the file

```
---
layout: markdown_page
title: ""
---
## Subheading

Here is your first paragraph replace this text.
```

10. Inside the quote add the title of your page. For example the title of my cloud native page would be "Building Cloud Native Applications With GitLab".
11. Using markdown you can add more content to the page. All you need is a title, subheading and a paragraph to get started.
12. Delete the `.gitkeep` file. This is a placeholder file from when you created the directory since git cannot track empty directories. A quick way to delete the file on the correct branch is to click on "edit" in the changes tab of your MR. This will open the file editor. click "cancel" and dismiss the popup that says "all changes will be lost". This will then place you in the file view for the `.gitkeep` file on your branch. Click the "delete" button to delete the file.
13. **ProTip**: Now that you no longer have a branch with no changes you can use the Web IDE to make further edits. (The Web IDE doesn't work if you have a branch with no changes. [Fix coming in 11.3](https://gitlab.com/gitlab-org/gitlab-ce/issues/48166)
14. **ProTip**: Add a link to the bottom of your page so people can continue reading related content. Popular choices would be `/product` , `/solutions`, `/pricing` or any pages related to your page.
15. If you need help you can Ping @williamchia or @jareko in the MR or on slack in the #website channel.  

### Updating an existing page

1. Click on the "edit" button at the bottom of the page.
1. Edit the page. Note: page content can be in markdown, `haml`, or possibly in a separate `.yml` file that populates fields in the `haml` file. The [hello bar](#editing-the-homepage-promo-banner-hello-bar) is an example of content in a `.yml` file.
1. If you need help you can Ping @gl-website in the MR or ping @website-team in the #website slack channel.  

### Updating the team page and org chart

1. Both the [team page](/team/) and [org chart](/team/chart/) are updated based on [`team.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/team.yml)
2. Edit [`team.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/team.yml) and create an MR
3. The org chart is built automatically based on `slug` and `reports_to` lines.
4. See the [team structure](https://about.gitlab.com/team/structure/#specialists-experts-and-mentors) page for more info on specialties, expertise, and mentorship availability to a listing.

### Updating the homepage promo banner (`hello-bar`)

- The homepage promo banner is edited at [`/source/includes/hello-bar.html.haml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/source/includes/hello-bar.html.haml).
- This banner includes an optional image (logo) to accompany the text.

### Adding features to webpages

All features and capabilities are listed in a single yaml file
([`features.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/features.yml)) under the `features` section.
It is the single source of truth for multiple pages across the website including:

- [Product pages](/product/) e.g. [continuous integration](/product/ci)
- [Pricing](/pricing/)
- [Compare](/comparison/)
- [ROI](/roi/)
- [Features](/features/)

To add a new feature, add a feature block to under the `features:` section of the page. Add the following attributes:
  - title: the name of the feature in quotes
  - description: a plaintext summary of the value the feature provides in quotes
  - link_description: OPTIONAL, anchor text of a link that will appear below the descriptions e.g. `link: https://docs.gitlab.com/ee/user/project/milestones/`
  - link: OPTIONAL, the url of the link (no quotes)
  - screenshot_url: OPTIONAL,the path to a screenshot of the feature in quotes. e.g. `screenshot_url: 'images/feature_page/screenshots/28-group-milestones.png'`
  - category: a list of one or more categories that this features belongs to. Adding a category to a feature causes it to show up in the features section on the product page for that category (e.g. see the [Continuous Integration page](/product/ci/))
  - solution: REQUIRED legacy field. A [stage of the DevOps lifecycle](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/stages.yml). Will be [removed soon](https://gitlab.com/gitlab-com/www-gitlab-com/issues/2435).
  - tier: `true` or `false` is this feature or capability available in this tier? `gitlab_core`, `gitlab_starter`, `gitlab_premium`, `gitlab_ultimate`
  - gitlab_com: `true` or  `false` is this feature or capability available on GitLab.com? Because GitLab.com tiers map 1:1 to self-managed tiers setting this will automatically assign the GitLab.com tier. E.g. `gitlab_core: true` + `gitlab_com: true` == `GitLab.com Free`. Adding a tiers fields is what powers the tier badges on product pages and comparison pages, as well as powers the tier [feature comparison of the pricing page](https://about.gitlab.com/pricing/self-managed/feature-comparison/).  
  - tools: `true` or `false` or `partially` - any tool from the `competitors:` section such as `jira:`, `circle_ci:`, `blackduck:`, etc. that does or does not have this feature. Examples of `partially` are if a competitor has some but not all of the feature described, or if they have the feature, but only through a plugin. See [Creating a comparison page](#creating-a-comparison-page)
  - pricing_page: `true` | `false` this option was created when the pricing page used to be called the "products" page. Setting true cause the feature to show up on the [pricing page](/pricing/#self-managed). Only a limited number of the most important capabilities should be shown on the main pricing page to keep it easily consumable. Folks can click on "see all features" to see the full list of features ([self-managed comparison](/pricing/self-managed/feature-comparison/), [GitLab.com comparison](/pricing/gitlab-com/feature-comparison/)).  

For example:

```

- title: "Group Milestones"
  description: "Create and manage milestones across projects, to work towards a target date from the group level. View all the issues for the milestone you’re currently working on across multiple projects."
  link_description: "Learn more about Group Milestones"
  link: https://docs.gitlab.com/ee/user/project/milestones/
  screenshot_url: 'images/feature_page/screenshots/28-group-milestones.png'
  solution: plan
  category:
      - portfolio_management
  gitlab_core: true
  gitlab_starter: true
  gitlab_premium: true
  gitlab_ultimate: true
  gitlab_com: true
  github_com: false
  github_enterprise: false
  bitbucket_org: false
  bitbucket_data_center: false
  gogs: false
  jira: false
  ca_agile_central: false

```
Copy and paste this template:

```

- title: ""
  description: ""
  link_description: ""
  link:
  screenshot_url: ''
  solution:
  category:
    -
  gitlab_core:
  gitlab_starter:
  gitlab_premium:
  gitlab_ultimate:
  gitlab_com:
  github_com:

```



### Creating a comparison page

The [`/comparison`](/comparison) section of the website shows info about DevOps tools and a feature comparison of those tools to Gitlab. Comparison pages are auto-generated from `features.yml`. All you need to do is add a tool to the `competitors` section and add that tool id to some features and the page will be created.

To add a new comparison page:
1. Edit [`features.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/features.yml)
2. Under the `competitors` section add a tool.

Although the summary and include_file fields are not strictly required by the parser in order to build the page, every tool should have at least one paragraph summarizing the comparison.

  - id: a lowercase, snake_case unique identifier (e.g. `travis_ci`)
  - name: the display name of the tool in single quotes
  - logo: the path to the logo, if there's no logo, add it in the `/images/logos/` directory
  - category: a list of [GitLab product categories](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/categories.yml) that this tool is for. Setting a category caused the tool to show up for that category when using the dropdown filter on a comparison page.
  - summary: OPTIONAL A summary paragraph describing the to tool compared to GitLab. Add a pipe ( `|` ) then add content in markdown indented on the next line. Be sure to add on additional empty line after your content.
  - include_file: OPTIONAL path to a markdown (`.md`) file that will be embedded on the page. Here is where you can add more robust content about the tool. Please use the template under `/source/devops-tools/misc/tool-template.html.md` and store your new file under `/source/devops-tools/TOOLNAME/index.html.md`.

  For example:

```
  jenkins:
     name: 'Jenkins'
     logo: '/images/comparison/jenkins-logo.svg'
     category:
       - ci
       - cd
  include_file: devops-tools/jenkins/index.html.md
  chef:
     name: 'Chef'
     logo: '/images/logos/sdlc-competitors/chef.png'
     category:
       - infrastructure_configuration
     summary: |
       Chef is a configuration management tool that enables deployment and maintentce of state for large scale infrasstructure. Chef excels as managing legacy infrastructure like physical servers and VMs. Chef was designed before widespread container adoption and does not implement Kubernetes natively.

       GitLab is a single appliation for the whole DevOps lifecylce that includes not only configuration management, but also capabilities for proejct management, source code management, CI/CD, and monitoring. GitLab is designed for Kubernetes and cloud native applications.

       GitLab can be used together with Chef to enable VM and bare metal configuration management. For Cloud Native applications run on Kubernetes, Chef is not required and GitLab can provide all the functionality natively.
```  

Copy and past this template:  

```
unique_tool_id:
    name:
    logo: '/images/logos/'
    category:
      -
    summary: |


```

3. Add features to the comparison section.

Be sure to add features that GitLab has that the other tool doesn't and also features the other tool has that GitLab doesn't so that our comparison are transparent and honest.

- On a feature block, add the tool id and then `true`, `false`, or `partially` to indicate support for the feature. Add the same details for gitlab tiers. Adding a tool id to a feature is what causes it to show up on the comparison page for that tool. (e.g. if you don't want a feature to show up on a comparison page remove the tool id line from that feature.)

For example:

```
  - title: "Free CI/CD with shared or personal Runners"
    capability: true
    description: "GitLab.com has shared Runners that allow you to use GitLab CI/CD completely free up to 2000 build minutes for private projects and unlimited for public projects. Alternatively, you can set up your own Runner for faster build processing, unlimited build minutes, or special requirements."
    link_description: "Explore GitLab.com offerings"
    link: /gitlab-com
    solution: gitlab_com
    gitlab_core: true
    gitlab_starter: true
    gitlab_premium: true
    gitlab_ultimate: true
    gitlab_com: true
    github_com: false
    bitbucket_org: 'partially'
    gitlab_ci: true
    codestar: false
  - title: "Domain Specific Lanuage"
    description: "A Domain Specific Lanuage (DSL) for defining infrstructure configuration allows thinking in resources, not files or commands to write declarative rather then procedural code."
    # link_description: ""
    # link: ''
    solution: missing
    gitlab_core: false
    gitlab_starter: false
    gitlab_premium: false
    gitlab_ultimate: false
    puppet: true
    chef: false

```
4. If you followed the above step, the new comparison page should be reachable
   under `/comparison/tool-vs-gitlab.html` and you should see it in the
   dropdown menu. The last thing you need to do is create the PDF. Follow the
   info in [creating comparison PDFs](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/doc/pdf.md).

5. Add logos to the homepage and comparison page
- Today still a manual process, but [will be automated soon](https://gitlab.com/gitlab-com/www-gitlab-com/issues/2735).
- Add the name, logo, and url into [sdlc.yml](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/sdlc.yml) under the `competitors` ssecion for the corresponding "phase" (i.e. Stage). 
- Both pages pull from the same yml so adding it will cause it to show up in both places. 
For example: 

```
- phase: Plan
...
  competitors:
    - name: Asana
      logo: /images/comparison/asana-logo.png
      link: /comparison/asana-vs-gitlab.html

```

### Adding content to resources

The [`/resources`](/resources/) section of the website contains downloadable files and links to helpful content.

1. To add a resource, edit the [`resources.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/resources.yml) file.
2. To create a new entry for your resource, use this template and add it to the top of `resources.yml`:

```
- title:
  url:
  image: /images/resources/gitlab.png
  type: Pick one --> 'Blog post' 'One-pager' 'Report' 'Webcast' 'White paper'
  topics:
    - Cloud native
    - Code review
    - Continuous delivery
    - Continuous integration
    - DevOps
    - Git
    - GitLab
    - On-demand training
    - Public Sector
    - Security
    - Software development
  solutions:
    - Distributed teams
    - Accelerated delivery
    - Executive visibility
    - Project compliance
    - Security and quality
```

3. **Uploading a PDF**: If the resource you'd like to add is a PDF, it can be uploaded to [`/pdfs/resources/`](https://gitlab.com/gitlab-com/www-gitlab-com/tree/master/source/pdfs/resources/).

4. **Selecting an image**: Each resources has a thumbnail image based on their topic; select the most relevant image for the content. The current thumbnail images are shown below and can be found [here](https://gitlab.com/gitlab-com/www-gitlab-com/tree/master/source/images/resources).
![ALT](/images/resources/resource-page-thumbnails.png)

5. **Selecting a type**: All resource types are listed in the code snippet above; select one that best fits your content. If the resource does not fit the current types, please see [Requesting Website Updates](#requesting-website-updates) to submit a proposal for new resource type(s).

6. **Selecting topics & solutions**: The code snippet above provides all of the current topics and solutions; chose the topics and solutions that best apply to the content. Please note they are case sensitive and incorrect casing or spelling will result in the generation of new, unwanted, topics and/or solutions.

### Requesting Website Updates
If you'd like to propose new changes to the website and the update is more complicated that you can do on your own to either [create a new page](#creating-a-new-page) or [update and existing page](updating-an-existing-page) you can request help from the Website team. New changes or updates with a due date should be requested at least 2 weeks prior to that due date.
1. Before requesting help, create the content that you want to go live. E.g. draft the exact words that you want updated.
1. To request help from the website team to update the site, create an issue in the [www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com/issues) project
1. Add the specific content (exact wording and images) in the issue description that you want to put live on the website. Note: If the the content is unclear, the issue will be assigned back to you to clarify the content before the website team will begin development work.
1. add the `Website` label
1. ping @gl-website in the MR or ping @website-team in the #website slack channel.
