---
created: 08/23/2026, 23:36
updated: 08/23/2026, 23:36
tags:
  - people
  - CPSC-476
birthday:
associates:
affiliated: "[[California State University Fullerton]]"
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