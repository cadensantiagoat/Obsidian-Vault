---
class: "[[CPSCP 488 - Natural Language Processing]]"
professor: "[[Dr. Christopher Ryu]]"
topic:
date: 09/23/2026
tags:
  - lecture-notes
  - CPSC-488
created: 09/23/2026, 19:01
updated: 09/23/2026, 19:01
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[L05_DistVectorSemantics.pdf]]


---

###  Notes
#### <b><u>Word Semantics</u></b>
##### Representing the word meaning
- linguistic way of thinking
	- using symbols to represent the meaning of the sentence
	- attach every meaning of vocab to create a language
- N-gram
	- not great at finding meaning but good at generating sentence
- Logics
	- ex. MOUSE(x) -> MAMMAL(x)
	- doesn't describe vocab
	- not any better than N-gram
- Lexical semantics
	- tried to define meaning of vocabulary
	- much more specific and adds context and meaning
	- study of word meanings and their relationships
- Relationships
	- Homonymy
		- word that has several different meanings
	- Hypernym
		- you can build a class hierarchy with this
		- ex. Cat IS-A animal
	- Synonym
		- same meaning but are different words
			- ex. couch/sofa
		- no examples of perfect synonym
	- Antonymy
		- opposite senses
			- ex. dark/light, short/long
		- opposite ends of a scale
	- Relatedness
		- words can be related by a semantic field
- Connotation
	- the implied meaning of a word
	- word meaning in 3d space
		- 3 affective dimensions:
			- valence (happy, hate)
			- arousal (crazy)
			- dominance (powerful)
#### <b><u>Better Models for Word Meaning</u></b>
- Meaning by Linguistic Distribution
	- defining a word through other words with related meanings
- Meaning as a Point in Space
	- each word corresponds to one vector
#### <b><u>Computational Models of Word Meaning</u></b>
- Distributional Semantics
	- meaning is given by the words that frequently appear close-by
- Vector semantics
	- word meaning is defined and represented in vector space


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 