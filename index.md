---
layout: page
title: Overview
permalink: /
---

**CQL Results** searches Confluence with CQL – the Confluence Query Language – and shows what it finds as a table: on a search page for everyone and inside any page.

Confluence search answers "where is that page?". It doesn't answer "which pages has nobody touched for a year, and who owns them?", "which attachments are the largest?" or "show the meeting notes of this space on its home page, newest first". CQL can – and CQL Results makes it usable for everyone:

- **CQL Search page** (Apps › CQL Search) – quick filters write the CQL for you; edit it by hand when you need more. Choose the columns, sort, load more, and **copy all results as a table** for Excel, Google Sheets or a Confluence page.
- **Ready-made searches** – stale pages, recent changes, attachments with type and size, old attachments, recent comments, all spaces and more, one click each.
- **Share a search as a link** – after a search, the page address holds the query and the columns. Bookmark it or send it to a colleague.
- **CQL Results macro** – put the results of a query on a page as a **table**, a **list of links** or just the **number of results**, optionally with a **search box** so readers can narrow the results. `currentSpace()` and `currentContent()` refer to the page with the macro.
- **Works in PDF and Word exports** – the exported page contains the results, not an empty box.

## Safe by design
- Every search runs **with the viewer's own permissions** – people see only what they could find in Confluence search themselves.
- The app is **read-only** and **stores nothing**. No data leaves Atlassian. **Runs on Atlassian.**

Start with the [user guide]({{ '/guide/' | relative_url }}).
