---
class: "[[CPSC 481 - Applied AI]]"
professor: "[[Dr. Anand Panangadan]]"
topic: Python Textbook Code
date: 04/09/2026
tags:
  - lecture-notes
  - AI
  - CPSC-481
created: 04/09/2026, 18:05
updated: 04/09/2026, 18:05
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[AIMA code.pdf]]


---

###  Notes
#### **State Space of the Sliding Tile Puzzle**
![[Pasted image 20260409180935.png|161]]
State:
- Sequence of tiles
- Number of tiles
- Dimensions of the board
- Information on the board position
- A 9-element tuple/array
- Blank represented by 0
- For Example:
	(5,2,7,8,4,0,1,3,6)
	![[Pasted image 20260409180954.png|112]]

Operators: one for sliding each square in each of four directions
- Better, one for moving the blank square in each of four directions
	possible_actions = ['UP', 'DOWN', LEFT', 'RIGHT'] # Python List

**What are the valid actions in a given state?**
![[Pasted image 20260409181601.png|325]]
![[Pasted image 20260409181649.png|505]]

**What is the *result* state after an action?**
![[Pasted image 20260409183149.png|332]]
![[Pasted image 20260409183313.png|399]]
- "new_state = list(state)" is written this way because types in python are immutable
	- if for example state was already of list type, you would have to write:
		"new_state = state.copy()" instead of
		"new_state = state"
		because python does assignment by reference instead of by value


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 