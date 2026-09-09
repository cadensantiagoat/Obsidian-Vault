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
#### <b><u>Self-Supervised Learning</u></b>
- starting with completely unlabeled data
##### pretext tasks
- define a task based on the meaning
- you don't care about the final goal but force the model to learn the useful pattern and data itself
##### Capabilities of self-supervised learning
- image completion
- rotation prediction
- "jigsaw puzzle"
- colorization 



---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 