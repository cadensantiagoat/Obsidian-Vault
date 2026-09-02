---
class: "[[CPSC 483 - Intro to Machine Learning]]"
professor: "[[Dr. Anli Ji]]"
topic: "Chapter 1: Machine Learning vs AI"
date: 08/25/2026
tags:
  - lecture-notes
  - CPSC-483
  - Machine-Learning
created: 08/25/2026, 17:57
updated: 08/25/2026, 17:57
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[CPSC 483 - W01_pdf.pdf]]


---

###  Notes
#### **What is Machine Learning vs What is Artificial Intelligence**
| Machine Learning                                                                                                              | AI                                                                                                                                                            |
| ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| - Algorithm on DS<br>	- Subset of AI<br>	- Models<br>	- Learning something<br>	- Specialized<br>	- Single task<br>	- Patterns | - System<br>	- Prediction<br>	- Large dataset<br>	- Mimic human intelligence<br>	- System completing task<br>	- Multiple task<br>	- Use context from patterns |

#### <b><u>AI?</u></b>
- Types of AI
	- personal recommendation system
	- face filters
	- digital assistants like Siri
- The simulation of human intelligence processes by machines
	- learns from the past to predict the future
#### <b><u>What is Learning?</u></b>
- the process of acquiring knowledge
	- facts: things known to be true
		- pi=3.141592...
	- patterns: repeated forms that represent the nature of facts
	- concepts: classes, class hierarchies created by generalization from patterns
		- dog, cat, bird => Animal (animal class hierarchy)
	- rules: P -> Q
		- if it rains, ground is wet
		- if oil price is too high, people travel less
	- models: abstract representation
		- mathematical functions such as v=d/t
	- skills: being able to do complex activities
		- playing soccer, writing programs, etc
#### <b><u>Machine Learning</u></b>
 "A field of study that gives computers the ability to learn without being explicitly programmed" - Arthur Samuel, 1959
 
 "Any change in a system that allows it to perform better the second time on repetition of the same task or on another task drawn from the same population" - Herbert Simon, 1983
 
 "A computer program that learns from experience E with respect to some class of tasks T and performance measure P. If its performance at tasks in T, is measured by P, it improves with experience E" - Tom Mitchell, 1997
 
- ML is the science/art of programming computers so they can learn from data
- <u>Why does it matter?</u>
	- living in data explosion society
		- everything we do has some sort of data
	- real-time decision-making needs
	- shift from rule-based systems to data-driven systems
	- it'd be difficult to analyze data manually
	- ML can quickly find patterns in data which helps us make data driven decisions or predictions
- Program flagging spam
	- Traditional approach with regards to a program flagging spam
		1. Study the problem
		2. Write rules
		3. Evaluate (if correct 4 if not 5)
		4. Launch!
		5. Analyze errors and go back to 1
	- Machine Learning Approach
		1. Study the problem 
		2. Train ML model
		3. Evaluate (if correct 4 if not 5)
		4. Launch!
		5. Analyze errors and go back to 1
		- <u>Benefit:</u> Automatically adapting to change
			- ML learns rules and patterns from data which saves time and effort
			- Requirements in real world is constantly changing
				- ex. stock market rising and dropping dramatically
			- Ability to stay up to date
			- Helps us understand the problem itself
		- This approach allows automations
		- Solve the whole problem by studying datasets with known inputs
		- Output of training -> **Model**
- Classical Examples of ML Tasks:
	- Pattern Recognition:
		- faces, speech, handwriting... 
		- motion, image synthesis...
	- Anomaly Detection
		- fraud, unusual sensor reading...
	- Prediction
		- market trends, health, weather
- Applications: 
	- Autonomous Cars
		- Use ML to understand sensor data and to predict if your car will hit an object 
	- Scene Labeling
	- Recommendation System
		- Collaborative
			- Learns user interests and groups users together to recommend shows the other hasn't seen
		- Content-based
			- Sends recommendation based on historical data of the user
- Challenges of Machine Learning
	- ill-posed problem
		- in reality we have a limited amount of data which causes a problem
			- **data scarcity**
			- small representation of the whole problem
	- New Goal: a model that **generalizes** beyond the dataset and that is not influenced by the noise in the dataset
		- Upper Bound and Lower Bound
	- Overfitting and Underfitting
		- Underfitting 
			- too simple
			- misses patterns
			- high bias
		- Overfitting
			- too complex
			- fits noise
			- poor generalization
- Criteria for Choosing Models
	- Inductive bias
		- the <u>set of assumptions</u> that define the model selction criteria of a ML algorithm 
			- necessary for learning (beyond the dataset)
			- otherwise we could only perform memorization
	- Two types of bias that we can use:
		- Restriction bias
			- constrains the set of models that the algorithm will consider during the learning process
			- picking one study method and sticking to that one method
		- Preference bias
			- guides the learning algorithm to prefer certain models over others
			- preference for a version of the type of study method we chose
				- leading a study group or simply being in the study group to be taught
- Types of Machine Learning
	- Supervised Learning
		- always a fact or a label given
		- classification
		- regression
	- Reinforcement Learning
	- Unsupervised Learning
		- don't let machine know the facts
		- the machine will group them together on it's own
			- **clustering**


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 
