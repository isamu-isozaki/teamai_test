---
layout: markdown_page
title: Support Engineer Ops
---

## On this page
{:.no_toc}

- TOC
{:toc}

----

Support Ops are the tools that are created by the support team to automate
tasks or improve our workflows.

## Premium Breach Notifications
{: #premium-breach-notifications}

The premium breach notifications is a webhook that is triggered by a ZenDesk
automation titled `Premium one hour breach tag`. The trigger looks for any
high premium tagged tickets that have less than 2 hours left on the breach clock.
The automation [runs at the top of every hour](https://support.zendesk.com/hc/en-us/articles/203662236-About-automations-and-how-they-work)
and due to this limitation, it does not run at the exact hour the ticket is less than 2 hour from breaching.

Once the ticket is updated, a trigger sends a webhook to slack which is
configured on the slack side.

The webhook is formatted in json:

```json
{
  "attachments":[
    {
        "color":"#FAB617",
        "author_name": "Ticket #{{ticket.id}} - {{ticket.title}}",
        "author_link": "{{ticket.url}}"
    }
  ]
}
```


## Support Live Feed and Services Live Feed
{: #support-live-feed}

The support live feed is a webhook that shows any ticket that is updated. It's
different from the ZenDesk Slack integration because it shows organization
names.

It only updates created and updated tickets.

The Support Live Feed does not display tickets addressed to GitLab.com or
GitHost.io. The Services Live Feed does not display EE tickets.

The webhook is formatted in json:

```json
{
  "attachments": [
  {
     "fallback": "",
     "color": "#4AACD8",
     "pretext": "{{ticket.status}} ticket updated by {{current_user.name}}:
        <{{ticket.link}}|Ticket #{{ticket.id}}>",
        "title": "{{ticket.title}}",
        "author_name": "{{ticket.organization.name}}",
        "title_link": "{{ticket.link}}",
        "text": "{{ticket.latest_comment}}",
        "fields": [
          {
          "short":
          true
          }
     ],
     "footer": "ZenDesk",
     "footer_icon":
     "https://slack-imgs.com/?c=1&o1=wi32.he32.si&url=https%3A%2F%2Fa.slack-edge.com%2F436da%2Fimg%2Funfurl_icons%2Fzendesk.png"
  }
]
}
```

## Other tools
{: #other-tools}

[Supportbot](https://gitlab.com/gl-support/gitlab-support-bot/tree/master/) : Bot for getting ZenDesk tickets.
