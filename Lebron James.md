---
created: 03/26/2026, 02:53
updated: 03/26/2026, 02:53
tags:
  - people
birthday: 
associates: 
affiliated: 
aliases: 
---

> [!info] current age: `= choice(this.birthday, date(today) - this.birthday, "Unknown")`

### Meetings with Lebron James


```dataview
TABLE date AS "Meeting Date", summary AS "Subject"

WHERE contains(people, this.file.link)

SORT date DESC
```