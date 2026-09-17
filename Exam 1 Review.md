---
class: "[[CPSCP 488 - Natural Language Processing]]"
professor: "[[Dr. Christopher Ryu]]"
topic:
date: 09/16/2026
tags:
  - lecture-notes
  - CPSC-488
  - Exam
created: 09/16/2026, 19:55
updated: 09/16/2026, 19:55
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- 


---

###  Notes
#### <b><u>Computer Organization</u></b>
- difficult to parallelize CPU which is why we added GPU
#### <b><u>HPC</u></b>
- focus on slide 12 and understand the difference between super computer and cluster/hypercluster
- Super computer: mass scale but are connected by cables which slows down everything
	- several computers
	- concentrated in one place
	- works as one giant computer
	- super expensive
	- better performance than cluster but cluster is more accessible
- Cluster: multiple computers tightly connected together 
	- Hypercluster are multiple clusters
#### <b><u>Measuring Computation Performance</u></b>
- know what FLOPS are 
- 1 teraflop: 1,000 gigaflops
- 1 petaflops: 1,000 teraflops
#### <b><u>Pros and Cons of Accelerators</u></b>
- GPU is good for single instruction multiple data
	- CPU sends one instruction and all the data and GPU can handle it quickly
- CPU multiple instruction multiple data
	- GPU slows computation time significantly when trying MIMD
		- CPU would have to keep sending multiple instructions to GPU to do computations
		- this is because there is a bottleneck sending info from CPU to GPU
#### <b><u>Process Flow on CUDA</u></b>
- understand the flow chart
#### <b><u>CUDA Core Execution</u></b>

#### <b><u>Virtualization of Computing Resources</u></b>
- know the concept of containers and kubernetes
#### <b><u>Workloads in the Kubernetes Cluster</u></b>
- know what pod and job are
#### <b><u>Linguistic and NLP Terms</u></b>
- know the terminology
#### <b><u>Foundational NLP Tasks</u></b>
- know basic NLP tasks
#### <b><u>Text Classification</u></b>
- know the basic idea of this
- use more than regression
#### <b><u>Sentiment Analysis</u></b>
- focus on sentiment building words
	- detects attitudes
- used for recommendation systems
#### <b><u>Preprocessing Text for NLP Tasks</u></b>
- tokenization
- skip binary multinominal matrix
#### <b><u>Dealing with Negation</u></b>
- very important
- tells how to capture the meaning
#### <b><u>What if Training Data is Not Enough?</u></b>
- why/when to use lexicons (a library you can use)
	- builds more confidence 
#### <b><u>Vectorizing Text Data</u></b>
- know the idea of one-hot encoding
	- Given the example paragraph create a One-Hot encoding vector
#### <b><u>Word Weighting</u></b>
- know the different frequencies
- weight of word = tf x idf
- TF-IDF Weighted Data
- Dense Vectors: Word embedding


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 