---
class: "[[CPSCP 488 - Natural Language Processing]]"
professor: "[[Dr. Christopher Ryu]]"
topic:
date: 09/02/2026
tags:
  - lecture-notes
  - CPSC-488
created: 09/02/2026, 18:59
updated: 09/02/2026, 18:59
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[L03_TextProcessing_Classification.pdf]]


---

###  Notes
#### <b><u>Vectorizing Text Data</u></b>
- needed so we can process it in our model
	- AI doesn't understand text but it understands numbers, specifically vectors and matrices
	- numbers are then ran through our algorithms
##### Document-term matrix (dtm)
(or Term-Document Matrix)
- horizontally or vertically
- content is the same but one is flipped
- no reason to do one over the other
##### Term-context matrix (tcm)
- terms are on the rows and columns
- gives useful information about the context of the document
- ex. Sentiment Analysis
##### Customized (curated) vectors
- matrix of curated features
	- calculate specifics which allows better accuracy with sentiment analysis
##### raw word frequencies
- models capture context by looking at word frequencies
- some words are more important than others
- there are better ways to get context though over raw word frequencies
	- word weighting 
	- capturing context
##### word weighting 
- count term frequency (the frequency of a particular word)
- document frequency (total # of documents that contain the term)
- if word appears frequently in multiple documents then we assume it's not that important
- if a word is infrequent but appears in a decent amount of documents then we assume it's important
- we automatically take log to "compress" the numbers
	- also turns multiplication into addition
- TF-IDF 
	- balances term frequency and global importance
	- good for document ranking, info retrieval, text classification
	- ignores semantic so not good enough for word prediction or generation
##### Advantages and Limitations of Frequency-based Vectorization
- high dimensional matrix
	- computationally challenging
- sparse matrix 
	- even best writers use only a handful of vocabulary
	- few words in vocabulary is actually used
- unable to capture semantics
	- doesn't get the meaning of the document
##### how can we create a vector that capture word similarity/context
- Word-Word or Term-Context Matrix
	- beginning idea of defining the meaning of vocabulary
		- can't define any vocab word without other vocab words
	- still relies on frequency
##### Dense vectors: word embedding
- what we want because it defines meaningful vocab
- embedding means dense vector that gives meaning
- low dimensionality 
- can capture semantic relationships
- does require a lot of computation


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] Study lecture slides 1-3 for exam 1
	- ML will not be part of exam
	- exam is conceptual
	- understand what the formulas do but not memorize the formula itself
	- skip slides 50-53 in text processing classification