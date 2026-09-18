---
class: "[[CPSC 375 - Intro to Data Science & Big Data]]"
professor: "[[Dr. Kanika Sood]]"
topic:
date: 09/18/2026
tags:
  - lecture-notes
  - CPSC-375
created: 09/18/2026, 14:00
updated: 09/18/2026, 14:00
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[CPSC375_W03L04_Exploratory data analysis.pdf]]


---

###  Notes
#### <b><u>Exploratory Data Analysis</u></b>
- Primary objectives in EDA:

	- summary on data
		- describe() function that gives 5pt statistics
	- visualization for data
	- quality of data
		- any outliers, noise, etc...
	- relationship between different features or columns
##### Summary Statistics
- shows mean, median, variance and quartiles
- quartiles used to get IQR = value(Q3) - value(Q1)
##### Data quality
- find if quality of data is good
- handle outliers and missing data
	- isna() or isnull() to find missing data
- check for every column that exists
##### Nummerical vs Categorical Variables
- numerical variables/ordinal variables
	- called ordinal because there is an order to the values
		- ex. 1, 2, 3, ...
		- Age (younger/older), weight(lighter/heavier)
- categorical variables
	- types of values are coming from a preset category
		- ex. primary colors, RGB
		- possible grades for a course: A, B, C, D, F
##### Some special values
- NA: not available
- NaN: not a number
- NaT: not a type


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 