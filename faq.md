---
layout: page
title: FAQ
permalink: /faq/
---

**Who sees what?**
Every search runs with the permissions of the person looking at it – on the search page, in a macro and in an export. Two people can see different rows in the same macro.

**Does the app store my queries or results?**
No. The app stores nothing. A macro's query is part of the page; a shared search is part of its link.

**Can I sort by file size or by owner?**
Click a column header to sort the rows that are loaded. CQL itself orders by fields such as `lastmodified`, `created` and `title`; it can't order by file size.

**How many results can I get?**
The search page loads 50 rows at a time; **Copy as table** collects up to 1,000. A macro shows 10–100 rows at first and loads more on request. Narrow the query for larger sets.

**The number of results looks too high.**
Confluence reports the total from its search index, which can lag a little behind after pages are deleted.

**Can I download a CSV file?**
Use **Copy as table** and paste into Excel or Google Sheets – it keeps the columns and adds full links.

**Is the macro in PDF and Word exports?**
Yes, as a table, list or number, with the rows shown at first and the permissions of the person exporting.

**My CQL gives an error.**
The message from Confluence is shown under the query. Common causes: text values need double quotes (`label = "my-label"`), dates use `now("-30d")`, and `currentSpace()` only works in a macro on a page.

**Does it replace Connect-based CQL search apps?**
It covers the same need on Atlassian's Forge platform: a CQL search page and results in pages. Existing macros of other apps are not migrated automatically – copy their CQL into a CQL Results macro.

**Is my content sent anywhere?**
No. The app runs on Atlassian Forge, is read-only and has no access to anything outside your site.
