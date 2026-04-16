---
created: 04/16/2026, 16:02
updated: 04/16/2026, 16:02
tags:
  - people
  - Professor
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