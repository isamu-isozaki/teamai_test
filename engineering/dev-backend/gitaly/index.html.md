---
layout: markdown_page
title: "Gitaly Team"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Common Links

- Gitaly's [public issue tracker](https://gitlab.com/gitlab-org/gitaly/issues/).
- [Chat channel](https://gitlab.slack.com/archives/g_gitaly); please use the `#g_gitaly` chat channel for questions that don't seem appropriate to use the issue tracker for.

## What is the Gitaly team?

The Gitaly team is responsible for building and maintaining systems to ensure that the git data storage tier of GitLab instances, and _GitLab.com in particular_, is fast.

The first project that the Gitaly team will be undertaking is a Git [RPC](https://en.wikipedia.org/wiki/Remote_procedure_call) service for handling all the git calls made by GitLab.

The goals of Gitaly are

1. Move git operations as close to the data as possible
1. Optimize git services using caching

See [the design document](https://gitlab.com/gitlab-org/gitaly/tree/master#reason) for an in-depth explanation behind the motivation for GitLab.
