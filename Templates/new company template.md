---
created: <% tp.date.now("MM/DD/YYYY, HH:mm") %>
updated: <% tp.date.now("MM/DD/YYYY, HH:mm") %>
tags: 
  - company
industry: 
website: 
aliases: 
---

### People at <% tp.file.title %>

```dataview
TABLE associates AS "Associates", location AS "Location"
WHERE contains(affiliated, this.file.link)