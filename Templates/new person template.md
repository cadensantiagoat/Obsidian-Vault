---
location: Empty
created: <% tp.date.now("MM/DD/YYYY, HH:mm") %>
updated: <% tp.date.now("MM/DD/YYYY, HH:mm") %>
start time: mm/dd/yyyy, 17:00
end time: mm/dd/yyyy, 17:30
# The Templater magic for creating/linking a dynamic person note:
# This will prompt you with a selection or allow you to create a new person.
# In the prompt, enter: [[Person Note Name]]
people: [<% tp.file.cursor(1) %>]
date: mm/dd/yyyy
tags: [meeting, IRL]
summary: Empty
---
