---
class: "[[CPSC 481 - Applied AI]]"
professor:
topic:
date: 04/28/2026
tags:
  - lecture-notes
  - CPSC-481
created: 04/28/2026, 17:36
updated: 04/28/2026, 17:36
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[Local search.pdf]]


---

###  Notes
#### Optimization Problems
- assign a number to every state (objective function) and find the state with the highest value (global maximum)
	- generic term "optimization problem"
	- highest score "maximization problem"
	- lowest score "minimization problem"
- 8-queens problem
	![[Pasted image 20260428175619.png|256]]
	objective function: count the amount of attacking pairs
	no. of neighbors = 7 x 8 = 56
	size of state space = 8$^{8}$ = 2$^{24}$
	2$^{10}$ ~ 1,000
	2$^{20}$ ~ 1m
	2$^{30}$ ~ 1B
	
#### Local Search
- objective function of my neighbors is nearby what mine is
- Look at the optimization function of my neighbors that are better states than me
#### Hill-Climbing Search
- uses little memory
- can get stuck in local maxima
- if algorithm gets stuck, restart the algorithm from a random point to escape local maxima
#### Simulated Annealing
- set a high temperature (T) at first and slowly lower the temperature
	- high temperature means you are more likely to jump out of a local maxima
- looks like hill climbing
- Search with Simulated Annealing
	![[Pasted image 20260430173753.png|370]]
- Simulated Annealing Example
	![[Pasted image 20260430174109.png|374]]
	What if T = 0?
	exp(-2/0) = exp(-inf) = 1/exp(inf) = 0
#### Genetic Algorithms



---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 