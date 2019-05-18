---
layout: markdown_page
title: "Database"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Database Reliability at GitLab

The group of Database Reliability Engineers is part of the SRE team that
runs GitLab.com. We care most about database reliability aspects of the
infrastructure and GitLab as a product.

We strive to approach database reliability from a data driven
perspective as much as we can. As such, we start by defining Service
Level Objectives below and document what service levels we currently aim
to maintain for GitLab.com.

Also see the [database team organization page](/handbook/engineering/infrastructure/database/team.html).

## Database SLOs

We use [Service Level Objects](https://en.wikipedia.org/wiki/Service_level_objective) (SLOs) to reason about the performance and
reliability aspects of the database. We think of SLOs as "commitments by
the architects and operators that guide the design and operations of the
system to meet those commitments."[^1]

This list is by no means complete and we're just about to define SLOs
and document them here. See [#147](https://gitlab.com/gitlab-com/database/issues/147).

### Backup and Recovery

In backup and recovery, there are two SLOs:

| SLO           | Current level | Definition |
| ------------- |:-------------:| -----:|
| `DB-DR-TTR`  | 8 hours       | Maximum time to recovery from a full database backup in case of disaster|
| `DB-DR-RETENTION`  | 7 days       | The number of days we keep backups for recovery purposes. |

The backup strategy is to take a daily snapshot of the full database
(basebackup) and store this in AWS S3. Additionally, we capture the
write-ahead log data in S3 to be able to perform point-in-time recovery
(PITR) using one of the basebackups.

For `DB-DR-TTR` we need to consider worst-case scenarios with the
latest backup being 24 hours old. Hence recovery time includes the time
it takes to perform PITR to recover from archive to a certain point in
time (right before the disaster).

We are able to recover to any point in time within the last `DB-DR-RETENTION` days.

### High Availability

For [GitLab.com we maintain availability](/handbook/engineering/infrastructure/production/#gitlabcom) above 99.95%. For the PostgreSQL database,
we define the following SLOs:

| SLO            | Level       | Definition |
| -------------- |:-----------:| ----------:|
| `DB-HA-UPTIME` | 99.9%       | General database availability |
| `DB-HA-PERF`   | p99 < 200ms | 99th percentile of database queries runtime below this level. |
| `DB-HA-LOSS`   | 60s         | Maximum accepted data loss in face of a primary failure |

A `DB-HA-UPTIME` of 99.9% allows for roughly 45 minutes of downtime per month. Uptime means, the database cluster is available to serve
queries from the application while maintaining other database SLOs.

We allocate a downtime budget of 45 minutes per month for planned downtimes,
although we strive to keep downtime as low as possible. The downtime
budget can be used to introduce change to the system. If the budget is
used up (planned or unplanned), we stop introducing change and focus on
availability (similar to SRE [error budgets](https://landing.google.com/sre/book/chapters/embracing-risk.html)).

As for `DB-HA-PERF`, 99% of queries should finish below 200ms.

With `DB-HA-LOSS` we require an upper bound on replication lag. A write
on the primary is considered at risk as long as it has not been
replicated to a secondary (or to the PITR archive).

[^1]: From "Database Reliability Engineering", O'Reilly Media, 2017
