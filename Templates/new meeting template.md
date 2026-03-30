---
location: Empty
created: <% tp.date.now("MM/DD/YYYY, HH:mm") %>
updated: <% tp.date.now("MM/DD/YYYY, HH:mm") %>
start time: mm/dd/yyyy, 17:00
end time: mm/dd/yyyy, 17:30
people: [<%*
const person = await tp.system.prompt("Who are you meeting with?");
if (person) {
    const fileExists = tp.file.find_tfile(person);
    if (!fileExists) {
        const template = tp.file.find_tfile("new person template"); 
        await tp.file.create_new(template, person);
    }
    tR += `"[[${person}]]"`;
}
%>]
date: mm/dd/yyyy
tags: 
  - meeting
  - IRL
summary: Empty
---

## Agenda
- 

## Notes
- 