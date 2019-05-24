---
layout: markdown_page
title: "Design"
---

## On this page
{:.no_toc}

- TOC
{:toc}

# On Design and Writing

As GitLab.com's levels of functionality and scale increase, so does its complexity. A disciplined approach to meet 
the challenges presented by said complexity is necessary so we can frame technical discussions and increase the 
leverage on technical decisions: **design**.

The late Andy Grove's [*High Output Management*](https://openlibrary.org/books/OL533591M/High_output_management/index.html.md)
highlights his thinking on business reports as an information medium, and these thoughts apply to design as well:

> As [design] is formulated and written, authors are forced to be more precise than they might verbally. Hence, their
value stems from the discipline and the thinking the writers are forced to impose upon theselves and they identify
and deal with trouble spots in their presentation. [Designs] are more a *medium* of *self-discipline* than a way
to communicate information. *Writing* the design is important; reading may not be so as much.

Reading is, of course, important, as it drives information and knowledge sharing as well as healthy technical discussions.
This makes the writing vital. Design clarifies and scopes the problem, drives productive discussions, and presents
decisons concisely. 

Also from the same book:

> All production flows have a basic characteristic: the material becomes more valuable as it moves through the 
process. [...] A common rule we should always try to heed is to detect and fix any problems in a production process
at the *lowest-value* stage possible.

Thus, early scoping and design is a valuable investment. 

Design is not intended to force all decisions up front but to methodically drive them. Time invested in design eliminates
confusion and ambiguity, particularly as it relates to scope, and ensures specific aspects of the engineering work we
perform take place (monitoring being one obvious case/index.html.md).

# Workflow

* Open issue to track design work and submit a Handbook MR with the design.
* Keep design documents in `https://github.com/isamu-isozaki/teamai_test/tree/master/engineering/infrastructure/design/`
* Keep a link to the appropriate issue in the design page
* A [template](template.html/index.html.md) is available to get designs started. This isn't intended to be a strict template,
but it highlights areas that expected to be covered in design. Monitoring is particularly important.

# Design Directory

* [`infra/5088`](https://gitlab.com/gitlab-com/gl-infra/infrastructure/issues/5088/index.html.md) [Storage Nodes](201809_StorageNodes.html/index.html.md)

