```dataview
TABLE status AS "Status", deadline AS "Deadline"
FROM #project
WHERE file.name != "Project Template"
SORT deadline ASC
```
