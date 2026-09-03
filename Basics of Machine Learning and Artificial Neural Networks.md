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
		 ![[Pasted image 20260902202235.png|556]]
		- generate numbers based on probability distribution
			- how to generate probability distribution?
				- Once you find these two every distribution can be explained
					- What is the mean?
					- What is the variance?
##### Fundamental Probability Rules
	- CONDITIONAL PROBABILITY (need to know)
	- JOINT PROBABILITY (need to know)
##### Probability, likelihood, and odds
- Probability
	- can only be calculated when you have a well defined model
- Likelihood
	- used to understand the model given data then you can use the model to find the probability
	- P(X|**Θ**) (we use this one more)
	- L(**Θ**|X) 
##### Probability distribution
- used for discrete variables
##### Gaussian Distribution
- used for continuous variables
- if you still want to use probability distribution then you have to set a range
	- ex. 0-1
##### Bayesian Approach and bayes' rule
- AI and generation heavily relies on Bayes' Rule
- The more data you get the easier it is to get Posterior probability
- Bayesian Influence: Getting as much data as you can to calculate Posterior Probability
- 
#### <b><u>Uncertainty and Entropy</u></b>
- Entropy is a measure of the uncertainty associated with a random variable
##### shannon's Entropy
- measured in binary bits
- The **expected** (average) number of bits needed to encode an outcome from the random variable X
- Entropy relevant for *Classification*
	- we are interested in knowing how uncertain the data is
- Large entropy more certain, smaller entropy is certain
- Logarithm function grows very smoothly
	- also turns multiplication into addition which is simpler, thus we use it a lot
##### Cross-entropy
- Cross-entropy
	- trying to understand how much two probability distributions deviate
	- uses model
	- larger value they divert more, the smaller the value the more identical
	- If they are exactly the same then it has 0 cross-entropy
- Kullback-Leibler divergence
	- another way to calculate cross-entropy
#### <b><u>Supervised Learning for Regression</u></b>
##### Gradient Descent method
- everything we do uses gradient descent
![[Pasted image 20260902213030.png]]
#### <b><u>Artificial Neural Networks</u></b>
##### Popular activation functions
- Sigmoid
	- ideal but takes too long
- ReLU (most popular activation function)
	- calculates max value
	- default activation function in pytorch library
#### <b><u>Training Artificial Neural Networks</u></b>
##### The recipe for supervised learning
1. Give a training data set
2. Define the objective function
	- determine if you want to maximize or minimize
	- most cases in ML is looking to minimize due to minimizing cost function in business
	- take benefit function and multiply by -1 to get minimum function
	- define log loss function to make curve smoother
3. Learn the model using:
	- Gradient
	- parameter update rule




---

> [!question] Confusions & Questions
> - Why are training datasets useful in machine learning?
> - 

### Action Items & Homework
- [ ] 