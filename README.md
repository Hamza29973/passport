# Passport Authentication Example (Node.js + Express)

A professional example of user authentication in a Node.js and Express application using **Passport.js**, supporting:

- Local username/password authentication
- Google OAuth 2.0 login
- Facebook login

Users are stored in an **in-memory database** (for demonstration purposes).

---

## 🚀 Features

- Register a user using local credentials
- Login with local credentials
- Login with Google
- Login with Facebook
- Session-based authentication with `express-session`
- Protected dashboard route accessible only to authenticated users
- Logout functionality

---

## 🛠 Technologies Used

- Node.js
- Express
- Passport.js
- bcryptjs (for password hashing)
- express-session (for session management)
- cookie-parser
- dotenv

---

## 📥 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Hamza29973/passport
cd passport
2. Install dependencies
npm install
3. Configure environment variables
Create or edit the .env file in the root directory:

PORT=3000
SESSION_SECRET=superSecretKey123

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret

FACEBOOK_CLIENT_ID=your_facebook_app_id
FACEBOOK_CLIENT_SECRET=your_facebook_client_secret
🔹 Replace your_google_client_id etc., with your actual credentials.
🔹 If you already have a .env file, just update the keys you need (e.g., GOOGLE_CLIENT_ID).

4. Run the server
npm start
The server will run on:

http://localhost:3000
🔑 API Endpoints
Local Authentication
Method	Route	Description
POST	/register	Register a new user
POST	/login	Login with username & password
POST	/logout	Logout user
Request example (Register/Login)

{
  "username": "yourusername",
  "password": "yourpassword"
}
OAuth Login
Google
GET /auth/google – Redirects to Google login

GET /auth/google/callback – Google OAuth callback

Facebook
GET /auth/facebook – Redirects to Facebook login

GET /auth/facebook/callback – Facebook OAuth callback

Protected Route
GET /dashboard – Accessible only for authenticated users
Displays user information and provides a logout button.
