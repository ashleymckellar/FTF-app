Forever Twilight in Forks Festival App
======================================

A web app for the **Forever Twilight in Forks** festival in Forks, Washington, providing users with event schedules, personalized itineraries, interactive maps, and festival store access. The app will eventually offer social media features for festival-goers to share their experiences and will later be built as a React Native mobile app.

Table of Contents
-----------------

-   [Features](#features)
-   [Tech Stack](#tech-stack)
-   [Project Structure](#project-structure)
-   [Getting Started](#getting-started)
    -   [Prerequisites](#prerequisites)
    -   [Installation](#installation)
    -   [Running the App](#running-the-app)
-   [API Documentation](#api-documentation)
-   [Authentication](#authentication)
-   [Contributing](#contributing)

* * * * *

Features
--------

-   **User Authentication**: Log in with email (JWT) or Google OAuth.
-   **Event Calendar**: Browse all festival events and times.
-   **Custom Itinerary**: Build and manage a personal schedule of festival events.
-   **Interactive Map**: Explore festival venues with a live, interactive map.
-   **Festival Store**: Access and purchase festival merchandise.
-   **Push Notifications**: Get live updates and alerts about the festival.
-   **Social Media (Planned)**: Share posts, photos, and comments with other attendees.

Tech Stack
----------

-   **Frontend**: Vite, React, TailwindCSS
-   **Backend**: Node.js, Express
-   **Authentication**: JWT for email login, Google OAuth for social login
-   **Database**: (To be decided, e.g., MongoDB, PostgreSQL)
-   **Push Notifications**: (To be added)
-   **Social Media Component**: (To be developed)

* * * * *

Project Structure
-----------------



`/ftf-app`                # Root directory, also serves as backend directory

    `/controllers`          # Backend logic for handling API requests

    `/routes`               # API routes

    `/models`               # Database models

    `/middleware`           # JWT and authentication middleware

    `/services`             # External services or helper functions

    `server.js`             # Entry point for the backend server

    `package.json`          # Backend dependencies

  `.env`                  # Environment variables (JWT secrets, OAuth keys, etc.)

 ` README.md`               # Project documentation

   `/client`                 # Vite + React frontend

    `/src`

      `/components`         # Reusable UI components

      `/pages`              # Application pages/routes

      `/services`           # API calls and business logic

      `/styles`             # TailwindCSS custom styles

      `/assets`             # Images, icons, etc.

    `vite.config.js`        # Vite configuration

    `package.json`          # Frontend dependencies

* * * * *

Getting Started
---------------

### Prerequisites

Before you start, make sure you have the following installed:

-   **Node.js** (version 14+)
-   **npm** or **yarn**
-   **MongoDB** (if using a MongoDB database)

### Installation

1.  **Clone the repository**:

    `git clone https://github.com/ashleymckellar/FTF-app.git
    cd ftf-app`

2.  **Install dependencies for the backend**:

    `npm install`

3.  **Install dependencies for the frontend**:

  `cd client`

  `npm install`

4. **Set up environment variables**:

    -   Create a `.env` file in the root directory with the following content:

      

        `PORT=8201`
        
        `SECRET=your_jwt_secret`
        
        `GOOGLE_CLIENT_ID=your_google_client_id`
        
        `GOOGLE_CLIENT_SECRET=your_google_client_secret`
        
        `MONGO_URI=your_mongo_db_connection_string`

### Running the App

1.  **Start the backend server**:

    `nodemon server.js`

2.  **Start the frontend**:

    `cd client`
    
    `npm run dev`

4.  **Open your browser** and navigate to `http://localhost:5173` to view the app (Vite's default dev server port).

* * * * *

API Documentation
-----------------

### Authentication Endpoints

-   **POST /api/auth/login**: User login with email and password (JWT).
-   **POST /api/auth/google**: Login via Google OAuth.

### Event Endpoints

-   **GET /api/events**: Retrieve a list of all festival events.
-   **POST /api/itinerary**: Add an event to the user's custom itinerary.
-   **GET /api/itinerary**: Retrieve the user's custom itinerary.

### Push Notifications

-   (To be added)

* * * * *

Authentication
--------------

The app uses **JWT** for email-based authentication and **Google OAuth** for Google-based login.

-   **JWT Authentication**: After logging in with email and password, a JSON Web Token (JWT) is issued. This token must be sent with subsequent API requests in the `Authorization` header.
-   **Google OAuth**: Users can authenticate via their Google accounts using OAuth 2.0, enabling a secure sign-in flow.

* * * * *

Contributing
------------

Contributions are welcome! To contribute:

1.  Fork this repository.
2.  Create a new branch for your feature

    `git checkout -b feature/your-feature`

3.  Make your changes and commit:

    `git commit -m "Add your feature"`

4.  Push your branch:

    `git push origin feature/your-feature`

5.  Open a pull request.

Contact
------------

For questions or issues, feel free to reach out at ashley.l.mckellar@gmail.com.
