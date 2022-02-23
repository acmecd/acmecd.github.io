---
layout: page
title: Assignment Info
permalink: /assignment/
---

# Assignment Info

Completed by [Richie Mitish](https://richiemitish.github.io/).

## Questions

How are the Customers using this solution? What are the most common and basic scenarios? FAQs? Examples of services within the Customer's perimeter and their payloads.

## Tools

VSCode, static site generator ([Jekyll](https://jekyllrb.com/) + [Docsy Jekyll](https://github.com/vsoch/docsy-jekyll) theme here).

## Navigation

- site search with search queries analytics is a must
- tags won't hurt
- `Previous` and `Next` buttons are nice to have in case of multi page guides
- breadcrumbs (nice to know where you are when landed from the web search)
- site navigation on the left
- table of contents for each page on the right (nice to know where you are when landed from the web search via any of the anchor links etc)
- support team contacts or live chat/new ticket widget
- API docs being either a part of the site (if possible) or a separate docs site
- ensure old URL => current URL redirection when any page's URL is changed (links management)
- external links must be marked with a corresponding icon next to them

Also a status page would be nice to have.

## Basic scenarios

Engineering staff would need a tutorial on how to construct the objects (of promotion stats, e-comm platform sales data etc) they need out of some service's payload ([Types ans Subtypes](../docs/cs/types) + [Objects](../docs/cs/objects) pages info, some payload parsing visualization in the ACME-CS UI maybe) and create a custom dashboard with those dimensions and metrics etc. Say, some service within the Customer's perimeter collects that data from external sources and the e-comm guys need Devs to set up a new one.

CTO would need the [Data Map Building](../docs/ops/datamap) pages to include that service's payload into the data map, would probably have to have a look at the [golden records](../docs/cs/objects-golden) page for objects optimization suggestions.
