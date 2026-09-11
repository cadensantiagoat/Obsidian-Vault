---
class: "[[CPSC 483 - Intro to Machine Learning]]"
professor: "[[Dr. Anli Ji]]"
topic:
date: 09/08/2026
tags:
  - lecture-notes
  - CPSC-483
created: 09/08/2026, 17:38
updated: 09/08/2026, 17:38
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- 


---

###  Notes
#### <b><u>Semi-Supervised Learning (aka. Weak Supervision)</u></b>
##### Why?
- lack of training data in real-world
- labeled data (training data) is hard to acquire and expensive
	- requires experts so that the labeling is accurate
- unlabeled data is abundant and cheap
- to prevent overfitting, we increase the sample size
- uses both supervised and unsupervised learning
- unlabeled examples **MUST BE** related to the target labels
##### Inductive learning method
training a classification (or regression) model using both labeled and unlabeled data
- pseudo-lableing (self-training)
	- supervised learning algorithm is trained <u>based on the labeled data </u> only to have a classifier (base model)
	- pseudo-labels are labels assigned by the model that it predicts. 
	- wrapper method
	- co-training
		- multiple base models that work together 
			- Base1 -> unlabeled -> labels
				- Origin + Base1 labels = Base2
			- Base2 -> unlabeled -> labels
				- Origin + Base2
- clustering-based (cluster-than-label)
	- grouped data points based on their similarities
	- first group everything about labeled data
	- every other unlabeled that comes in will be grouped based on my labeled data
- active learning
	- human annotator that only focuses on the last part
##### Unsupervised pre-processing
- auto-encoder
	- learns to represent each image in a more compact way
		- edges, texture, shapes, other patterns
##### Applications
- Google photos uses facial recognition 
- Creating transcripts from audio and labeling what that person said
#### <b><u>Self-Supervised Learning (pseudo-labeling)</u></b>
- starting with completely unlabeled data
##### pretext tasks
- define a task based on the meaning
- you don't care about the final goal but force the model to learn the useful pattern and data itself
##### Capabilities of self-supervised learning
- image completion
- rotation prediction
- "jigsaw puzzle"
- colorization 
##### self-supervised learning vs. others
- vs. supervised learning 
	- supervised requires human-labeled data
	- self-supervised learning generates targets from data itself
- vs. unsupervised learning
	- unsupervised discovers pattern or structure
	- self-supervised creates a specific prediction task
- vs. semi-supervised learning
	- semi-supervised learning uses both labeled and unlabeled datasets
	- self-supervised learning doesn't need labeled data at all and creates supervision directly from the unlabeled data itself
#### <b><u>Reinforcement Learning</u></b>
- **agent** gathers information through interacting with the environment
- learns from surroundings and mistakes, there is no dataset
##### applications
- robot walking
- autonomous vehicles
- playing Go games
- **Policies** - maximize the total rewards at the end
- recommendation systems
##### is rl supervised or unsupervised
- neither but shares characteristics of both
- similar to supervised because there is a target or goal
- similar to unsupervised because explicit goals are not given but forced to learn those optimal goals by trial and error
- have to find a balance between exploiting and exploration
#### <b><u>Other Categories of Machine Learning</u></b>
##### Deep learning
- a more focused version of ML and is not a separate learning paradigm
	- a type of model or architecture people use a lot
	- can be used with other methods like supervised, unsupervised, RL, 
- idea is inspired by the human brain and how it works
- many layers in between input and output layer
	- "deep" refers to the depth of the middle layers
- connections between neurons have a weight assigned to them which represents how important the connection is
	- will pass information no matter what
- bias helps neuron decide if they should pass information onto the next neuron
##### Deep learning vs traditional machine learning
- Traditional
	- depends heavily on the data itself
		- feature engineering
			- manually deciding what features we want to use from an image
		- ![[Pasted image 20260910175108.png]]
- Deep learning
	- needs a large amount of data
	- high amounts of computational resources
	- SHAP
	- Salient map
##### Transfer Learning
- also inspired by the human brain
- take a pre-trained model and use it for a similar task or a specific problem
- learning process is smoother since you don't have to start from scratch
- reduced amount of training data needed and reduced training time since you use a model that is trained already
- can be common in neural networks
- **Tuning** how we make our model perform better
##### Batch Learning vs online learning
- Batch Learning
	- train entire model first then deploy
	- usually offline
	- collect a massive complete dataset
	- have to retrain the entire model when you get a new dataset
	- has to be retrained every once in awhile
	- better when dataset is high quality and you have a smaller dataset
- Online Learning (incremental)
	- train, deploy, and update continuously
	- continuous processing
	- updates model itself
	- better when you need it to adapt
##### Transfer learning vs batch/online learning
- Transfer learning 
	- not a type of online learning
	- not mutually exclusive categories
	- focusses on where the model start
- Online learning
	- can make its own model along the way
##### Ensemble Learning
- combining predictions from multiple models to make our model better
	- multiple models called weak learners
- model works well because mistakes can be handled better, improving performance
- big challenges 
	- model integrity and compatibility
	- computing resources
#### <b><u>Choosing the Right ML Methods</u></b>
- no one model works best 
- look at type of data
	- labels
	- numbers
	- classes
- what are you trying to predict?
	- labels, classes, associations
- find best policy for actions
	- reinforcement learning
#### <b><u>ML-related Roles in the Industry</u></b>
- data engineer
- data scientist
- AI architect
- ML engineer



---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 