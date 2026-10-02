---
class: "[[CPSC 483 - Intro to Machine Learning]]"
professor: "[[Dr. Anli Ji]]"
topic:
date: 10/01/2026
tags:
  - lecture-notes
  - CPSC-483
created: 10/01/2026, 17:33
updated: 10/01/2026, 17:33
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- 


---

###  Notes
#### <b><u>From Linear Regression to Polynomial Regression</u></b>
- What if relationship in data wouldn't fit in a straight line
	- add additional features on top of the existing linear regression model
- Is Polynomial Regression Really Linear?
	- linear refers to our unknown parameters
	- combining coefficients in a linear way
- Polynomial Features
	- works well when you have multiple of the original features 
	- ![[Pasted image 20261001174520.png|318]]
	- higher degree requires more computation and is harder to understand, adds lots of complexity
- Learning Curves
	- shows how performance changes as we give the model more data
	- Underfitting
		- Use better model
		- add usefule features
		- increase polynomial degree
	- Overfitting
		- Feed more training data until the validation error reaches the training error
		- reduce complexity of the model 
#### <b><u>Bias vs. Variance vs. Irreducible Error</u></b>
- Bias
	- wrong assumptions
	- high-bias model most likely to underfit training data
- Variance
	- model reacts very strongly to a particular observation (small noise or fluctuation)
	- associated with overfitting problem
- Irreducible Error
	- due to noisiness of the data itself
	- only way to reduce error is to clean up the data
		- strict, well organized data cleaning process
- Bias/Variance Trade-off
	- Highly complex model = low bias + high variance
	- Very simple model = high bias + low variance
#### <b><u>Complex Models</u></b>
- You can lower the degree to make model less complex
- Can add penalties to model complexity to keep models features (regularization)
- Regularizing Models
	- Minimizes the loss function and the regularized term
	- regularized term tells the complexity of the model based on the coefficient
	- not letting coefficient grow too large
	- like giving the model a budget
	- penalties controlled by hyperparameter α
	- makes model less sensitive to the noise
	- can underfit the model by penalizing too harshly, making the model very simple
		- have to choose hyperparameter term very carefully
	- choose α value that works the best through cross-validation
#### <b><u>Regularizing Models - Three ways</u></b>
- Ridge Regression (L2 regularization)
	- shrinks coefficient close to 0 but most features still remain
	- tells model not to rely on any single feature unless you really need to
- LASSO Regression (Least Absolute Shrinkage and Selection Operator)
	- aka L1 regularization
	- push coefficient **all the way** to 0
		- eliminates the less important features
		- a feature selection type of process
- Elastic Net Regression
	- combines the behavior of LASSO and Ridge together, a middle ground
	- want coefficients to shrink like Ridge but also want feature selection of LASSO
	- useful when we have many features, especially when some of them are strongly related to each other 
#### <b><u>Regularizing Models - Early Stopping</u></b>
- very different way to regularize iterative learning algorithms like gradient descent
- stop training as soon as validation error reaches a minimum
- graph shows that instead of continuously learning, the model begins to overfit
- with stochastic and mini-batch gradient descent there is an issue with early stopping in a local min rather than a global min
	- can be hard to find global min
- keep track of the entire thing to make sure we don't miss the global min
- roll back and restore to the model parameters that had the best results
#### <b><u>From Regression Back to Classification</u></b>
- From numerical back to categorical
- Logistic Regression
	- applied for classification problems, specifically binary classification
	- probability of how much of the instances belong to a positive class or to a negative class
	- How?
		- starts exactly like linear regression
			- calculate a weighted sum
			- add a logistic function (sigmoid function) that takes any real value and maps it between 0 and 1
##### Training Logistic regression - cost function
- Log-loss function (another type of cost function)
	- gives more convenient wait to optimize your objective
	- analyze when the model is confident and wrong
	- penalizes wrong prediction very heavily
	- no analytical solution of how we can make this better
	- must solve by gradient descent (iterative approach)



---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 