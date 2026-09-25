---
class: "[[CPSC 483 - Intro to Machine Learning]]"
professor: "[[Dr. Anli Ji]]"
topic:
date: 09/24/2026
tags:
  - lecture-notes
  - CPSC-483
created: 09/24/2026, 17:37
updated: 09/24/2026, 17:37
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
#### <b><u>Evaluating Models</u></b>
- objective way to compare between models
	- comparing them on the same task
- helps us decide the best values for hyperparameters
	- hyperparameters are settings that help us control the models
		- like a control knob that you can change before the learning process
		- you can end up with different predictions for your models
- hyperparameter vs. regular model parameters
	- ![[Pasted image 20260924174525.png]]
	- regular parameters
		- the actual data that we are feeding in
		- the different features/characteristics
	- hyperparameters
		- settings that we enforce
			- ex. restricting depth of a tree or how many splits the tree can do 
- Cross validation
	- train model multiple times and compare how model performs based on the different trainings
	- once final version of retrained model is done do you do final evaluation
- How to evaluate?
	- Binary Classification
		- Generic labels: Positive or Negative
			- only correct answer is positive, other options are negative
		- Ground truth: data given by your data set
		- Predictions: the models output
		- take larger set and sort them in the 2 classes (positive or negative)
		- looks at if the model is making the predictions correctly
			- if truth and prediction match -> true, else false
		- Confusion Matrix (possible outcomes for binary classification)
			- true positive - ground truth and prediction are matching
			- true negative - negative is being predicted correctly
			- false positives - model gives different opinion than ground truth
			- false negative - predicting negative when ground truth is positive
		- Accuracy & Error rate
			- accuracy = (TP + TN) / all
			- error rate = (FP + FN) / all
			- P = TP + FN
			- N = FP + TN
			- all = P + N
			- limitations:
				- class imbalance
					- ![[Pasted image 20260924180422.png]]
					- one class may be rare
##### classifier evaluation metrics
- Confusion Matrix (possible outcomes for binary classification)
	- true positive - ground truth and prediction are matching
	- true negative - negative is being predicted correctly
	- false positives - model gives different opinion than ground truth
	- false negative - predicting negative when ground truth is positive
- Accuracy & Error rate
	- accuracy = (TP + TN) / all
	- error rate = (FP + FN) / all
	- P = TP + FN
	- N = FP + TN
	- all = P + N
	- limitations:
		- class imbalance
			-  ![[Pasted image 20260924180422.png]]
			- one class may be rare
- Precision & Recall
	- Precision: exactness
	- Recall: completeness
	- these are inversely related
- F measures
	- high precision but low recall
	- low precision but high recall
	- ![[Pasted image 20260924181452.png|262]]
	- ![[Pasted image 20260924181509.png|243]]
- Sensitivity & Specificity 
	- if you make classifier very aggressive you will 
	- practice:
		- ![[Pasted image 20260924182517.png]]
		- ![[Pasted image 20260924183610.png]]
- Precision/Recall Trade off
	- compute score based on decision function
		- if score is greater than threshold than it is positive
		- anything below is negative
		- changing threshold varies precision and recall
		- lower threshold = more positive -> high recall
		- higher threshold = more negative -> higher precision
			- shows inverse relationship between recall and precision
	- Precision-Recall Curve
		- can compare model to these scores

---

###  Notes
- 


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 