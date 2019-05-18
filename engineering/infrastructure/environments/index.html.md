---
layout: markdown_page
title: "Infrastructure Environments"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Environments

### Development

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Development | various | Development| on save | Fixture | individual dev|

Development happens on a local machine. Therefore there is no way to provide any SLA. Access is to the individual dev. This could be either EE/CE depending on what the developer is working on.

### Demo

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Demo | "GitLab Sales Demo Domains - Internal only" (found on the google drive) | Sales| Release | Fixture | Production Team|

This should be a fully featured version of the current EE release. The high SLA and tightened access is to ensure it is always available for sales. There are no features (feature flags/canary/etc) that we do not ship.

### .org

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
| .org | [dev.gitlab.org](https://dev.gitlab.org) | Tools for Gitlab.com | Nightly | Real Work | Production and build team |

Currently there are two main uses for the .org environment, Builds and repos that are needed in case gitlab.com is offline. This is a critical piece of infrastructure that is always growing in size due to build artifacts. There are discussions to make a new build server where nightly CE/EE builds can be deployed or to move the infra repos to a new host that would be an separate (not gitlab.com) EE instance. Although the environment has dev in its domain name don't refer to it as dev since that could be confused with a local development environment.

### Review Apps

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Review apps | various | Test proposal| on commit | Fixture | Review app owner |

Ephemeral app environments that are created dynamically every time you push a new branch up to GitLab, and they&#39;re automatically deleted when the branch is deleted. Single container with limited access.

### One-off

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
| one-off  | various | Testing specific features in a large environment | Release + patches | User specific  | Team developing feature |

This is less of a staging environment more like a large scale development environments. This could be because of the number of repos required, or a full sized db is required. A version of CE/EE is installed and then patches are applied as work progresses. These should be very limited in number.

### Staging

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Staging  | [staging.gitlab.com](https://staging.gitlab.com) | To test master | Nightly | [Pseudonymization of prod](https://en.wikipedia.org/wiki/Pseudonymization) | all engineers |

**version 0.5**

This is the version we have today. A full environment that is managed by Chef and Terraform (single environment). This setup can at most be updated nightly\* because it requires an omnibus version to install. This would be a static environment with a pseudonymization production database. The DB is a snapshot of the production DB (updated only often enough to keep migration times to a minimum).

If you need an account to test QA issues assigned to you on Staging, you may already have an account as Production accounts are brought across to Staging. Otherwise, if you require an account to be created, create an issue in the [Infrastructure project](https://gitlab.com/gitlab-com/infrastructure/issues/) with the `access request` label.

 \* or however often we can have an omnibus build created.

**Version 1.0**

K8s &amp; helm charts (cloud native)

The final version of staging is multiple container deploys managed by K8s via helm charts. This could be mapped to Master and re-deployed every time there is a successful merge to master.  There is already work started to move us to containers.   [https://gitlab.com/gitlab-org/omnibus-gitlab/issues/2420](https://gitlab.com/gitlab-org/omnibus-gitlab/issues/2420)

### Ops

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
| ops | ops.gitlab.net | GitLab.com Operations | official ee releases | Fixture | SREs |

The ops environment hold all infrastructure that is critical for managing GitLab.com infrastructure.

At this time it includes:

* Proxy for ElasticCloud.
* Internal monitoring infrastructure that serves dashboards.gitlab.net
* An isolated GitLab deployment that serves as a backup for all operations related GitLab repositories.
* CICD jobs for critical operations tasks such as backups and maintenance.
* Runners that need to connect to production infrastructure, such as GitLab chatops.

### GeoPrd (gprd)

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
| gprd | [gprd.gitlab.com](https://gprd.gitlab.com) | HA deployment GCP, production geo secondary | Official releases | Production secondary | Production team |

The Geo-Production environment is currently being used for the transfer of Gitlab.com data
using the Geo feature into GCP. Once the environment is scaled and the data transfer using
the Geo feature is confirmed, the Production environment will be failed over to the GeoPrd
environment, which will then serve all customer traffic on GitLab.com.

### GeoStg (gstg)

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
| gstg | [gstg.gitlab.com](https://gstg.gitlab.com) | HA geo testing in GCP, staging geo secondary | Official releases | Staging secondary | Production team |

The Geo-Staging environment functions as a clone of the GeoPrd environment with
the same topology, but fewer nodes to reduce cost. It is currently being used to validate
the Geo feature by acting as a Geo secondary to the Staging environment.

## Production

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Production  | [gitlab.com](https://gitlab.com) | Production| Release Candidate | Production | Production team |

Production will be full scale and size with the ability to have a canary deploy. Production has limited access.

## Canary

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
| Cny | [gitlab.com](https://gitlab.com) | Production| Release Candidate | Production | Production team |

The canary environment consists of single VMs that are deployed to before a full sitewide deployment is done on Production.
The canary web end can be accessed by setting a cookie in the browser, for more information see [canary  testing](/handbook/engineering/#canary-testing).


## Self-Managed

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Self-Managed  | various | Self hosted versions of CE & EE | User specific  | User specific  | User specific |

These are environments that are run on-premises by the end-user. We have no influence, access or control of these environments.

## Nodes

If you work at GitLab also see the [list of nodes managed by Chef](https://dev.gitlab.org/cookbooks/chef-repo/tree/master/nodes) to get an idea.
