---
layout: page
title: User guide
permalink: /guide/
---

## Search page
1. Open **Apps › CQL Search** in the Confluence navigation.
2. Use the **quick filters** – text (or title only), type, space, labels, changed / not changed for, mine, sort. They write the query into the **CQL** box. You can edit the CQL by hand; the filters overwrite it again when you change them.
3. **Search**. Choose the **Columns** you want; click a column header to sort the loaded rows; **Load more** adds the next results.
4. **Copy as table** collects all results (up to 1,000) as tab-separated text with full links. Select all, copy, and paste into Excel, Google Sheets or a Confluence table.
5. **Ready-made searches** (top right) run common reports with fitting columns, for example *Pages not changed for a year* or *Attachments with type and size*.

After a search the **address of the page** holds the query and the columns. Bookmark it or send it to a colleague – opening it runs the search with their permissions.

## Columns
Title (link), Type, Space, Parent, Path (the ancestors in the page tree), Owner, Created by, Created, Last modified by, Last modified, Labels, Version, Excerpt, File type and File size (attachments).

## CQL Results macro
1. Edit a page, type `/cql` and choose **CQL Results**.
2. Open the macro's settings (the pencil) and fill in:
   - **CQL query** – for example `type = page AND space = currentSpace() AND label = "meeting-notes" ORDER BY created DESC`. Try the query on the search page first.
   - **Show as** – a table, a list of links, or only the number of results (for dashboards: "open decisions: 12").
   - **Columns** of the table and the number of **rows shown at first** (10–100; viewers get **Show more**).
   - **Search box** – lets viewers narrow the results by text, for example a search of one space or one label on its own page.
   - **Heading** – optional.
3. Publish. Every viewer sees the results **they** are allowed to see.

In **PDF and Word exports** the macro is exported as a table, list or number with the rows shown at first.

## CQL in one minute
- Fields: `type`, `space`, `title`, `text`, `label`, `creator`, `contributor`, `mention`, `created`, `lastmodified`, `parent`, `ancestor`, `id`.
- Operators: `=`, `!=`, `~` (contains), `in (…)`, `>=`, `<`, `AND`, `OR`, `NOT`, brackets.
- Functions: `currentUser()`, `currentSpace()`, `currentContent()`, `now("-30d")`, `startOfMonth()`, `startOfYear()`.
- Order: `ORDER BY lastmodified DESC`, `created`, `title`.

Examples:
- `type = page AND lastmodified < now("-365d") ORDER BY lastmodified ASC` – pages nobody changed for a year.
- `ancestor = currentContent() AND label = "decision"` – decisions below the page with the macro.
- `type = attachment AND space = "DOCS" ORDER BY lastmodified DESC` – attachments of a space.
- `mention = currentUser() AND lastmodified >= now("-7d")` – where I was mentioned this week.

Full reference: [Advanced searching using CQL](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).
