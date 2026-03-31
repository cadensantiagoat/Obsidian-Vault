---
created: 03/30/2026, 02:15
updated: 03/30/2026, 02:15
tags:
  - people
  - Professor
birthday:
associates:
affiliated: "[[California State University Fullerton]]"
aliases:
  - Dr. P
---

> [!info] current age: `= choice(this.birthday, date(today) - this.birthday, "Unknown")`

### Meetings with Dr. Anand Panangadan


```dataview
TABLE start-time AS "Meeting Date", summary AS "Subject"

WHERE contains(people, this.file.link)

SORT date DESC
```