---
class: "[[CPSC 481 - Applied AI]]"
professor: "[[Dr. Anand Panangadan]]"
topic: Uninformed Search
date: 04/07/2026
tags:
  - lecture-notes
  - AI
  - CPSC-481
created: 04/07/2026, 17:39
updated: 04/07/2026, 17:39
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[Uninformed search.pdf]]


---

###  Notes
-  **Search Algorithm Properties**
	- Complete: Guaranteed to find a solution if one exists?
	- Optimal: Guaranteed to find the least cost path?
	- Time Complexity
	- Space Complexity
- **Depth-first tree search** has redundant paths where some states can be reached in more than one way
	- What if there is a loop? 
		- it would cause an infinite loop
		- in implementation you would run out of memory (**stack overflow**)	
	- **Properties:**
		![[Pasted image 20260407175727.png|335]]
		- What nodes does DFS expand?
			- Some left/right prefix of the tree
			- could process the whole tree
			- if m is finite, takes **time** O(b$^{m}$)
		- How much **space** does the frontier take?
			- Only has nodes on path to root + siblings for each: so, O(bm)
		- Is it **complete**?
			- State space can have loops, or could be infinite, so **no**
		- Is it **optimal**?
			- No, it finds the "leftmost" solution, regardless of depth or cost
	- **Depth-first Tree search with loop checking**
		- 



---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 