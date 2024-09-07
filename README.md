**Forever Twilight in Forks Festival App**

A web app for the Forever Twilight in Forks festival in Forks, Washington, providing users with event schedules, personalized itineraries, interactive maps, and festival store access. The app will eventually offer social media features for festival-goers to share their experiences.  Once this app is completed, it will be refactored to be a mobile app built with React Native.

**Table of Contents**

Features
Tech Stack
Project Structure
Getting Started
Prerequisites
Installation
Running the App
API Documentation
Authentication
Contributing

User Authentication: Log in with email (JWT) or Google OAuth.
Event Calendar: Browse all festival events and times.
Custom Itinerary: Build and manage a personal schedule of festival events.
Interactive Map: Explore festival venues with a live, interactive map.
Festival Store: Access and purchase festival merchandise.
Push Notifications: Get live updates and alerts about the festival.
Social Media (Planned): Share posts, photos, and comments with other attendees.

**Tech Stack**

Frontend: Vite, React, TailwindCSS
Backend: Node.js, Express
Authentication: JWT for email login, Google OAuth for social login
Database: To be decided - either MongoDB or Firebase Realtime Database
Push Notifications: (To be added - likely using Firebase)
Social Media Component: (To be developed)
Project Structure

bash
Copy code
/forever-twilight-app
  /client                 # Vite + React frontend
    /src
      /components         # Reusable UI components
      /pages              # Application pages/routes
      /services           # API calls and business logic
      /styles             # TailwindCSS custom styles
      /assets             # Images, icons, etc.
    vite.config.js        # Vite configuration
    package.json          # Frontend dependencies
  /backend                # Node.js + Express backend
    /controllers          # Backend logic for handling API requests
    /routes               # API routes
    /models               # Database models
    /middleware           # JWT and authentication middleware
    /services             # External services or helper functions
    server.js             # Entry point for the backend server
    package.json          # Backend dependencies
  .env                    # Environment variables (JWT secrets, OAuth keys, etc.)
  README.md               # Project documentation
Getting Started

**Prerequisites**
Before you start, make sure you have the following installed:

Node.js (version 14+)
npm or yarn
MongoDB (if using a MongoDB database)


**Installation**
**Clone the repository:**
git clone https://github.com/ashleymckellar/FTF-app.git

**Install dependencies for the backend:**
npm install

**Install dependencies for the frontend:**
cd client
npm install

**Set up environment variables:**
Create a .env file in the root directory with the following content (and make sure your .env is added to your gitignore in the root directory):
PORT=8201
SECRET=your_jwt_secret
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
MONGO_URI=your_mongo_db_connection_string

**Running the App**
**Start the backend server:**
nodemon server.js

**Start the frontend:**
cd client
npm run dev
Open your browser and navigate to http://localhost:5173 to view the app (Vite’s default dev server port).

**API Documentation**

**Authentication Endpoints**
POST /api/auth/login: User login with email and password (JWT).
POST /api/auth/google: Login via Google OAuth.
Event Endpoints
GET /api/events: Retrieve a list of all festival events.
POST /api/itinerary: Add an event to the user's custom itinerary.
GET /api/itinerary: Retrieve the user's custom itinerary.
Push Notifications
(To be added)
Authentication

The app uses JWT for email-based authentication and Google OAuth for Google-based login.

JWT Authentication: After logging in with email and password, a JSON Web Token (JWT) is issued. This token must be sent with subsequent API requests in the Authorization header.
Google OAuth: Users can authenticate via their Google accounts using OAuth 2.0, enabling a secure sign-in flow.
Contributing

**Contributions are welcome! To contribute:**

Fork this repository.
Create a new branch for your feature:
bash
Copy code
git checkout -b feature/your-feature
Make your changes and commit:
bash
Copy code
git commit -m "Add your feature"
Push your branch:
bash
Copy code
git push origin feature/your-feature
Open a pull request.
License

This project is licensed under the MIT License. See the LICENSE file for details.

Contact

For questions or issues, feel free to reach out at ashley.l.mckellar@gmail.com.
