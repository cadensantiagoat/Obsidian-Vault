---
class: "[[CPSC 431 - Database and Applications]]"
professor: "[[Thomas Bettens]]"
topic:
date: 04/16/2026
tags:
  - lecture-notes
created: 04/16/2026, 16:03
updated: 04/16/2026, 16:03
---

> [!summary] Lecture Summary
> *(Write a 1-2 sentence summary of this lecture after class)*

###  Materials
*(Drag and drop your PDF slides or syllabus below this line)*
- ![[FinalProject.pdf]]
- [Visual Paradigm Professional 17.2](https://ap.visual-paradigm.com/california-state-univ-fullerton) 
	Used for System Design modeling which includes:
	- UML
	- ERD
	- Data Flow Diagram... 


---

###  Notes
- Expected to show 15-20 second video of execution of two Use Cases
	has to follow Use Case (Steps the user has to take)

### Classroom connection
1. Find Local IP Address on the router
	mac: Open Terminal and type `ifconfig | grep inet` or check your Network Settings.
	
	**This IP address is the URL your classmates will type into their browsers.** (e.g., they will go to `http://192.168.1.15/login.php`).
1. Open Firewall
	**If you are on Mac:** Go to System Settings > Network > Firewall, and temporarily disable it for the presentation, or explicitly allow incoming connections for Docker/Apache.

#### **Use Case**
- shows main success scenario and alternative paths
- sequence diagrams that definitely show success scenario and maybe errors or alternatives 

#### **3-Tier System**
- Client
	Presentation
	1. Request to App (has data)
- App
	2. Authenticate to Database
	4 Response to Client (sending client to homepage)
- Database
	3.  Responds to authentication (probably more exchanges as well)
#### Requirements view
- make them testable
- show non functional requirements and make them testable
- should only cover non functional requirements while use case/testing view shows functional requirements


---

> [!question] Confusions & Questions
> - Don't use Extends or Include in diagram?

### Action Items & Homework
- [ ] 15-20 second video of Use Cases
- [x] Requirements View for presentation
	- [ ] Double check if DB admin is a role needed in requirements view doc
- [ ] Implementation View