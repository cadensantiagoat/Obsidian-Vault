---
class: "[[CPSC 375 - Intro to Data Science & Big Data]]"
professor: "[[Dr. Kanika Sood]]"
topic:
date: 11/06/2026
tags:
  - lecture-notes
created: 11/06/2026, 14:04
updated: 11/06/2026, 14:04
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[CPSC375_W08W10_L09_KNN_DistanceMetrics.pdf]]


---

###  Notes
#### K-Nearest Neighbors
- similarity based metric/learning technique
	- k -> # of neighbor
	- nearest -> proximity dist. metric
- uses majority voting
0. Choose k
	- even numbers are no good since they can end with a tie
	- {3, 5, 7, ...} good numbers
		- lower number is cheaper computationally
1. Compute distance with all other neighbors
	- choose dist. metric to compute
2. Sort distances (ascending order)
3. Pick k nearest neighbors and choose their target values
4. majority voting on the neighbors class
- y=mx+c
	- y -> output | future event
	- x -> input | past event/data
- distance metrics
	- euclidean distance
	- jaccard distance
	- manhattan distance
- knn has assumption that my closes neighbors know the most about me



---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 