---
created: 03/26/2026, 02:21
updated: 03/26/2026, 02:21
tags:
  - people
birthday: 
associates: 
affiliated: 
aliases: 
---

> [!info] current age: `= choice(this.birthday, (date(today) - this.birthday).years + " years, " + (date(today) - this.birthday).months + " months, " + (date(today) - this.birthday).days + " days", "Unknown")`

### Meetings with Lebron James

```dataview
TABLE date AS "Meeting Date", summary AS "Subject"
WHERE contains(people, this.file.link)
SORT date DESC