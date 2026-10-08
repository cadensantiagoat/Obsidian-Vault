---
class: "[[CPSCP 488 - Natural Language Processing]]"
professor: "[[Dr. Christopher Ryu]]"
topic:
date: 09/16/2026
tags:
  - lecture-notes
  - CPSC-488
created: 09/16/2026, 19:54
updated: 09/16/2026, 19:54
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[L04_LM.pdf]]


---

###  Notes
#### <b><u>Language Model (LM)</u></b>
- calculating the probability of words in a sentence to generate sentences
- can predict next words using joint and conditional probabilities
- designed for generating sentence not necessarily understanding sentences
- more universal
##### Predicting the Next Word with lm
- compute the probability distribution of the next word
- AI chooses words based on context or by highest probability word 
	- if you choose highest probability word then it would generate typical sentences
- have to introduce randomness to AI
##### What can we do with a lm?
- speech recognition improved significantly due to LM
- rank possible sentences
- LLM based on this idea
- us knowing grammar is us calculating the probability of the next words ourselves
##### Example use of language models
- googles auto complete
- speech recognition
##### Markov Model
- looking at current state and recent states
- user chooses how far in the past the states they want to observe
	- going further back increases context window
- simplifies calculations of N gram models
- how we calculate the conditional probabilities
- it's a shortcut to calculating conditional probabilities
	- more accurate probability
- sufficient means that you predict the future 100% of the time with the current/recent states
##### Hidden Markov Model (hmm)
- faster in certain situations
##### N-gram language model
- not as accurate as markov model
##### Dealing with Variable Length Text
- first words are very important for context
- special symbols for a sentence beginning and sentence ending
##### Generating a n-gram sentence
- calculate the conditional probabilities of certain words used together
##### N-gram LMs in Practice
- method for selecting next word
	- MLE (maximum likelihood estimation) to deal with data sparsity
		- sentence would be very boring
##### Using the probability of a sentence
- bigram probabilities for P
- reflects what's going on in the UC Berkeley campus
#### <b><u>Smoothing Methods</u></b>
##### intuition of smoothing
- we lower the probabilities of the frequently used vocab and increase the probabilities of the vocab barely used
- increase the chance of the barely used vocabulary by increasing it a little bit so that there is a chance the vocab is selected
- smoothing only helps generating better sentences
#### <b><u>Evaluation of Language Models</u></b>
##### evaluation of n-gram models
- performance metric for LM 
	- <u>perplexity</u> which is inverse of geometric mean
		- main idea:
			- higher entropy = higher uncertainty 
			- lower entropy = better at predicting next word
##### Geometric mean
- arithmetic mean easily influenced by outliers
- geometric mean more resistant to outliers


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 