---
tags:
  - project
  - full-stack
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
#### Supabase RDBMS
### 1. `profiles` Table

Supabase handles email/passwords in a hidden `auth.users` table. You create a public `profiles` table to store the data your app actually displays.

- **`id`** (UUID, Primary Key) - _Matches the ID from Supabase Auth_
    
- **`username`** (Text, Unique)
    
- **`created_at`** (Timestamp)
    

### 2. `gyms` Table

This is the core of your map. Every time a user posts a new park, a row goes here.

- **`id`** (UUID, Primary Key)
    
- **`created_by`** (UUID, Foreign Key referencing `profiles.id`)
    
- **`park_name`** (Text, Required)
    
- **`address`** (Text, Required) - _You can use the free tier of the Mapbox Search API for autocomplete._
    
- **`latitude`** (Double Precision / Float, Required)
    
- **`longitude`** (Double Precision / Float, Required)
    
- **`primary_image_url`** (Text, Required) - _Supabase Storage will hold the actual image file, and this column will just store the link to it._
    
- **`description`** (Text, Optional)
    
- **`created_at`** (Timestamp)
    

### 3. `reviews` Table

Since a gym can have many reviews, and a user can write many reviews, we separate this into its own table.

- **`id`** (UUID, Primary Key)
    
- **`gym_id`** (UUID, Foreign Key referencing `gyms.id`)
    
- **`user_id`** (UUID, Foreign Key referencing `profiles.id`)
    
- **`rating`** (Integer, Required) - _Constrained between 1 and 5._
    
- **`review_text`** (Text, Optional)
    
- **`created_at`** (Timestamp)
    

### 4. `equipment_catalog` Table

To keep your app's data clean, it's best to have a predefined list of equipment. If you let users type in text, you'll end up with "Pull up bar", "Pull-up Bar", and "pullup bar", which makes filtering the map impossible.

- **`id`** (Integer, Primary Key)
    
- **`name`** (Text, Required) - _(e.g., Pull-up Bar, Dip Station, Parallel Bars, Sit-up Bench)_
    

### 5. `gym_equipment` Table (The Join Table)

Because your flow mentions users can "Add additional/updated/missing gym equipment" to _existing_ gyms, this table connects a Gym to the Equipment it has, and tracks _who_ added it.

- **`gym_id`** (UUID, Foreign Key referencing `gyms.id`)
    
- **`equipment_id`** (Integer, Foreign Key referencing `equipment_catalog.id`)
    
- **`added_by_user_id`** (UUID, Foreign Key referencing `profiles.id`) - _Tracks who verified this piece of equipment is there._
    
- **`created_at`** (Timestamp) _(Note: The Primary Key for this table would be a composite of `gym_id` and `equipment_id` so the same equipment isn't added twice to the same park)._