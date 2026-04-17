---
class: "[[CPSC 481 - Applied AI]]"
professor: "[[Dr. Anand Panangadan]]"
topic:
date: 04/16/2026
tags:
  - lecture-notes
  - CPSC-481
created: 04/16/2026, 17:33
updated: 04/16/2026, 17:33
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[Informed search.pdf]]


---

###  Notes
#### **A* Search**
- Combines UCS and Greedy
- Data Structures:
	- Frontier: Priority Queue,
	- Explored: Set, for efficiency
![[Pasted image 20260416173542.png|355]]
- Is A* optimal?
	![[Pasted image 20260416173820.png|332]]
	- Need estimates to be less than actual costs
- Conditions for optimality of A*
	1. Heuristic must be admissible
		- Must never overestimate true cost
		- Admissible (optimistic) heuristics slow down bad plans but never outweigh true costs
		- Admissible Heuristics:
			A heuristic *h* is admissible (optimistic) if:
				![[Pasted image 20260416174135.png|138]]
			where *h*$^{*}$(n) is the true cost to nearest goal
	2. Heuristic must be consistent (monotonic)
		- The estimated cost of getting to a goal is never more than cost of an action + estimated cost of next state
		- ![[Pasted image 20260416174828.png|204]]
- Optimality of A* Search
	- Complete: Terminates even on infinite state spaces if a reachable goal exists
	- Optimal: Always finds the closest goal
	- Optimally efficient: No other optimal algorithm with the same heuristics expands fewer nodes
	- Note: Uniform cost search is a special case of A* (h=0)
- Complexity of A* Search
	Time Complexity:
	- number of states still exponential in the length of the solution
	- number of states depends on the "error" in the heuristic
		Error = h$^{*}$(n) - h(n)
	Space Complexity:
	- keeps all generated nodes in memory, so exponential
	A* usually runs out of memory long before it runs out of time
- UCS vs A* Contours
	- Uniformed-cost expands equally in all "directions"
		![[Pasted image 20260416175600.png|114]]
	- A* expands mainly toward the goal, but does hedge its bets to ensure optimality
		![[Pasted image 20260416175338.png|167]]
	
- A* Applications
	- Video games
	- Path planning
	- Resource planning problems
- Creating Heuristics
	Admissible Heuristics:
		- most of the work in solving hard search problems optimally is in coming up with admissible heuristics
		- often are solutions to relaxed problems, where new actions are available
	![[Pasted image 20260416182152.png|267]]
	


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 