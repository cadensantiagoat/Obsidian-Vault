---
created: <% tp.date.now("MM/DD/YYYY, HH:mm") %>
updated: <% tp.date.now("MM/DD/YYYY, HH:mm") %>
tags:
  - people
birthday: 
associates: 
affiliated: 
aliases: 
---

> [!info] current age: `= choice(this.birthday, date(today) - this.birthday, "Unknown")`

### Meetings with <% tp.file.title %>


```dataview
TABLE date AS "Meeting Date", summary AS "Subject"

WHERE contains(people, this.file.link)

SORT date DESC
```