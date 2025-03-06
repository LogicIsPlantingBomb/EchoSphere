# EchoSphere - Backend for Anonymous Discussion Platform

## Project Overview
This is the backend for an anonymous discussion platform built using Node.js and Express. The platform allows users to discuss hot topics anonymously or with their identity, with features like user authentication, post creation and deletion, and more.

## File Structure
```
.
├── app.js                        # Initializes app and middleware
├── controllers
│   └── user.controller.js         # Handles user-related logic (login, register, etc.)
├── db
│   └── db.js                      # Database connection setup
├── middlewares
│   └── auth.middleware.js         # JWT authentication middleware
├── models
│   ├── blacklistToken.model.js    # Blacklisted tokens for logout handling
│   └── userModel.js               # User schema (email, password, isAnonymous, etc.)
├── package.json                   # Project dependencies
├── package-lock.json              # Dependency lockfile
├── README.md                      # Project documentation
├── routes
│   └── user.routes.js             # Routes for user actions (signup, login, profile)
├── server.js                      # Main entry point — starts Express server
└── services
    └── userServices.js            # Handles business logic (interacting with DB, etc.)
```

## Features
- **User Authentication:** Sign up, log in, and log out with JWT tokens.
- **Anonymity Option:** Future feature — users can choose whether to be anonymous.
- **CRUD Operations for Posts:** (To be added later)
- **Real-time Interactions:** Planned with Socket.io for live updates.

## Installation
1. Clone the repository:
   ```bash
   git clone <repo-url>
   ```
2. Install dependencies:
   ```bash
   cd backend
   npm install
   ```
3. Set up environment variables:
   Create a `.env` file in the root and add:
   ```plaintext
   PORT=5000
   MONGO_URI=your_mongo_db_uri
   JWT_SECRET=your_jwt_secret
   ```
4. Run the development server:
   ```bash
   npm run dev
   ```

## API Endpoints
### User Routes
- **POST** `/api/users/register` — Register a new user
- **POST** `/api/users/login` — Log in and receive a JWT token
- **GET** `/api/users/profile` — Get user profile (protected route)
- **POST** `/api/users/logout` — Log out by blacklisting JWT token

## Tech Stack
- **Node.js**
- **Express.js**
- **MongoDB** (for database)
- **JWT** (for authentication)

## To-Do
- [ ] Add post creation and deletion features
- [ ] Implement real-time voting and betting system with Socket.io
- [ ] Integrate user anonymity toggle

## Contributing
Feel free to open issues or submit pull requests! We’re open to suggestions and improvements.

---

Let me know if you'd like any edits, especially for upcoming features like real-time updates or bets! 🚀

