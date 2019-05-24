---
layout: markdown_page
title: "Application Security Market Analysis"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Market Overview
Security is on a dynamic trajectory. It has been traditionally focused on guarding the perimeter in a defensive approach. Enterprises would start with simple endpoint protection and network security and layer on tools for “Defense in Depth�. Today’s security is much more proactive and predictive combining internal and external data from a variety of sources and applying user behavior analytics and machine learning to identify suspicious activity.

Security investments followed a similar trajectory. Traditionally the bulk of the spending has been to protect infrastructure. In 2015, Gartner Analyst, Joseph Feiman, estimated for every $1 spent on application security, $23 was spent in other security. Application Security has only been a mainstream concern for recent years - but that’s changing! There are several dynamics making application security a bigger priority including:
- Well known and significant application-focused attacks such as Heartbleed.  
- GDPR requires that enterprises assume the risk of the vendors they use. Vulnerabilities that might be present in purchased applications become of more concern.  
- Open source code is becoming a norm. This [451 article](https://drive.google.com/file/d/1T75K9qjBtdRkFdgVy--mrKmFrWXe8cTy/view/index.html.md) explains how one small piece of code can have vast implications when it has a vulnerability that is exploited.  
- With cloud computing, the infrastructure’s security becomes the responsibility of the cloud provider. Enterprises have less perimeter to protect and are focusing more on endpoints and applications.  
- DevOps velocity requires rapid CI/CD. Traditional gated security does not fit this model forcing tradeoffs with security and more agile security processes. This has led to DevSecOps but it is still early.

Enterprises with advanced DevOps and/or Application Security programs are looking for remediation advice as the developer types the code as a means of not only reducing vulnerabilities, but also educating developers by teaching them security best practices real-time.  Fortify and a few other advanced app sec vendors provide this.  

## Compliance
Compliance is always the lowest common denominator - think of it as the MVC for security. Enterprises that depend upon software and technology to run their business seldom rely on compliance alone to guide their security efforts.

## Competitor Scope

|Vendor/Scope|SAST        |DAST        |Dep Scanning|Cont Scanning|License Mgmt|
|:-----------|:----------:|:----------:|:----------:|:----------:|:----------:|
|GitLab      |X           |X           |X           |X           |X           |
|BlackDuck   |            |            |X           |X           |X           |
|CA Veracode |X           |X           |X           |            |            |
|IBM AppScan |X           |X           |X           |            |            |
|Fortify     |X           |X           |X           |            |            |
|SonarQube   |            |            |X           |            |            |
|Sonatype    |            |            |X           |X           |X           |
|WhiteSource |            |            |X           |            |X           |


## Role-based Personas

### Security specialist
* managing multiple projects with overall view
* time sensitive
* already in production
* generalist vs. app sec specialist
* security dashboard will be aimed at them

### Developer
* security-aware or security-unaware
* MR with report will be aimed at them

### Security director
* manage team and understand processes
* long term view
* specific security data/dashboard eventually will be aimed at them


## Market Segment Overview
### Companies with sophisticated app SEC programs (target in Q4-18/index.html.md)

{:.no_toc}
#### Characteristics
{:.no_toc}
* Mostly large, Fortune 2000 companies
* Already invested in tools like Veracode or Fortify ($100k-1m+/index.html.md)
* Have dedicated application security professionals - Application Security Engineers
* Probably also engage in threat hunting Threat Intelligence Analysts and security researchers
* Custom code is key to their business
* Often in the financial services industry and for-profit health care providers and insurers
* Large Security budget
* Often application security is funded after a breach, a penetration test or a failed audit.

#### Challenges
{:.no_toc}
* Time to market
* Efficient SDLC balanced with security to protect reputation from risk of data breach

#### Value proposition
{:.no_toc}
* Compliment existing app security tool with GitLab embedded in the developers workflow in order to speed time to market and less cost.
* Improve security by finding more security bugs earlier, clearing some of the noise from security analysts.
* GitLab security will likely not immediately displace other app SEC tools that are already entrenched.
* Opportunity to better integrating security methods and knowledge with a development team.

### Companies with established Security Programs (target Q3-18/index.html.md)

#### Characteristics
{:.no_toc}
* Just starting to focus on Application Security (sweet spot/index.html.md)
* All sizes of companies - even large F2000’s may lack application security focus
* May have a Security Operations Center (SOC/index.html.md) with Security Operations Engineers
* Most security budget is on endpoint security and network security
* Rely on penetration testing for compliance and app sec
* Most advanced may have a web application firewall (WAF/index.html.md)
* Maybe more focused on compliance than threat detection - Compliance Analyst, Risk Management
* May not have substantial in-house code
* Developers likely focus more on integrations and web front-ends

#### Challenges
{:.no_toc}
* Resource constrained
* Application security expertise.

#### Value Proposition
{:.no_toc}
* A low cost and a way of integrating app sec into development with tools they're already using to build and deploy and avoiding the integration cost and effort. They may be concerned about the product being lightweight but may try it as an alternative to costlier dedicated app sec tools

### Companies with minimal security focus (opportunistic target/index.html.md)

#### Characteristics
{:.no_toc}
* SMB, start-ups
* Likely to have one or two security generalists, or IT Operations folks
* No application security program, priority is endpoint security and network (if they are not cloud-focused/index.html.md)
* Rely on penetration testing for compliance and app sec
* Focused on MVC to meet comply with regulatory requirements (GDPR for personally identifiable data, PCI for credit cards, HIPAA for healthcare, etc./index.html.md)
* Want to check the box and say that they are doing application security testing
* Don't plan to invest in improving secure coding and a process improvement.
* May not understand the security findings and need help width prioritization and Remediation.

#### Challenges
{:.no_toc}
* Resource constrained
* Lack of security expertise

#### Value Proposition
{:.no_toc}
* GitLab can help you check the compliance box for security testing and because it’s integrated with your development processes, there is no incremental effort to do so.
