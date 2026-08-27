---
class: "[[CPSCP 488 - Natural Language Processing]]"
professor: "[[Dr. Christopher Ryu]]"
topic: HPC & Deep learning frameworks
date: 08/26/2026
tags:
  - lecture-notes
  - CPSC-488
created: 08/26/2026, 18:59
updated: 08/26/2026, 18:59
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[L01A_HPC.pdf]]


---

###  Notes
#### <b><u>Basics of High -Performance Computing (HPC)</u></b>
##### **Computer Organization**
- Von Neuman architecture
	- the architecture that every CPU uses
##### **High Performance Computing**
- Why do we need HPC?
	- Due to  **matrix vector multiplication** for data compression/encoding
- Measuring Computation Performance
	- Floating-Point Operations Per Second (FLOPS)
		- 1 petaflops: 1,000 teraflops
- CUDA (Compute Unified Device Architecture)
	- Processing Flow on  CUDA
		- Transmission delay when sending instructions from CPU to GPU is massive due to cables
	- Not necessarily the best technology but everyone uses CUDA and it is difficult to have companies migrate to anything else
- Accelerated Processing Unit (APU)
	- integrates a CPU and GPU onto a single chip but is not used very often in reality
- Pros and Cons of Accelerators
	- GPU better than supercomputer for Single Instruction Multiple Data (SIMD) like **matrix multiplication**
- Software Frameworks for HPC
	- OpenCL can handle any GPU
		- Open source standard, cross-platform with complex and varying performance
		- rarely updates their library
- GPU Cores
	- Several cores that are stacked on top of each other which is how they can have so many cores
- CUDA Core Execution
	- utilizes maximum parallelism
	- CUDA architecture gives very detailed way of using your program in a parallel manner


---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] 