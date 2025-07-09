# internshipprojectbackend
# 🔐 JWT Authentication API

A simple and secure backend API built with **Node.js**, **Express**, and **MongoDB**, supporting user **registration**, **login**, and **protected routes** using **JSON Web Tokens (JWT)**.

---

## 🚀 Features

- ✅ User Registration (`/api/auth/register`)
- ✅ User Login with JWT (`/api/auth/login`)
- ✅ Protected route for authenticated users (`/api/auth/me`)
- ✅ Password hashing with bcrypt
- ✅ Token-based authentication
- ✅ MongoDB integration with Mongoose
- ✅ Deployed on Vercel (optional)

---

## 🛠 Tech Stack

- **Backend:** Node.js, Express
- **Database:** MongoDB (via Mongoose)
- **Authentication:** JWT, bcrypt
- **Deployment:** Vercel 
- **Environment Management:** dotenv

---

## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/harshvardhan119/internshipprojectbackend.git

2. Install Dependencies

npm install
3. Setup Environment Variables
Create a .env file in the root:

env
Copy
Edit
PORT=5000
MONGO_URI=mongodb://localhost:27017/jwt-auth
JWT_SECRET=your_secret_key_here
⚠️ Don’t forget to add .env to .gitignore!

▶️ Running the Server

node server.js
The API will be available at:
http://localhost:5000

🔗 API Endpoints
📌 Register User
POST /api/auth/register

json
Copy
Edit
{
  "email": "test@example.com",
  "password": "password123"
}
📌 Login User
POST /api/auth/login

json
Copy
Edit
{
  "email": "test@example.com",
  "password": "password123"
}
Response:

json
Copy
Edit
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6..."
}
📌 Get Current User (Protected)
GET /api/auth/me

Headers:

makefile
Copy
Edit
Authorization: Bearer <your_jwt_token>
🌐 Deployment on Vercel 
my vercel backend link - https://internshipprojectbackend.vercel.app
Add vercel.json in the root:
json
Copy
Edit
{
  "version": 2,
  "builds": [
    { "src": "server.js", "use": "@vercel/node" }
  ],
  "routes": [
    { "src": "/(.*)", "dest": "/server.js" }
  ]
}
Environment Variables (on Vercel dashboard):
MONGO_URI

JWT_SECRET

📁 Project Structure
pgsql
Copy
Edit
jwt-auth-backend/
├── models/
│   └── User.js
├── routes/
│   └── auth.js
├── server.js
├── .env
├── .gitignore
├── package.json
└── vercel.json
✅ Postman Testing
Register a new user.

Log in to receive a JWT token.

Use the token to access the /api/auth/me route.

