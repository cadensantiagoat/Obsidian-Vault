```
TABLE date AS "Meeting Date", people AS "Attendees", summary AS "Subject"
WHERE contains(tags, "meeting")
SORT date DESC
```
