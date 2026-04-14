---
class: "[[CPSC 471 - Computer Communications]]"
professor: "[[Dr. Yun Tian]]"
topic: Chapter 5 Network Layer
date: 04/14/2026
tags:
  - lecture-notes
  - CPSC-471
created: 04/14/2026, 10:05
updated: 04/14/2026, 10:05
---

> [!summary] Lecture Summary
> Went over BGP, SDN, ICMP, and Network Management. Study distance algorithms examples in notes (Dijkstra's). 

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[Chapter_5_NetworkLayer-Controlplane.pdf]]


---

###  Notes
#### **BGP Basics**
![[Pasted image 20260414101431.png]]
- eBGP connects ASes to each other
- iBGP connects the routers within ASes
![[Pasted image 20260414101311.png]]
- Can bypass AS 3 to get to X through c2 and a3
- BGP messages
	- OPEN: opens TCP connection to remote BGP peer and authenticates sending BGP peer
	- UPDATE: advertises new path (or withdraws old)
	- KEEPALIVE: keeps connection alive in absence of UPDATES
	- NOTIFICATION: reports errors in previous msg. also closes connection
- Hot potato routing: choose local gateway that has least intra-domain cost
- BGP route selection
	1. local preference value attribute: policy decision
	2. shortest AS-PATH 
	3. closes NEXT-HOP router: hot potato routing 
	4. additional criteria

#### **Software Defined Networking (SDN control plane)**
![[Pasted image 20260414102537.png]]
- per-router control plane: individual routing algorithm components in each and every router interact in the control plane to computer forwarding tables
![[Pasted image 20260414102613.png]]
- Remote controller computes, installs forwarding tables in routers
- Traffic engineering:
	- difficult with traditional routing
	![[Pasted image 20260414102754.png]]
	- What if network operator wants u-to-z traffic to flow along uvwz, rather than uxyz?
		- need to re-define link weights so traffic routing algorithm computes routes accordingly
	![[Pasted image 20260414102843.png]]
	- What if network operator wants to split u-to-z traffic along uvwz and uxyz (load balancing)?
		- can't do it (or need a new routing algorithm)
- Components of SDN controller
	![[Pasted image 20260414103148.png]]
	- OpenFlow Protocol
		- one implementation of SDN
		- operates between controller, switch
		- TCP used to exchange messages
		- 3 classes of OpenFlow messages:
			- controller-to-switch
			- asynchronous (switch to controller)
			- symmetric
		- distinct from OpenFlow API
			- API used to specify generalized forwarding actions
-  Challenges
	- hardening control plane: dependable, reliable, performance-scalable, secure distributed system
	- networks, protocols meeting mission-specific requirements
	- internet-scaling: beyond a single AS
	- SDN critical in 5G cellular networks

#### **Internet Control Message Protocol (ICMP)**
- supports running different apps
- error reporting
- network-layer "above" IP
![[Pasted image 20260414104148.png|205]]
- Traceroute and ICMP
	![[Pasted image 20260414104253.png]]

#### **Network Management**
- autonomous systems (aka "network"): 1000s of interacting hardware/software components
- other complex systems requiring monitoring, configuration, control
- Components:
	*see slides*
	- Managing server
	- Managed device
	- Network management protocol
	- Data
- Operator approaches to management
	- CLI (Command Line Interface)
		- operator issues (types, scripts) direct to individual devices
	- SNMP/MIB
		- operator queries/sets devices data using Simple Network Management Protocol
	- NETCONF/YANG
		- more abstract, network-wide, holistic
		- emphasis on multi-device configuration management
		- YANG: data modeling language
		- NETCONF: communicate YANG-compatible actions/data to/from/among remote devices
- SNMP protocol
	- message types
		![[Pasted image 20260414104950.png|309]]
	- message formats
		![[Pasted image 20260414105030.png|323]]
	- Management Information Base (MIB)
		- managed device's operational data
		- gathered into device MIB module
		- Structure of Management Information (SMI): data definition language 
- NETCONF
	- actively manage/configure devices network-wide
	- operates between managing server and managed network devices
	- remote procedure call (RPC) paradigm
		- NETCONF protocol messages encoded in XML
		- exchanged over secure, reliable transport protocol
	- Operations
		![[Pasted image 20260414105415.png|519]]
- YANG
	- data modeling language used to specify structure, syntax, semantics of NETCONF network management data
	- XML document describing device, capabilities can be generated from YANG description
	- can express constraints among data that must be satisfied by a valid NETCONF configuration


- main takeaway that prof said is if you forget most things remember the importance of divide and conquer and *incremental solving* (not too sure if that's correct for incremental solving)



---

> [!question] Confusions & Questions
> - 

### Action Items & Homework
- [ ] Exam May 5 (Chapters 4, 5, 6 and part of chapter 7)
