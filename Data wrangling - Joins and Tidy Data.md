---
class: "[[CPSC 375 - Intro to Data Science & Big Data]]"
professor: "[[Dr. Kanika Sood]]"
topic:
date: 10/02/2026
tags:
  - lecture-notes
  - CPSC-375
created: 10/02/2026, 14:06
updated: 10/02/2026, 14:06
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[CPSC375_W05W06L07_Data wrangling-Joins and Tidy Data.pdf]]


---

###  Notes
#### <b><u>Join</u></b>
- can only join if you have common variables
- creates a brand new merged table
- merge(left, right)
	- picks the common value to do the merge
- columns always start from the left table even if you do a right join (MIDTERM QUESTION)
	- left table column order will be picked up
#####  4 types of joins
1. Inner
	- default join if not specified
	- take everything from the left and match it from the right
	- if present in both tables it goes into the new created table
2. Outer (full join)
	- everything in both tables gets merged
3. Left
	- every entry from the left is included in the new table
4. Right
	- every entry on the right table is included in the new table
##### Filter join types
- Semi-join
	- return all rows from the LEFT where there are matching values in RIGHT, keeping just columns from LEFT
- Anti-join
	- return all rows from LEFT where there are not matching values in RIGHT, keeping just columns from LEFT
##### Data structure semantics
- what makes a dataset tidy vs. untidy
	- tidy
		- more narrow but longer
	- untidy
		- wider but shorter
#### <b><u>Tidy Data</u></b>
1. Each variable forms a column
2. Each observation forms a row
3. Each type of observational unit (e.g. persons, schools, counties) forms a table
##### Why tidy data?
- adds consistency which makes our jobs easier in the future
##### Data tidying verbs: .melt()
- Parameters to .melt():
	- id_vars: what we want to keep as columns
	- value_vars: variables to reshape
	- var_name: name of a new column to be created
	- value_name: where we get the values for the new column created
- NA values are not dropped by default
	- can drop by adding
		- .dropna(subset=[value_name]):
- 



---

> [!question] Confusions & Questions
> - Midterm Question:  

### Action Items & Homework
- [ ] 