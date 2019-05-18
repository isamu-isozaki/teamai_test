---
layout: markdown_page
title: "Production Architecture"
---


Our core infrastructure is currently hosted on several cloud providers,
all with different functions. This document does not cover servers that
are not integral to the public facing operations of GitLab.com.

## On this page
{:.no_toc}

- TOC
{:toc}

## Other Related Pages

- [Application Architecture documentation](https://docs.gitlab.com/ee/development/architecture.html)
- [GitLab.com Settings](/gitlab-com/settings/)
- [Monitoring Performance of GitLab.com](monitoring)
- [GitLab performance monitoring documentation](https://docs.gitlab.com/ee/administration/monitoring/performance/introduction.html)
- [Performance of the Application](/handbook/engineering/performance)
- [Gemnasium service production architecture](gemnasium-service.html)


## Current Architecture
{: #infra-current-archi-diagram}

<img src="/images/handbook/engineering/infrastructure/production-architecture/gitlab-infra.png">

[Source](https://www.draw.io/?state=%7B%22ids%22:%5B%221JVdcF29Nb3fYTZ57YL7xIbFlWm6fW9lC%22%5D,%22action%22:%22open%22,%22userId%22:%22109983779601367693333%22%7D#G1JVdcF29Nb3fYTZ57YL7xIbFlWm6fW9lC)

### Service Architecture
<img src="/images/handbook/engineering/infrastructure/production-architecture/service-arch.png">

[Source](https://www.draw.io/?state=%7B%22ids%22:%5B%221MopYWzl0XDDUmEibEpTOAj2Jhto3dULp%22%5D,%22action%22:%22open%22,%22userId%22:%22109983779601367693333%22%7D#G1MopYWzl0XDDUmEibEpTOAj2Jhto3dULp)

### Database Architecture

<img src="https://docs.google.com/drawings/d/e/2PACX-1vT8Sa-5ktbwB8ZDdBVCvryxPY7RmeifOTm8wBlCKpbDCesOmwEZk6cWlRi2YscGCnTQU725zDMYmmAH/pub?w=960&h=720">

[Source](https://docs.google.com/drawings/d/1htdnQoJ5siedgCrjOjYFHEBTvJb29s_k6L24IRqh6mA/edit), GitLab internal use only

### Storage Architecture

<img src="https://docs.google.com/drawings/d/e/2PACX-1vT3gT8v7GNEOykjTKCYUNp-gslk1eZQSiEmLZPKLt9Dh9BsaQvRrZWFdfpIU7xYApJkhLy5J5VN3cT5/pub?w=960&h=720">

[Source](https://docs.google.com/drawings/d/1ObQRiSf1n6xLTTQdwt8OETP77EIrQzjl4-BhdZ8zp3U/edit), GitLab internal use only

### Monitoring Architecture

<img src="https://docs.google.com/drawings/d/e/2PACX-1vRGbx0P4CQvD-yPZIfDRVsCOKAwo5LGMl9Fa7QKBWYsefEdhR2vmDPdcyGmQCwMZwWQmbmbdlO1SLlf/pub?w=960&h=720">

[Source](https://docs.google.com/drawings/d/1ffCoExVFbSOLu-aOVbM1I0FQ9EmU-vGDtGWQHM9-uj0/edit), GitLab internal use only

## Host Naming Standards

### Hostnames

A hostname shall be constructed by using the service offered by that node, followed by a dash, and a two digit incrementing number.

i.e.: `sidekiq-NN`, `git-NN`, `web-NN`

Service specific identifiers, when it connotes a difference in build or function, will be identified as `-specific` and precede the two digit numeric

i.e.: `sidekiq-realtime-01`

### Service Tiers

Following the hostname shall be the service tier that the node belongs in:
- `sv` for Service
- `lb` for Load Balancer
- `db` for Database Nodes
- `inf` for Infrastructure Nodes

### Environments

Following the service tier shall be the environment:
- `gprd` for Production
- `gstg` for Staging
- `dev` for Development

### TLD Zones

When it comes to DNS names all services providing GitLab as a service shall be in the `gitlab.com` domain, ancillary services in the support of GitLab (i.e. Chef, ChatOps, VPN, Logging, Monitoring) shall be in the `gitlab.net` domain.

## Internal Networking Scheme

We leverage the use of VPC's greatly.  You can see how we configure these for each of our environments and servers in our [terraform repo](https://gitlab.com/gitlab-com/gitlab-com-infrastructure).

### Remote Access

Access is granted to only those whom need access to production.  At this point
in time we utilize bastion hosts.  Instructions for requesting and using the
bastion hosts can be found in our
[runbooks](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/access-gstg-gprd-hosts.md)

## Secrets Management

GitLab utilizes two different secret management approaches, GKMS for machine in side of Google Cloud Provider, and Chef Encrypted Data Bags for all other host secrets.

### GKMS Secrets

Secrets are divided up based upon the Chef role that will be requiring them 
(i.e. Load Balancers, Sidekiq, Storage) and are arranged in JSON files.
The JSON files are encrypted and stored in Google Cloud Storage (GCS) with access
restriction being limited to the environment consuming the keys (i.e. production
servers only have access to the production GCS storage bucket).
The JSON files are encrypted with GKMS keys that are managed by the GKMS service.

#### Node Secret Execution
When a node performs a chef run it pulls the encrypted JSON file out of GCS, makes
a request to the GKMS system as the node, requesting a key to decrypt an object,
and since the nodes have permission the JSON file is decrypted and read into memory
of the current Chef process, making it available for Chef parsing where the secrets
are applied to templates and scripts. Keys are auto-rotated every 90 days.

### Chef Encrypted Data Bags

Secrets are again divided up based upon the Chef role that will be requiring them
and are arranged in JSON structured files. These files are then encrypted and signed with
the individual Chef administrator keys, and the client node keys that need to have access.

#### Node Secret Execution
During a Chef run the client node requests the encrypted data bag from the Chef
server, uses it's own private key to decrypt the contents, and then applies them
to the configuration templates and scripts. Keys are manually rotated roughly every
90 days or whenever we make an change to the Chef administrators, whichever comes first.

## Azure

Azure is where we have lingering infrastructure.  Remaining servers exist here
for a wide variety of reasons.

* Testing/Comparisons with old infrastructure changes
* [Dev](https://dev.gitlab.com)

## Digital Ocean

Digital Ocean houses several servers that do not need to directly interact with our main infrastructure.

* Chef Configuration Management Servers
* Kerberos
* Our backup environment for CI Runners
* [Contributors](https://contributors.gitlab.com)
* [Forum](https://forum.gitlab.com)
* [Quality Insights](http://quality-dashboard.gitlap.com)

## AWS

We host our DNS with route53 and we have several EC2 instances for various purposes. The servers you will interact with most are listed below:

* [License](https://license.gitlab.com)
* [Package](https://packages.gitlab.com)
* [Redash](https://redash.gitlab.com)
* [Version](https://version.gitlab.com)

## Monitoring

See how it's doing, for more information on that, visit the [monitoring handbook](/handbook/engineering/monitoring/).

## Technology at GitLab

We use a lot of cool ([but boring](/handbook/#values)) technologies here at GitLab. Below is a non-exhaustive list of tech we use here.

* [Chef](https://www.chef.io/chef/)
* [Consul](https://www.consul.io)
* [ELK Stack](https://www.elastic.co/products)
* [PostgreSQL](https://www.postgresql.org/)
* [Prometheus](https://prometheus.io/)
* [Redis](https://redis.io/)
* [Ruby](https://www.ruby-lang.org/) (probably goes without saying)
* [Terraform](https://www.terraform.io)

## Proposed Cloud Native Architecture
{: #infra-proposed-cloud-native}

We are working on running GitLab.com on Kubernetes by containerizing all the different services and components that are necessary to run GitLab-EE at GitLab.com scale.

This is the proposed architecture to move from what we are running in static VMs to a container orchestration managed world.

### Pods Definition
{: #infra-proposed-archi-pods}

<img src="https://docs.google.com/drawings/d/e/2PACX-1vT9k6ZoyVGeDlWWrdHFwnGliGi1lC_gVzUy-Al1GJMbqN6Q28vEuMrQuQkyBdvLbaLfpEgPlqyRfGc7/pub?w=935&h=823">

[Source](https://docs.google.com/drawings/d/1BL9hjUUvnZarjO-f_ENoCKdlSTX_MGWXVbZSjkjEd04/edit), GitLab internal use only
