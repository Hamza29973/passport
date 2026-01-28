# Passport Authentication Example

This is a Node.js and Express application demonstrating authentication using **Passport.js** with:

- Local username/password authentication
- Google OAuth 2.0 login
- Facebook login

Users are stored in a temporary in-memory array (for demo purposes).

---

## Features

- Register and login with local credentials
- Login with Google or Facebook accounts
- Protected dashboard route accessible only to authenticated users
- Logout functionality

---

## Technologies Used

- Node.js
- Express
- Passport.js
- bcryptjs (for password hashing)
- express-session (for session management)
- cookie-parser
- dotenv

---

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/Hamza29973/passport
cd passport
2. Install dependencies
npm install
3. Create .env file
Create a .env file in the root directory:

PORT=3000
SESSION_SECRET=superSecretKey123

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret

FACEBOOK_CLIENT_ID=your_facebook_app_id
FACEBOOK_CLIENT_SECRET=your_facebook_client_secret
Replace the placeholders with your actual credentials.

4. Run the server
npm start
Server will run on: http://localhost:3000

API Endpoints
Local Auth
POST /register – Register a new user
Body: { "username": "yourusername", "password": "yourpassword" }

POST /login – Login with local credentials
Body: { "username": "yourusername", "password": "yourpassword" }

POST /logout – Logout user

OAuth Login
GET /auth/google – Redirects to Google login

GET /auth/google/callback – Google OAuth callback

GET /auth/facebook – Redirects to Facebook login

GET /auth/facebook/callback – Facebook OAuth callback

Protected Route
GET /dashboard – Accessible only for authenticated users

Notes
This app uses an in-memory database (users array). All data is lost on server restart.

For production, replace with a real database (e.g., MongoDB, PostgreSQL).

Passwords are hashed using bcryptjs.



Do you want me to do that?
