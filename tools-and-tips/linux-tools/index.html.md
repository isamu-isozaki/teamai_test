---
layout: markdown_page
title: "Tools"
---

## On this page
{:.no_toc}

- TOC
{:toc}

# Linux Setup
* Linux is allowed as an engineer.  The following is a basic guide to go over
  the basics of what is recommended for installation to get you up and running
  as quickly as possible.
* Not everything listed here may apply to your use case.
* This document will not cover the customization desired for your own personal
  configuration and setup of your desktop/window manager/etc.
* This guide is intended to be very generic. Be aware package names listed
  here may be named differently on your distro of choice.
* And as always, there are multiple ways to do many things, so if you have a
  better preference or are more familiar with another method, feel free to do so
  and contribute back to this document.

## Generic Tooling
* Some common tools are potentially best to download via their site, these
  include:
  * [Google Chrome](https://www.google.com/chrome/)
  * [Slack](https://slack.com/downloads/linux)
  * [Zoom](https://zoom.us/download)
  * Checkout our [Tools page](/handbook/tools-and-tips/) for more potential items.
* It's advised to have some sort of version manager for programming languages as
  what's supplied by repos is typically not sufficient
  * [asdf](https://github.com/asdf-vm/asdf) is pretty good, and usable across
    many platforms
    * This project includes a [large amount of plugins](https://github.com/asdf-vm/asdf-plugins)
      to control various packages as well as languages that you'd need
* Other common packages - this list includes things that always appear to be
  required no matter what realm of work you are in:
  * `gcc`
  * `git`
  * `libereadline-dev`
  * `libssl-dev`
  * `make`
  * `zlib1g-dev`
* Abide by our [security practices](/handbook/security/):

## Production Engineering
* As a Production Engineer, we'll need some common tooling
  * [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/awscli-install-linux.html)
  * [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)
  * [Docker](https://docs.docker.com/install/)
  * [Vagrant](https://www.vagrantup.com/downloads.html)
  * [VirtualBox](https://www.virtualbox.org/wiki/Linux_Downloads)
  * [gcloud CLI](https://cloud.google.com/sdk/docs/#install_the_latest_cloud_tools_version_cloudsdk_current_version)
* Other important packages:
  * `gnupg2`
  * `pwgen`
  * `scdaemon`
  * `yubikey-personalization`
* If you chose to utilize `asdf` as mentioned above, install a few plugins to
  prep yourself to be ready to install a few tools in the future:
  * `asdf install-plugin golang`
  * `asdf install-plugin kubectl`
  * `asdf install-plugin minikube`
  * `asdf install-plugin ruby`
  * `asdf install-plugin terraform`
* Then you'll need to find out which version of the above needs to be installed
  * Check the appropriate repos or ask someone:
  * `asdf install ruby 2.4.4`
  * `asdf install terraform 0.11.5`
  
## Development
* In development, we'll probably need the following packages installed:
  * `cmake`
  * `g++`
  * `krb5`
  * `libkrb5-dev`
  * `libmysqlclient-dev`
  * `libpq-dev`
  * `libre2-dev`
  * `libsqlite3-dev`
* If you chose to utilize `asdf` as mentioned above, install a few plugins to
  prep yourself to be ready to install a few tools in the future:
  * `asdf install-plugin nodejs`
  * `asdf install-plugin postgres`
  * `asdf install-plugin ruby`
* Then you'll need to find out which version of the above needs to be installed
  * Check the appropriate repos or ask someone:
  * `asdf install ruby 2.4.4`
  * `asdf install nodejs 8.11.3`

# Troubleshooting
* Here's a list of common situations that prove to be problematic on linux.
  You'll want to ensure these components work as desired:
  * Audio through various types of headphones
  * Video capturing - Zoom video and Zoom screen sharing
  * Display - screen resolution or video card related issues
