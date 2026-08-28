---
created: 08/28/2026, 14:01
updated: 08/28/2026, 14:01
tags:
  - people
birthday: 
associates: 
affiliated: 
aliases: 
---

> [!info] current age: `= choice(this.birthday, date(today) - this.birthday, "Unknown")`

### Meetings with Untitled


```dataview
TABLE start-time AS "Meeting Date", summary AS "Subject"

WHERE contains(people, this.file.link)

SORT date DESC
```

### Notes
- 