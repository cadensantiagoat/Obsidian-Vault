---
class: "[[CPSCP 488 - Natural Language Processing]]"
professor: "[[Dr. Christopher Ryu]]"
topic: Machine learning and Artificial Neural Networks
date: 08/26/2026
tags:
  - lecture-notes
  - CPSC-488
  - Machine-Learning
  - Artificial-Neural-Networks
created: 08/26/2026, 19:39
updated: 08/26/2026, 19:39
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[L01B_ML_ANN.pdf]]


---

###  Notes
#### <b><u>Machine Learning</u></b>
##### Definition 
- Study of methods to develop a system that can learn
	- ML is core element of almost all AI systems
##### Key components in machine learning
- Learning goal and algorithm
	- find patterns, relationships, functions, or policies
	- learning algorithm selected based on learning goal
- Input *data* or *experience* (datasets)
	- *Data* with or without label
		- data with label (class, target) is called "**training dataset**"
			- everyone wants **labeled data** because it is **generally more powerful**
	- *Experience* from an environment
	there are some jobs where there only task is to create datasets
- Output: knowledge in different forms
	- patterns
	- classes
	- clusters 
	- etc... 
##### Types of Data for machine learning
- Training datasets
	- datasets collected and categorized based on expert knowledge
##### taxonomy of machine learning
- Supervised learning
	- acquire the knowledge or concept from the **training dataset**
- Unsupervised learning
	- option to use when you have **no training datatset** (dataset with no labels)
	- not very good and can be confusing
	- have to do a lot more work to understand data
- Reinforcement learning
	- used in AI agents to make them very powerful and to find optimal solutions 
#### <b><u>Data Preparation and Preprocessing</u></b>
##### How to collect a dataset
- Sampling from a population
	- Population is the complete collection of all elements to be studied
	- Sample is a sub-collection of members selected from a population
	*Why is sampling accurate enough?*
	- <u>Law of large numbers</u>
		- the more samples you collect from the population, the closer the sample mean will be to the population mean
	- <u>Central limit theorem</u>
		- as you collect more and more data, the shape of the data will eventually look like a bell curve and the mean will be in the center of the bell curve
##### data Preprocessing
- Scaling
	- converting data to a specific range
- Normalization
	- every data gives a z score
	- used because you'll have such a wide range that the bell curve will be flat which prevents better accuracy
##### Dimensionality Reduction
- Curse of dimensionality
	- too much data creating "noise"
- Dimensionality reduction
	- methods to get rid of redundant columns to make model more efficient, accurate, and simpler
#### <b><u>Basics of Probability Theories</u></b>
##### Random Variables and Probabilities
- RANDOM VARIABLES (need to know)
	- Random numbers



---

> [!question] Confusions & Questions
> - Why are training datasets useful in machine learning?
> - 

### Action Items & Homework
- [ ] 