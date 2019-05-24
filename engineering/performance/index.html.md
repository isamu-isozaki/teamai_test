---
layout: markdown_page
title: "Performance"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Other Related Pages
{:.no_toc}

- [GitLab.com (infra/index.html.md) Architecture](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/production-architecture/index.html.md/index.html.md)
- [Monitoring GitLab.com](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/monitoring/index.html.md/index.html.md)
- [Application Architecture Documentation](https://docs.gitlab.com/ee/development/architecture.html/index.html.md)
- [GitLab.com Settings](/gitlab-com/settings/index.html.md/index.html.md)
- [GitLab Performance Monitoring Documentation](https://docs.gitlab.com/ee/administration/monitoring/performance/introduction.html/index.html.md)

**Meta issue** to track various issues listed here is at on the [infrastructure tracker](https://gitlab.com/gitlab-com/infrastructure/issues/2373/index.html.md).

## Speed index

### Target

Performance of GitLab and GitLab.com is ultimately about the user experience. As also described in the [product management handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/product/#performance/index.html.md), "faster applications are better applications".

Our target is: an average **Speed Index of less than 2 seconds** for GitLab.com

The [Speed Index](https://sites.google.com/a/webpagetest.org/docs/using-webpagetest/metrics/speed-index/index.html.md) is "the average time at which visible parts of the page are displayed".

There are many other performance metrics that can be useful in analyzing and prioritizing work, some of those are discussed in the sections below. But the user experienced Speed Index is the target for the site as a whole, and should be what everything ties back to in the end.

In everything that is to follow, times are measured from a single geo-location (in Europe/index.html.md) using ["Cable" connectivity](https://sites.google.com/a/webpagetest.org/docs/using-webpagetest/metrics/speed-index#TOC-5Mbps-Cable/index.html.md) for that location (5 /1 Mbps/index.html.md).

### Past and Current Performance

The URLs from GitLab.com listed in the table below form the basis for measuring performance improvements - these are heavy use cases. The times indicate time passed from web request to "the average time at which visible parts of the page are displayed" (per the definition of Speed Index/index.html.md). Since the "user" of these URLs is a controlled entity in this case, it represents an _external_  measure of "Speed Index".

| Type |  End of Q4-17 | Now |
|------|--------------:|-------------:|-------------:|-----|
| Issue List: [GitLab CE Issue List] | | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana issue list]* |
| Issue: [GitLab CE #4058] | [1786] | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana 4058] |
| Issue Boards: [GitLab CE repo boards] | | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana ce boards] |
| Merge request: [GitLab CE !9546] | [19908] | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana 9546] |
| Pipelines: [GitLab CE pipelines] | | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana ce pipelines] |
| Pipeline: [GitLab CE pipeline 9360254] | [2705] | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana pipeline 9360254] |
| Repo: [GitLab CE repo] | [2293] | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana ce repo] |
| Repository: [GitLab CE Repository] | | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana ce repository] |
| Single File: [GitLab Single File Repository] | | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana ce single file repository] |
| Explore: [GitLab explore] | | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana gitlab explore] |
| Snippet: [GitLab Snippet 1662597] | | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>][grafana snippet] |

*To access the sitespeed grafana dashboards you need to be logged into your Google account

