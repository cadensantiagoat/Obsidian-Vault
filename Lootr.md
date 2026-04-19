---
tags:
  - fully-hacks-2026
status: Active
deadline:
created: 04/18/2026, 18:04
updated: 04/18/2026, 18:04
---

> [!summary] Project Goal
> Take a photo of an object and turn it into a game

###  Next Actions
- [ ] need to know what the absolute maximum and minimum playable values are in the physics engine and set the Zod to those limits.
- [ ] setup Neon Postgres Database
- [ ] Implement actual ArcGIS REST API POST request in services/arcgis.service.js
- [ ] implement Human Delta API request in services/human-delta.service.js

###  Project Notes & Resources
#### **Tech Stack**
- react native
- Groq llm
- Media Pipe
- Node.js/Express.js (backend)
- Neon (Database)
#### **Features**
- camera scan
- map that shows games that others have made and their location
#### **2d games**
	- balancing
	- catching
	- side scrolling
	- dodging
	- stacking 
#### **Database**
Stores games created, who made them, and the leaderboard for each game. 

#### **How to Connect React Native App to Lootr Backend**
### 1. Running the Backend Locally

Before the app can talk to the backend, you need to have the server running on your computer.

1. Pull the latest code from GitHub.
    
2. Open your terminal, navigate to the `backend` folder, and install the dependencies:
    
    Bash
    
    ```
    cd backend
    npm install
    ```
    
3. **CRITICAL:** Create a `.env` file inside the `backend` folder and add the Groq API key (ask me for the key if you don't have it!). It should look like this:
    
    Plaintext
    
    ```
    GROQ_API_KEY=your_api_key_here
    ```
    
4. Start the server:
    
    Bash
    
    ```
    npm run dev
    ```
    
    _(You should see a message saying "🚀 Lootr Backend is ALIVE!" on port 3000)._
    

### 2. The "Localhost" Mobile Warning ⚠️

Since you are testing on a mobile emulator or physical phone, you **cannot** just fetch `http://localhost:3000`. The mobile device thinks "localhost" is the phone itself, not the computer running the server!

- **If using an iOS Simulator:** You can usually use `http://localhost:3000` or `http://127.0.0.1:3000`.
    
- **If using an Android Emulator:** You MUST use `http://10.0.2.2:3000` (this is Android's special alias to reach your computer).
    
- **If using a Physical Device (via Expo Go):** You MUST use your computer's local Wi-Fi IP address (e.g., `http://192.168.1.5:3000`).
    

### 3. The API Contract

We currently have one main endpoint for you to hit when the user scans an object.

- **URL:** `http://<YOUR_IP>:3000/api/v1/game/generate`
    
- **Method:** `POST`
    
- **Headers:** `Content-Type: application/json`
    

**What you send to the backend (Request Body):**

JSON

```
{
  "objectLabel": "coffee mug"
}
```

**What the backend guarantees it will send back (Response Body):** Even if the AI completely crashes, the backend guarantees it will always return a JSON object exactly matching this structure so your game engine never breaks.

JSON

```
{
  "gameType": "balance", 
  "title": "Don't Spill!",
  "parameters": {
    "speed": 1.2,    
    "gravity": 1.5   
  }
}
```

_Note: `gameType` will ALWAYS be one of: `dodge`, `catch`, `balance`, `swipe`, `timing`, or `runner`. The numbers for `speed` and `gravity` will ALWAYS be a float between `0.1` and `3.0`._

### 4. Copy-Paste React Native Example

Here is a drop-in `fetch` function you can use in the mobile app to test the connection immediately:

JavaScript

```
const generateLootrGame = async (scannedItemName) => {
  try {
    // Replace with your correct IP depending on your emulator/device!
    const BACKEND_URL = 'http://10.0.2.2:3000/api/v1/game/generate'; 

    const response = await fetch(BACKEND_URL, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify({ objectLabel: scannedItemName }),
    });

    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }

    const gameConfig = await response.json();
    
    console.log("SUCCESS! Game generated:", gameConfig);
    console.log("Triggering mini-game mode:", gameConfig.gameType);
    
    // Pass this config to your game engine!
    return gameConfig; 

  } catch (error) {
    console.error("Failed to fetch game config:", error);
    // You can handle network failures here (e.g., show an offline error to the user)
  }
};

// Test it out!
// generateLootrGame("rusty sword");
```