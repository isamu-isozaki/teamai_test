---
layout: markdown_page
title: "Production Onboarding"
---

## On this page
{:.no_toc}

- TOC
{:toc}


## Dashboards

It is useful to have the following dashboards bookmarked and easily accessible

1. [Grafana](https://dashboards.gitlab.net/dashboard/db/triage-overview?refresh=1m&orgId=1/index.html.md)
1. [Google Cloud](https://console.cloud.google.com/home/dashboard?project=gitlab-production&pli=1/index.html.md)
1. [System Logs](https://log.gitlab.net/app/kibana/index.html.md)
1. [Fastly](https://manage.fastly.com/dashboard/services/652MHuIME217ZATbh7vFWC/datacenters/all/index.html.md) CDN

### Cloud Providers

1. [Google Cloud](https://console.cloud.google.com/home/dashboard?project=gitlab-production&pli=1/index.html.md)
1. [Amazon Web Services](https://console.aws.amazon.com/console/home?region=us-east-1#/index.html.md)
1. [DigitalOcean ](https://cloud.digitalocean.com/dashboard/index.html.md)
1. Azure

### Monitoring tools

1. [PagerDuty](https://gitlab.pagerduty.com/incidents/index.html.md) Alerting
1. [Grafana](https://dashboards.gitlab.net/dashboard/db/host-stats?refresh=1m&orgId=1&var-node=about.gitlab.com/index.html.md) Peformance Monitoring

### Issue Trackers

It is useful to have the following issue trackers bookmarked and easily accessible

1. [On Call](https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=âœ&state=opened&label_name%5B%5D=oncall/index.html.md)

### Yubikey

Production Engineers should be using a [YubiKey](https://www.yubico.com/index.html.md) and should not have keys on their laptop.

Follow the [yubikey runbook](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/yubikey.md/index.html.md) to set up

## Credentials

The following is intended to be a comprehensive list of credentials and access
that need to be set up, which are not covered above or elsewhere in the handbook.
The list may not be up to date.  If something is missing, please add it.

1. SSH Key - this is provided to you by the yubikey setup
1. [GitLab.com](https://gitlab.com/index.html.md) account
1. [GitLab.com](https://gitlab.com/index.html.md) admin account
1. [dev.GitLab.org](https://dev.gitlab.org/index.html.md) account
1. Chef access
1. Cloud Providers
  - Amazon Web Services
  - Azure
  - Digital Ocean
  - Google Cloud

# Slack Channels

1. #production  (Say hello to @marvin to create an account/index.html.md)
1. #sre-lounge
1. #alerts (There are several alerts channels/index.html.md)

## Suggested Software Tools

As production engineers we are allowed to utilize a linux workstation.  The list
below is mostly comprised of OSX tools.  You'll need to find the linux
equivalent to match the linux distro of your choice.

In addition to the standard tools for interacting with the rest of GitLab,
the following tools help when working on production issues.

Required tools
1. [Homebrew](https://brew.sh/index.html.md)
1. SSH, properly configured
1. chef, knife, berkshelf
1. kubectl (`brew install kubernetes-cli`/index.html.md)

Nice to have
1. iTerm (`brew cask install iterm2`/index.html.md)
1. A text editor such as [Atom](https://atom.io/index.html.md/index.html.md), [Sublime](https://www.sublimetext.com/index.html.md/index.html.md), [Textmate](https://macromates.com/index.html.md), [MacVim](http://macvim-dev.github.io/macvim/index.html.md/index.html.md), or [neovim](https://neovim.io/index.html.md)
1. watch (`brew install watch`/index.html.md)
1. tmux/tmate (`brew install tmux tmate`/index.html.md)
1. A markdown editor such as [macdown](https://macdown.uranusjr.com/index.html.md) (`brew cask install macdown`/index.html.md)
1. gsed (`brew install gnu-sed`/index.html.md)

To [replace mac utilities with gnu core utilities]( https://apple.stackexchange.com/questions/69223/how-to-replace-mac-os-x-utilities-with-gnu-core-utilities/index.html.md) use the --with-default-names option.

### Brew Files

There are sample brew files in the [Infrastructure Project](https://gitlab.com/gitlab-com/infrastructure/index.html.md)

### iOS apps

1. [Slack](https://itunes.apple.com/us/app/slack/id618783545?mt=8/index.html.md)
1. [Zoom](https://itunes.apple.com/us/app/zoom-cloud-meetings/id546505307?mt=8/index.html.md)
1. [PagerDuty](https://itunes.apple.com/us/app/pagerduty/id594039512?mt=8/index.html.md)
1. [Working Copy](https://itunes.apple.com/us/app/working-copy/id896694807?mt=8/index.html.md) (Optional/index.html.md)

## Reference Material

List of relevant reference material that an engineer may need to brush up on

1. [Chef](https://docs.chef.io/index.html.md)
1. [Terraform Docs](https://www.terraform.io/docs/index.html/index.html.md) or [getting started guide](https://www.terraform.io/intro/index.html/index.html.md)
