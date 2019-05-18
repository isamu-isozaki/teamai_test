---
layout: markdown_page
title: "CI/CD Tools Primer"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## CI vs CD

![CD vs CD Pipeline](https://docs.gitlab.com/ee/ci/img/cicd_pipeline_infograph.png)
From [https://docs.gitlab.com/ee/ci/](https://docs.gitlab.com/ee/ci/)

### Continuous Integration (CI)
- **Continuous Integration** is a development practice
- Focuses on frequently integrating code into a shared repository
- Involves automatically building and testing every change that is committed
- Higher frequency of integration and testing means smaller problems
   - smaller problems are easier/quicker to fix
- Focus is to find code issues as early and quickly as possible
   - while the developer is still in context of code change, so easier to resolve problems
- Enables developer confidence in code, which results in faster development

### Continuous Delivery/Deployment (CD)
- Can mean either Continuous Delivery and/or Deployment
- Either way, CD is a release management practice
- **Continuous Delivery** means that the software is always ready to be released
   - Can mean it is ready to be pushed to a staging or production system
   - Or that it is ready to be shipped/distributed (not everyone does web apps)
- **Continuous Deployment** means that changes are actually released to production automatically when the pipeline successfully completes
- Continual testing for releasability lowers the risk of each release - goal: boring releases
- When releases are low risk, they happen more, and value gets delivered to customers more frequently

## Market Overview

### Forrester CI Wave
![Forrester CI Wave](/images/home/forrester-ci-wave-graphic.svg){: .small.left}


- No vendor can survive today by only doing CI
- Vendors in the CI space have all evolved to include CD, as it is a natural extension of the capabilities of a CI system
- This evolution largely involves adding integrations to provision and configure environments (the automation is already a capability)
- Containers, micro-services, and Kubernetes changed the game of what it takes to do CI/CD
   - build artifacts through the pipeline now come wrapped in their application environments
   - storing container images instead of build artifacts
   - full integration testing becomes easier in earlier stages
   - CI/CD tools can now more easily automate everything about an applications deployment with minimal integration work
- So now CI/CD vendors are all racing to add Docker and Kubernetes support

## Competitor Scope - Continuous Integration

|Feature           |GitLab      |Circle CI   |TFS/VSTS    |Jenkins     |Travis CI   |BitBucket    |
|:-----------------|:----------:|:----------:|:----------:|:----------:|:----------:|:-----------:|
|Auto-scaling      |Y           |Y           |N           |N           |Y           |Y            |
|Pipeline graphs   |Y           |Y           |Y           |Integration |N           |Integration  |
|Parallel jobs     |Y           |Y           |Y           |Y           |Y           |Y            |
|Config as Code    |Y           |Y           |Y           |Y           |Y           |Y            |
|Container support |Y           |Y           |Y           |Y           |Y           |Y            |

## Competitor Scope - Continuous Delivery/Deployment

|Feature           |GitLab      |Circle CI   |TFS/VSTS    |Jenkins     |Travis CI   |BitBucket    |
|:-----------------|:----------:|:----------:|:----------:|:----------:|:----------:|:-----------:|
|Environments      |Y           |N           |Y           |N           |Y           |Y            |
|Env History       |Y           |N           |N           |N           |N           |Y            |
|No Conf staging apps|Y           |N           |N           |N           |Y           |N            |
|Deploy boards     |Y           |N           |Y           |Integration |Y           |N            |
|Nat Canary Deploy |Y           |N           |Y           |N           |Y           |N            |
|Secure variables  |Y           |N           |Y           |Integration |N           |Y            |
|Deploy tracability|Y           |N           |Y           |Integration |Y           |Y            |
|Protected Envs    |N           |N           |Y           |N           |N           |Y            |
