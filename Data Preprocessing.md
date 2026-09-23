---
class: "[[CPSC 483 - Intro to Machine Learning]]"
professor: "[[Dr. Anli Ji]]"
topic:
date: 09/22/2026
tags:
  - lecture-notes
  - CPSC-483
created: 09/22/2026, 17:33
updated: 09/22/2026, 17:33
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- 


---

###  Notes
#### <b><u>Feature Transformation</u></b>
##### Scaling
- changing categorical to numerical is a form of feature transformation
- the way data is collected is not always the best for machine learning
- huge difference in scale can affect how the model treats those features
- changing how the information is presented to us
- Min-max scaling (normalization)
	- transforming it into a fixed range
	- keeps data with same distribution
	- allows to compare between 2 different values
	- sensitive to outliers
- Standardization
	- calculate mean of the entire set of features
	- take x, subtract by the mean, divide by std deviation
##### Custom Transformers
- apply a different mathematical function
- do we discover new features that could be relevant to that data?
- can chain several transformations together
#### <b><u>Create a Test Set</u></b>
##### sampling
- split data into to training set and testing set


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 