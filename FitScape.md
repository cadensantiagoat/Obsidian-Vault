---
tags:
status: Active
deadline:
created: 04/20/2026, 23:29
updated: 04/20/2026, 23:29
---

> [!summary] Project Goal
> Mobile App that helps users find outdoor gyms or equipment like pull-bars, dip stations, or machines. Users will be able to post gyms that they find themselves and users can rate and review the gyms.

###  Next Actions
- [x] Figure out best tech stack to use
- [ ] Create database schema in Supabase

###  Project Notes & Resources
#### Tech Stack
- **Frontend**
	React Native with Expo:
	- easy to use without needing to configure native iOS and Android build environments right away
- **Backend**
	Supabase:
	- includes PostgreSQL db, user authentication, and file storage
	- PostgreSQL handles relational structure efficiently
- **Maps & Geolocation**
	react-native-maps
	- community standard map component for React Native
	- displaying native maps is free since they are native device SDKs
- **Geocoding**
	1. OpenStreetMap
		- completely free
		- does not require API key
		- limit of 1 request per second (ok for early-stage app)
	2. Mapbox
		- slightly faster
		- free tier that gives 100,000 free geocoding API requests per month without paying
- **State Management & Navigation**
	React Navigation:
	- industry standard for routing in React Native
	Zustand:
	- managing global app state (keeping track of whether a user is logged in or what their current location is)

#### User-Flow (until diagram is created)
- **Users**
	LOGIN/ CREATE ACCOUNT
	1. Look for gyms in the map
	2. "Create" a gym that they have found.
		- required to take a photo to post a gym
		- once photo is taken the long/lat of the photo will be recorded to give users an exact location of where the gym is within a park or area (assuming that user allows location services)
		- required to attach name of the park itself and attach address of the park (map integration can autocomplete?)
		OPTIONAL
		- add description, review the park, list gym equipment available
	3. Review Gyms
		- account is required
		- Leave a rating
		OPTIONAL 
		- Leave a review
		- Add additional/updated/missing gym equipment
#### Ideas
- tagging system for gyms/exercise
	- ex. strength training, cardio, etc...
