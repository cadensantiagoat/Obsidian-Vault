---
class: "[[CPSC 483 - Intro to Machine Learning]]"
professor: "[[Dr. Anli Ji]]"
topic:
date: 10/13/2026
tags:
  - lecture-notes
  - CPSC-483
created: 10/13/2026, 17:39
updated: 10/13/2026, 17:39
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- 


---

###  Notes
#### <b><u>Support Vector Machines (SVM)</u></b>
- supervised machine learning method
- performs both linear and nonlinear classification and regression
#### <b><u>Linear SVM classification</u></b>
- classify data by finding an optimal line (<u>hyperplane</u>) that maximizes the distance between each class
- margin is the space between the classes
##### Hard margin classification
- extremely sensitive to outliers
- have to do outlier detection to remove their effects
##### soft margin classification
- allows some mistakes (margin violations) to happen 
- make mistakes as small as possible
- <u>slack variables</u> allow misclassification of difficult or noisy examples
	- 0 < zeta < 1 means it is still on correct side of hyperplane but within the margin
	- zeta = 0 correct side of the margin, no violation
	- zeta >= 1 wrong side of hyperplane
- Hyperparameter C
	- regularization parameter that controls the penalty for misclassification errors
	- Increase C to decrease tolerance for breaking the margin
#### <b><u>Nonlinear SVM Classification</u></b>
##### polynomial features
- mapping data to high dimension
- same idea as polynomial regression
- problems
	- combinatorial explosion
##### Kernel trick
- we only need dot products in the transformed space
- K(x,z) computes the dot products in higher dimensional feature spaces and calculates the entire thing rather than each feature one by one
- 




---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 