<!-- issue links -->
[GitLab CE Issue List]: https://gitlab.com/gitlab-org/gitlab-ce/issues
[GitLab CE #4058]: https://gitlab.com/gitlab-org/gitlab-ce/issues/4058
[7365]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
[2874]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
[1786]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-12-27-19-26-37/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
<!-- MR links -->
[GitLab CE !9546]: https://gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546
[9034]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
[13161]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
[19908]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-12-27-19-26-37/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
<!-- Pipeline links -->
[GitLab CE pipeline 9360254]: https://gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254
[GitLab CE pipelines]: https://gitlab.com/gitlab-org/gitlab-ce/pipelines
[14454]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
[3010]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
[2705]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-12-27-19-26-37/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
<!-- Repo links -->
[GitLab CE repo]: https://gitlab.com/gitlab-org/gitlab-ce/tree/master
[3230]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-29-07-44-06/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html
[2189]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html
[2293]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-12-27-19-26-37/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html
<!-- Issue board links -->
[GitLab CE repo boards]: https://gitlab.com/gitlab-org/gitlab-ce/boards
<!-- GitLab Explore -->
[GitLab explore]: https://gitlab.com/explore
<!-- GitLab Repository-->
[GitLab CE Repository]: https://gitlab.com/gitlab-org/gitlab-ce/tree/master
[GitLab Single File Repository]: https://gitlab.com/gitlab-org/gitlab-ce/blob/master/app/assets/javascripts/main.js
<!-- GitLab Snippets -->
[GitLab Snippet 1662597]: https://gitlab.com/snippets/1662597
<!-- Grafana links -->
[grafana issue list]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_gitlab-org_gitlab-ce_issues&var-browser=chrome&var-connectivity=native&var-function=median
[grafana 4058]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_gitlab-org_gitlab-ce_issues_4058&var-browser=chrome&var-connectivity=native&var-function=median
[grafana 9546]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_gitlab-org_gitlab-ce_merge_requests_9546&var-browser=chrome&var-connectivity=native&var-function=median
[grafana pipeline 9360254]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_gitlab-org_gitlab-ce_pipelines_9360254&var-browser=chrome&var-connectivity=native&var-function=median
[grafana ce repo]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_gitlab-org_gitlab-ce&var-browser=chrome&var-connectivity=native&var-function=median
[grafana ce boards]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_gitlab-org_gitlab-ce_boards&var-browser=chrome&var-connectivity=native&var-function=median
[grafana ce pipelines]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_gitlab-org_gitlab-ce_pipelines&var-browser=chrome&var-connectivity=native&var-function=median
[grafana gitlab explore]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1
[grafana ce repository]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_gitlab-org_gitlab-ce_tree_master&var-browser=chrome&var-connectivity=native&var-function=median
[grafana ce single file repository]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_gitlab-org_gitlab-ce_blob_master_app_assets_javascripts_main_js&var-browser=chrome&var-connectivity=native&var-function=median
[grafana snippet]: https://dashboards.gitlab.net/d/1EBTz3Dmz/sitespeed-page-summary?orgId=1&var-base=sitespeed_io&var-path=default&var-group=gitlab_com&var-page=_snippets_1662597&var-browser=chrome&var-connectivity=native&var-function=median

---

## Steps

### Web Request
{: #flow-of-web-request}

All items that start with the tachometer (<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>/index.html.md) symbol represent a step in the flow that we _measure_. Wherever possible, the tachometer icon links to the relevant dashboard in our [monitoring](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/monitoring/index.html.md/index.html.md). Each step in the listing below links back to its corresponding entry in the [goals table](#web-goals-table/index.html.md).


Consider the scenario of a user opening their browser, and surfing to their dashboard by typing `gitlab.com/dashboard`, here is what happens:

1. <a name="request-reaches-BE"></a> [**User request**](#tb-request-reaches-BE/index.html.md)
    1. <a name="start-request"></a> User enters gitlab.com/dashboard in their browser and hits enter
    1. <a name="lookup-IP"></a> [Lookup IP in DNS](#tb-lookup-IP/index.html.md) (not measured/index.html.md)
       - Browser looks up IP address in DNS server
       - DNS request goes out and comes
    back (typically ~10-20 ms, [data?]; often times it is already cached so
      then it would be faster/index.html.md).
       - For more details on the steps from browser to application, enjoy reading <https://github.com/alex/what-happens-when>
    1. <a name="browser2AzLB"></a> [Browser to Azure LB](#tb-browser2AzLB/index.html.md) (not measured/index.html.md)
       - Now that the browser knows where to find the IP address, browser sends the web
    request (for gitlab.com/dashboard/index.html.md) to Azure's load balancer (LB/index.html.md).
1. <a name="backend-processes"></a> [**Backend processes**](#tb-backend-processes/index.html.md)
    1. <a name="AzLB2HAProxy"></a> [Azure LB to HAProxy](#tb-Az2LB2HAProxy/index.html.md) (not measured/index.html.md)
       - Azure's load balancer determines where to route the packet (request/index.html.md), and
       sends the request to our Frontend Load Balancer(s/index.html.md) (also referred to as
         HAProxy/index.html.md).
    1. <a name="HAProxy-SSL"></a> [HAProxy SSL with browser](#tb-HAProxy-SSL/index.html.md) (not measured/index.html.md)
       - HAProxy (load balancer/index.html.md) does SSL negotiation with the browser
    1. <a name="HAProxy2NGINX"></a> [HAProxy to NGINX](#tb-HAProxy-SSL/index.html.md) (not measured/index.html.md)
       - HAProxy forwards the request to NGINX in one of our front end workers.
       In this case, since we are tracking a web request, it would be the NGINX box in the
         "Web" box in the [production-architecture diagram](https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/production-architecture/index.html.md); but alternatively the request can come in via API or a git command
         from the command line, hence the API, and git "boxes" in that diagram.
        - Since all of our servers are in ONE Azure VNET, the overhead of SSL
          handshake and teardown between HAProxy and NGINX should be close to negligible.
    1. <a name="NGINX-buffer"></a> [NGINX buffers request](#tb-NGINX-buffer/index.html.md) (not measured/index.html.md)
       - NGINX gathers all network packets related to the request ("request
       buffering"/index.html.md). The request may be split into multiple packets by the intervening network,
       for more on that, read up on [MTUs](https://en.wikipedia.org/wiki/Maximum_transmission_unit/index.html.md).
       - In other flows, this won't be true. Specifically, request buffering is
       [switched off for LFS](https://gitlab.com/gitlab-org/gitlab-workhorse/issues/130/index.html.md).
    1. <a name="NGINX2workhorse"></a> [NGINX to Workhorse](#tb-NGINX2workhorse/index.html.md) (not measured/index.html.md)
       - NGINX forwards the full request to Workhorse (in one combined request/index.html.md).
    1. <a name="workhorse2various"></a> [Workhorse distributes request](#tb-workhorse2various/index.html.md)
       - Workhorse splits the request into parts to forward to:
       - <a name="workhorse2unicorn"></a> [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/transaction-overview?panelId=13&fullscreen&orgId=1/index.html.md)
       [Unicorn](#tb-workhorse2unicorn/index.html.md).  Time spent waiting for Unicorn to pick up a request is `HTTP queue time`.
       - <a name="workhorse2gitaly"></a> [Gitaly](#tb-workhorse2gitaly/index.html.md) [not in this scenario, but not measured in any case]
       - <a name="workhorse2nfs"></a> [NFS](#tb-workhorse2nfs/index.html.md) (git clone through HTTP/index.html.md) [not in this scenario, but not measured in any case]
       - <a name="workhorse2redis"></a> [Redis](#tb-workhorse2redis/index.html.md) (long polling/index.html.md) [not in this scenario, but not measured in any case]
    1. <a name="unicorn2various"></a> [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/transaction-overview?panelId=2&fullscreen&orgId=1/index.html.md) [Unicorn calls services](#tb-unicorn2various/index.html.md)
       - Unicorn, (often just called "Rails", or "application server"/index.html.md),
       translates the request into a Rails controller request; in this case
       `RootController#index`. The round trip time it takes for a request to
       _start_  in Unicorn and _leave_ Unicorn is what we call `Transaction
       Timings`. RailsController requests are sent to (and data is received from/index.html.md):
       - <a name="unicorn2db"></a> [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/transaction-overview?panelId=9&fullscreen&orgId=1/index.html.md) [PostgreSQL](#tb-unicorn2db/index.html.md) (`SQL timings`/index.html.md),
       - <a name="unicorn2nfs"></a> [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/daily-overview?panelId=14&fullscreen&orgId=1/index.html.md) [NFS](#tb-unicorn2nfs/index.html.md) (`git timings`/index.html.md),
       - <a name="unicorn2redis"></a> [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/daily-overview?panelId=13&fullscreen&orgId=1/index.html.md) [Redis](#tb-unicorn2redis/index.html.md) (`cache timings`/index.html.md).
       - In this `gitlab.com/dashboard` example, the controller addresses all three [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/rails-controllers?orgId=1&var-action=RootController%23index/index.html.md).
       - There are usually _multiple_ SQL calls (or file, or cache, etc./index.html.md) calls for a given
      controller request. These add to the overall timing, especially since they are
      sequential. For example, in
      this scenario, there are [29 SQL calls (search for `Load`/index.html.md)](http://profiler.gitlap.com/20170524/901687e2-9fa1-4256-8414-c4835dc31dbc.txt.gz/index.html.md)
      when this _particular user_ hits `gitlab.com/dashboard/issues`. The number of SQL calls
      will depend on how many projects the person has, how much may already be in cache, etc.
       - Rails tackles the steps within a controller request sequentially.
          In other words if it needs to make calls out to the database and to
          git, it is not set up to those in parallel but rather has to wait for
          the response to the first step before proceeding to the next step.
       - In the Rails stack, middleware typically adds to the number of round trips
       to Redis, NFS, and PostgreSQL, per controller call, in addition to the
       timings of Rails controllers.  Middleware is used for {session state, user
      identity, endpoint authorization, rate limiting, logging, etc} while the
      controllers typically have at least one round trip for each of {retrieve
      settings, cache check, build model views, cache store, etc.}. Each such
      roundtrip is _estimated_ to take < 10 ms.
    1. <a name="unicorn-views"></a> [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/transaction-overview?panelId=8&fullscreen&orgId=1/index.html.md)  [Unicorn constructs Views](#tb-unicorn-views/index.html.md)
         - The construction of views can take a long time (`view timings`/index.html.md).
         In some controllers, data is gathered _first_ after which a view is
         constructed. In other controllers, data is gathered _from within_  a
         View, so that the `view timing` in those cases includes the time it
         took to call NFS, PostgreSQL, Redis, etc. And in many cases, both are done.
         - A particular view in Rails will often be constructed from multiple partial
        views. These will be used from a template file, specified by the controller
        action, that is, itself, generally included within a layout template.
        Partials can include other partials. This is done for good code
        organization and reuse. As an example, when the _particular user_  from the
        example above loads `gitlab.com/dashboard/issues`, there are [56 nested / partial views rendered (search for `View::`/index.html.md)](http://profiler.gitlap.com/20170524/901687e2-9fa1-4256-8414-c4835dc31dbc.html.gz/index.html.md)
         - Partial views may be cached via various [Rails techniques](http://guides.rubyonrails.org/caching_with_rails.html/index.html.md), such as Fragment Caching. In addition,
         GitLab has a Markdown cache stored in the database that is used to
         speed up the conversion of Markdown to HTML.
         - Perceived performance in the way of First Paint can be affected by
         how much of the content of a view is rendered by the backend vs.
         sending a "minimal" html blob to the user and relying on Javascript /
         AJAX / etc. to fetch additional elements that take the page from First
         Paint to "Fully Loaded". See the section about the frontend for more on this.
    1. <a name="unicorn2html"></a> [Unicorn makes HTML](#tb-unicorn2html/index.html.md) (not measured/index.html.md)
        - Once the Views are built, Unicorn completes making the "HTML blob" that
        is then returned to the browser.
        - Some of these blobs are expensive to compute, and are sometimes hard-coded
      to be sent from Unicorn to Redis (i.e. to cache/index.html.md) once rendered.
    1. <a name="html2browser"></a> [HTML to Browser](#tb-html2browser/index.html.md) (not measured/index.html.md)
       - The HTML blob is sent back to the Browser via the following path:
       - <a name="unicorn2workhorse"></a> [Unicorn to Workhorse](#tb-unicorn2workhorse/index.html.md) (not measured/index.html.md)
       - <a name="workhorse2NGINX"></a> [Workhorse to NGINX](#tb-workhorse2NGINX/index.html.md) (not measured/index.html.md)
       - <a name="NGINX2HAProxy"></a> [NGINX to HAProxy](#tb-NGINX2HAProxy/index.html.md) (not measured/index.html.md)
       - <a name="HAProxy2AzLB"></a> [HAProxy to Azure LB](#tb-HAProxy2AzLB/index.html.md) (not measured/index.html.md)
       - <a name="AzLB2browser"></a> [Azure LB to Browser](#tb-AzLB2browser/index.html.md) (not measured/index.html.md)
1. <a name="renderpage"></a> [**Render Page**](#tb-renderpage/index.html.md)
    1. <a name="browser-firstbyte"></a> [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/gitlab-web-status?refresh=1m&panelId=14&fullscreen&orgId=1&from=now-90d&to=now/index.html.md) [**First Byte**](#tb-browser-firstbyte/index.html.md)
      - The time when the browser receives the [first byte](https://github.com/isamu-isozaki/teamai_test/tree/master/glossary/#first-byte/index.html.md).
      In addition to everything in the backend, this also depends on network speed.
      In the dashboard linked to by the tachometer above, First Byte is measured
      from a Digital Ocean box in the US with relatively little network lag thus
      representing an estimate of _internal_ First Byte. Past performance on
      first byte is recorded [elsewhere on this page](#first-byte-external/index.html.md).
      - For any page, you can use your browser's "inspect" tool to look at "TTFB" (time to first byte/index.html.md).
      - [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/index.html.md/index.html.md)
      `First Byte - External` is measured for a hand selected number of URLs using [SiteSpeed](https://sitespeed.io/index.html.md)
    1. <a name="reaching-speed-index"></a> [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/index.html.md/index.html.md) [**Speed Index**](#tb-reaching-speed-index/index.html.md)
      - Browser parses the HTML blob and sends out further requests
      to GitLab.com to fetch assets such as javascript bundles, CSS, images, and
      webfonts.
      - The timing of this step depends (amongst other things/index.html.md) on the number and
      the size of assets, as well as network speed. For _each_ static asset, there is a
      round-trip of:
            - for cached assets: browser <i class="fas fa-long-arrow-alt-right fa-fw"
           aria-hidden="true"></i> nginx <i class="fas fa-long-arrow-alt-right fa-fw"
           aria-hidden="true"></i> nginx confirms cached asset is still valid <i
           class="fas fa-long-arrow-alt-right fa-fw" aria-hidden="true"></i> browser
            - for non-cached or expired cached assets: browser <i class="fa
           fa-long-arrow-right fa-fw" aria-hidden="true"></i> workhorse <i class="fa
           fa-long-arrow-right fa-fw" aria-hidden="true"></i> workhorse grabs asset
           from local cache <i class="fas fa-long-arrow-alt-right fa-fw"
         aria-hidden="true"></i> browser.
            - for a page that is served through GitLab Pages: browser <i class="fa
           fa-long-arrow-right fa-fw" aria-hidden="true"></i> pages daemon
           (independent service in the architecture/index.html.md) <i class="fas fa-long-arrow-alt-right
           fa-fw" aria-hidden="true"></i> browser.
      - Stylesheets can block page rendering by default, which can lead to
      unnecessary delays in page rendering.
      - Starting in 9.5, scripts won't block rendering anymore as they are
      loaded with `defer="true"`, so they are parsed and executed in the same
      order as they are called but only after html + css has been rendered.
      - Enough meaningful content is rendered on screen to calculated the "Speed Index".
    1. <a name="reaching-fullyLoaded"></a> [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/index.html.md/index.html.md) [Fully Loaded](#tb-reaching-fullyLoaded/index.html.md)
      - When the scripts are loaded, Javascript compiles and evaluates them within the page.
      - On some pages, we use AJAX to allow for async loading. The AJAX call can
      be triggered by all kinds of things; for example a frontend element (button/index.html.md)
      or e.g. the `DOMContentLoaded` event. The new call is for a new URL, and such requests are routed either
      through the Web or API workers, invoke their respective Rails controllers
      on the backend, and return the requested files (HTML, JSON, etc/index.html.md).
      For example, the calendar and activity feeds on a username page `gitlab.com/username`
      are two separate AJAX calls, triggered by `DOMContentLoaded`. (The
      `DOMContentLoaded` event "marks the point when both the [DOM](https://css-tricks.com/dom/index.html.md/index.html.md)
      is ready and there are no stylesheets that are blocking JavaScript
      execution" (taken from an article about the [critical rendering
      path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp/index.html.md)/index.html.md)/index.html.md).
      The alternative to using AJAX would be to include the full Rails code to
      generate the calendar and activity feed within the same controller that
      is called by the gitlab.com/username URL; which would lead to slower First
      Paint since it simply involves more calls to the database etc.


---

### Git Commit Push

First read about the [steps in a web request](#flow-of-web-request/index.html.md) above, then pick up the thread here.

After pushing to a repository, e.g. from the _web UI_:

1. In a web browser, make an edit to a repo file, type a commit message, and hit "Commit"
1. NGINX receives the git commit and passes it to Workhorse
1. Workhorse launches a `git-receive-pack` process (on the workhorse machine/index.html.md) to save the new commit to NFS
1. On the workhorse machine, `git-receive-pack` fires a [git hook](/glossary/#git-hook/index.html.md) to trigger `GitLab Shell`.
   - GitLab Shell accepts Git payloads pushed over SSH and acts upon them (e.g. by checking if you're authorized to perform the push, scheduling the data for processing, etc/index.html.md).
   - In this case, GitLab Shell provides the `post-receive` hook, and the `git-receive-pack` process passes along details of what was pushed to the repo to the `post-receive` hook. More specifically, it passes a list of three items: old revision, new revision, and ref (e.g. tag or branch/index.html.md) name.
1. Workhorse then passes the `post-receive` hook to Redis, which is the Sidekiq queue.
   - Workhorse informed that the push succeeded or failed (could have failed due to the repo not available, Redis being down, etc./index.html.md)
1. Sidekiq picks up the job from Redis and removes the job from the queue
1. Sidekiq updates PostgreSQL
1. Unicorn can now query PostgreSQL.

---

## Goals

### Web Request

Consider the scenario of a user opening their browser, and surfing to their favorite URL on `GitLab.com`. The steps are described in the section on ["web request"](#flow-of-web-request/index.html.md). In this table, the steps are measured and goals for improvement are set.

Guide to this table:
- All times are reported in milliseconds.
- `# per request` : average number of times this step occurs per request. For instance, an average "transaction" may require [0.2 SQL calls, 0.4 git calls, 1 call to cache](https://docs.google.com/spreadsheets/d/15mhXjwkx2lOXJps7lsp_o0zbwGSyOdYOTc8-McwBy0A/pubhtml/index.html.md), and 30 nested views to be built.
- `p99 Q2-17`: the p99 timing (in milliseconds/index.html.md) at the end of Q2, 2017
- `p99 Now`: link to the dashboard that displays the _current_ p99 timing
- `p99 Q3-17`: the target for the p99 timing by the end of Q3, 2017
- Numbers in _italics_ are _per event_  and/or _in parallel_  with other timings, and therefore do not sum to the (sub/index.html.md)totals. The non-italic numbers _do_ sum to the (sub/index.html.md)totals.

<a name="web-goals-table"></a>

| Step                                                    | # per request | p99 Q2-17 | p99 Now | p99 Q3-17 goal | Issue links and impact |
|---------------------------------------------------------|--------------:|--------:|--------:|-------------:|------------------------|
| <a name="tb-request-reaches-BE"></a>[**USER REQUEST**](#request-reaches-BE/index.html.md) |               |         |         |              |                        |
| <a name="tb-lookup-IP"></a>[Lookup IP in DNS](#lookup-IP/index.html.md)                          |     1         |~10| ? |~10|  [Use a second DNS provider](https://gitlab.com/gitlab-com/infrastructure/issues/1711/index.html.md)  |
| <a name="tb-browser2AzLB"></a>[Browser to Azure LB](#browser2AzLB/index.html.md)                    |     1         |~10| ? |~10|                        |
| <a name="tb-backend"></a>[**BACKEND PROCESSES**](#backend-processes/index.html.md) |    |         |         |              | [Extend monitoring horizon](https://gitlab.com/gitlab-com/infrastructure/issues/1879/index.html.md) |
|<a name="tb-AzLB2HAProxy"></a>[Azure LB to HAProxy](#AzLB2HAProxy/index.html.md)                     |     1         |~2| ? |~2|                        |
|<a name="tb-HAProxy-SSL"></a>[HAProxy SSL with Browser](#HAProxy-SSL/index.html.md)                 |     1         |~10| ? |~10| [Speed up SSL](https://gitlab.com/gitlab-com/infrastructure/issues/2321/index.html.md) |
|<a name="tb-HAProxy2NGINX"></a>[HAProxy to NGINX](#HAProxy2NGINX/index.html.md)              |     1         |~2| ? |~2|                        |
|<a name="tb-NGINX-buffer"></a>[NGINX buffers request](#NGINX-buffer/index.html.md)                   |     1         |~10| ? |~10|                        |
|[<a name="tb-NGINX2workhorse"></a>NGINX to Workhorse](#NGINX2workhorse/index.html.md)          |     1         |~2|  ? |~2|                        |
|<a name="tb-workhorse2various"></a>[Workhorse distributes request](#workhorse2various/index.html.md)      |     1         |         |         |      | [Adding monitoring to workhorse](https://gitlab.com/gitlab-com/infrastructure/issues/2025/index.html.md) |
|<a name="tb-workhorse2unicorn"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to Unicorn_](#workhorse2unicorn/index.html.md) | 1 | 18  | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/transaction-overview?panelId=13&fullscreen&orgId=1/index.html.md) | 10 | [Adding Unicorns](https://gitlab.com/gitlab-com/infrastructure/issues/1883/index.html.md) |
|<a name="tb-workhorse2gitaly"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to Gitaly_](#workhorse2gitaly/index.html.md)   | |     | ?  |     |   |
|<a name="tb-workhorse2nfs"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to NFS_](#workhorse2nfs/index.html.md)         | |     | ?  |     |   |
|<a name="tb-workhorse2redis"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to Redis_](#workhorse2redis/index.html.md)      | |     | ?  |     |   |
|<a name="tb-unicorn2various"></a>[Unicorn calls services](#unicorn2various/index.html.md)          |  1  |  2500       | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/transaction-overview?panelId=2&fullscreen&orgId=1/index.html.md)  |  1000 | [Allow more GitLab internals monitoring](https://gitlab.com/gitlab-org/gitlab-ce/issues/28465/index.html.md)    |
|<a name="tb-unicorn2db"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Unicorn_ <i class="fas fa-arrows-alt-h fa-fw" aria-hidden="true"></i> _Postgres_](#unicorn2db/index.html.md)      | | _250_ |[<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/transaction-overview?panelId=9&fullscreen&orgId=1/index.html.md)| _100_ | [Speed up slow queries](https://gitlab.com/gitlab-org/gitlab-ce/issues/34535/index.html.md)  |
|<a name="tb-unicorn2nfs"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Unicorn <i class="fas fa-arrows-alt-h fa-fw" aria-hidden="true"></i> NFS_](#unicorn2nfs/index.html.md)          | | _460_ | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/daily-overview?panelId=14&fullscreen&orgId=1/index.html.md)  | _200_ | [Move to Gitaly](https://gitlab.com/gitlab-org/gitaly/issues/313/index.html.md) - [sample result](https://gitlab.com/gitlab-com/infrastructure/issues/1912#note_31368476/index.html.md) |
|<a name="tb-unicorn2redis"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Unicorn <i class="fas fa-arrows-alt-h fa-fw" aria-hidden="true"></i> Redis_](unicorn2redis/index.html.md)       | |  _18_ | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/daily-overview?panelId=13&fullscreen&orgId=1/index.html.md) |     |   |
|<a name="tb-unicorn-views"></a>[Unicorn constructs Views](#unicorn-views/index.html.md) |  | 1500   | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/transaction-overview?panelId=8&fullscreen&orgId=1/index.html.md)  |  |       |
|<a name="tb-unicorn2html"></a>[Unicorn makes HTML](#unicorn2html/index.html.md) |  |    |   |  |       |
|<a name="tb-html2browser"></a>[HTML to Browser](#html2browser/index.html.md) |  |    |   |  |       |
|<a name="tb-unicorn2workhorse"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Unicorn to Workhorse_](#unicorn2workhorse/index.html.md) | 1 | ~2 | ?  | ~2  |  |
|<a name="tb-workhorse2NGINX"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to NGINX_](#workhorse2NGINX/index.html.md)             |      1        | ~2| ? |~2|                        |
|<a name="tb-NGINX2HAProxy"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_NGINX to HAProxy_](#NGINX2HAProxy/index.html.md)                 |      1        |~2| ? |~2| [Compress HTML in NGINX](https://gitlab.com/gitlab-org/gitlab-ce/issues/33719/index.html.md)  |
|<a name="tb-HAProxy2AzLB"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_HAProxy to Azure LB_](#HAProxy2AzLB/index.html.md)               |      1        |~2| ? |~2|                        |
|<a name="tb-AzLB2browser"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Azure LB to Browser_](#AzLB2browser/index.html.md)               |      1        |~20| ? |~20|                        |
|<a name="tb-renderpage"></a>[**RENDER PAGE**](#renderpage/index.html.md) |  |         |         |              |                        |
|<a name="tb-browser-firstbyte"></a> [**FIRST BYTE**](#browser-firstbyte/index.html.md) (see [note 1](#note-blackbox/index.html.md)/index.html.md)]  |   | **1080 - 6347** |   [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](https://dashboards.gitlab.net/dashboard/db/gitlab-web-status/index.html.md)      | **1000**  |                        |
|<a name="tb-reaching-speed-index"></a>[**SPEED INDEX**](#reaching-speed-index/index.html.md) (see [note 2](#note-fp-times/index.html.md)/index.html.md) |  | **3230 - 14454** | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/index.html.md/index.html.md)  |   **2000**     | [Remove inline scripts](https://gitlab.com/gitlab-org/gitlab-ce/issues/34903/index.html.md), [Defer script loading when possible](https://gitlab.com/gitlab-org/gitlab-ce/merge_requests/12759/index.html.md), [Lazy load images](https://gitlab.com/gitlab-org/gitlab-ce/issues/34361/index.html.md), [Set up a CDN for faster asset loading](https://gitlab.com/gitlab-com/infrastructure/issues/2092/index.html.md), [Use image resizing in CDN](https://gitlab.com/gitlab-org/gitlab-ce/issues/34364/index.html.md) |
|<a name="tb-reaching-fullyLoaded"></a>[Fully Loaded](#reaching-fullyLoaded/index.html.md) (see [note](#note-fl-times/index.html.md)/index.html.md) |  |   6093 - 14003   |  [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/index.html.md/index.html.md)  |  not specified  |   [Enable webpack code splitting](https://gitlab.com/gitlab-org/gitlab-ce/issues/33391/index.html.md) |
|---------------------------------------------------------|---------------|---------|---------|--------------|------------------------|


**Notes:**
- 1\. <a name="note-blackbox"></a> The range here corresponds to the range in First Byte times of the 4 sample URLs provided in the First Byte [table](#first-byte/index.html.md). However, based on all _non-staging_ URL's measured in [this dashboard](https://dashboards.gitlab.net/dashboard/db/gitlab-web-status?refresh=1m&panelId=14&fullscreen&orgId=1&from=now-90d&to=now/index.html.md), between 2017-03-30 and 2017-06-28, the number would be 3,833 ms.
- 2\. <a name="note-fp-times"></a> The range here corresponds to the range in Speed Indices of the 4 sample URLs provided in the Speed Index [table](#speed-index/index.html.md).
- 3\. <a name="note-fl-time"></a> The range here corresponds to the range in Fully Loaded times of the 4 sample URLs provided in the Speed Index [table](#speed-index/index.html.md).


### Git Commit Push

_Table to be built; merge requests welcome!_

## Modifiers

For any performance metric, the following modifiers can be applied:
- **User**: how a _real_  GitLab user would experience and measure the time.
- **Internal**: the time as measured from _inside_  GitLab.com's infrastructure (the boundary is defined as being at the "network | Azure load balancer" interface/index.html.md).
- **External**: the time as measured from any specified point outside GitLab.com's infrastructure; for example a DO box with Prometheus monitoring or a browser in a specified geo-region on a specified network speed.

## First byte

### External

Timing history for First Byte are listed in the table below (click on the tachometer icons for _current_ timings/index.html.md). All times are in milliseconds.

| Type |  End of Q4-17 | Now |
|------|--------------:|-------------:|-------------:|-----|
| Issue: [GitLab CE #4058] | [857]| [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/index.html.md/index.html.md) |
| Merge request: [GitLab CE !9546] | [18673] | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/index.html.md/index.html.md) |
| Pipeline: [GitLab CE pipeline 9360254] | [1529] | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/index.html.md/index.html.md) |
| Repo: [GitLab CE repo] | [1076] | [<i class="fas fa-tachometer-alt fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/index.html.md/index.html.md) |

<!-- issue links -->
[GitLab CE #4058]: https://gitlab.com/gitlab-org/gitlab-ce/issues/4058
[3693]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
[1874]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
[857]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-12-27-19-26-37/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
<!-- MR links -->
[GitLab CE !9546]: https://gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546
[6347]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
[11547]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
[18673]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-12-27-19-26-37/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
<!-- Pipeline links -->
[GitLab CE pipe 9360254]: https://gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254
[2987]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
[1512]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
[1529]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-12-27-19-26-37/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
<!-- Repo links -->
[GitLab CE repo]: https://gitlab.com/gitlab-org/gitlab-ce/tree/master
[1071]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-29-07-44-06/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html
[1096]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html
[1076]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-12-27-19-26-37/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html


### Internal
{: #first-byte-internal}

To go a little deeper and measure performance of the application & infrastructure without consideration for frontend and network aspects, we look at "transaction timings" [as recorded by Unicorn](#unicorn2various/index.html.md). These timings can be seen on the
[Rails Controller dashboard](https://dashboards.gitlab.net/dashboard/db/rails-controllers?orgId=1&var-action=Projects::MergeRequestsController%23show/index.html.md) _per URL that is accessed_ .

For instance, to get the transaction timing for the merge request referenced above first visit the merge request page, then visit the Rails Controller dashboard and scroll down to the [Transaction Details table](https://dashboards.gitlab.net/dashboard/db/rails-controllers?panelId=11&fullscreen&orgId=1&var-action=Projects::MergeRequestsController%23show/index.html.md). We do not currently have time series graphs _per URL_ nor do we have specific targets in terms of what this timing should be.

## Availability and Performance Priority Labels
{: #performance-labels}

To clarify the priority of issues that relate to GitLab.com's availability and
performance you should add the `~performance` label, as well as a "Severity"
label. There are two factors that influence which severity label you should
pick:

1. How frequently something is used.
2. How likely it is for something to cause an outage.

For strictly performance related work you can use the [Controller Timings
Overview](https://dashboards.gitlab.net/dashboard/db/controller-timings-overview?/index.html.md)
Grafana dashboard. This dashboard categorises data into three different
categories, each with their associated severity label:

1. Frequently Used: S2
2. Commonly Used: S3
3. Rarely Used: S4

This means that if a controller (e.g. `UsersController#show`/index.html.md) is in the
"Frequently Used" category you assign it the `S2` label.

For database related timings you can also use the
[SQL Timings Overview](https://dashboards.gitlab.net/dashboard/db/sql-timings-overview?orgId=1/index.html.md).
This is the dashboard primarily used by the Database Team to determine the AP
label to use for database related performance work.

For availability related work you can determine the label as follows:

1. An outage is (almost/index.html.md) guaranteed to occur in the near future: S2
2. An outage is likely to occur in the near future: S3
3. An outage _may_ occur but it's not likely: S4

## Database Performance

Some general notes about parameters that affect database performance, at a very crude level.

- From whitebox monitoring,
   - Of time spent on/by Rails controllers, this much is spent in the database: <https://dashboards.gitlab.net/dashboard/db/rails-controllers?orgId=1&panelId=5&fullscreen> (for a specific Rails controller / page/index.html.md)
   - _Global_ SQL timings: <https://dashboards.gitlab.net/dashboard/db/transaction-overview?panelId=9&fullscreen&orgId=1&from=now-2d&to=now>
- A single HTTP request will execute a single controller. A controller in turn will usually only use one available database connection, though it may use 2 if first a read was performed, followed by a write.
   - pgbouncer allows up to 150 concurrent PostgreSQL connections. If this limit
is reached it will block pgbouncer connections until a PostgreSQL connection becomes available.
    - PostgreSQL allows up to 300 connections (connected, whether they're active or not doesn't matter/index.html.md). Once this limit is reached new connections will be rejected, resulting in an error in the application.
    - When the number of processes > number of cores available on the database servers, the CPU constantly switches cores to run the requested processes; this contention for cores can lead to degraded performance.
- As long as the database CPU load < 100% (<https://dashboards.gitlab.net/dashboard/db/postgresql-overview?refresh=5m&orgId=1&from=now%2Fw&to=now&panelId=13&fullscreen>/index.html.md), then in theory the database can handle more load without adding latency. In practice database specialists like to keep CPU load below 50%.
    - As an example of how load is determined by underlying application design:
       DB CPU percent used to be lower (20%, prior to 9.2, then up to 50-75% [when 9.2 RC1 went live](https://gitlab.com/gitlab-org/gitlab-ce/issues/32536/index.html.md), then back down to 20% by the time 9.2 was released.
- pgbouncer
   - What it does: pgbouncer maps _N_ incoming connections to _M_ PostreSQL connections, with _N_ >= _M_ (_N_ < _M_ would make no sense/index.html.md). For example, you can map 1024 incoming connections to 10 PostgreSQL connections. This is mostly influenced by the number of concurrent queries you want to be able to handle. For example, for GitLab.com our primary rarely goes above 100 (usually it sits around 20-30/index.html.md), while secondaries rarely go above 20-30 concurrent queries. The more secondaries you add, the more you can spread load and thus require fewer connections (at the
  cost of having more servers/index.html.md).
   - Analogy: pgbouncer is a bartender serving drinks to many customers. Instead of making the drinks himself she instructs 1 out of 20 â€œbackendâ€ bartenders to do so. While one of these bartenders is working on a drink the other 19 (including the â€œmainâ€ one/index.html.md) are available for new orders. Once a drink is done one of the 20 â€œbackendâ€ bartenders gives it to the main bartender, which in turn gives it to the customer that requested the drink. In this analogy, the _N_ incoming connections are the patrons of the bar, and there are _M_ "backend"
   bartenders.
   - Pgbouncer frontend connections (= incoming ones/index.html.md) are very cheap, and you have have lots of these (e.g. thousands/index.html.md). Typically you want _N_ >= _A_ with _N_ being the pgbouncer connection limit, and _A_ being the number of connections needed for your application.
   - PostgreSQL connections are much more expensive resource wise, and ideally you have no more than the number of CPU cores available per server (e.g. 32/index.html.md). Depending on your load this may not always be sufficient, e.g. a primary in our setup will need to allow 100-150 connections at peak.
   - Pgbouncer can be configured to terminate PostgreSQL connections when idle for a certain time period, conserving resources.
