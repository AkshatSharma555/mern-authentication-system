# MERN Authentication System 🔐

<br />
<div align="center">
  <img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/shield-halved.svg" alt="Logo" width="80" height="80">

  <h3 align="center">MERN Authentication System</h3>

  <p align="center">
    A production-grade authentication system built with the MERN stack and modern best practices.
    <br />
    <br />
    <a href="https://github.com/[YOUR-USERNAME]/[YOUR-REPO]/issues">Report Bug</a>
    ·
    <a href="https://github.com/[YOUR-USERNAME]/[YOUR-REPO]/issues">Request Feature</a>
  </p>
</div>

<div align="center">

[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

</div>

> This system includes JWT-based authentication, secure password hashing, email verification, password reset, and protected API routes.

---

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#-features">Features</a></li>
    <li><a href="#-tech-stack">Tech Stack</a></li>
    <li><a href="#-folder-structure">Folder Structure</a></li>
    <li>
      <a href="#-getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#backend-setup-server">Backend Setup</a></li>
        <li><a href="#frontend-setup-client">Frontend Setup</a></li>
      </ul>
    </li>
    <li><a href="#-api-endpoints">API Endpoints</a></li>
    <li><a href="#-roadmap">Roadmap</a></li>
    <li><a href="#-author">Author</a></li>
  </ol>
</details>

---


## ✨ Features

-   🔑 User Registration with **Email Verification**
-   🔒 Secure Login using **JWT (JSON Web Token)**
-   🔐 Password Hashing with **bcrypt**
-   📧 Forgot Password & Reset Password (via Email)
-   🛡️ Middleware-protected API routes
-   🧩 Modular **MVC architecture**
-   ⚛️ Context-based state management in React
-   🎨 **TailwindCSS + Vite** frontend for a modern UI
-   ⚙️ Environment-based configuration using `.env`

---

## 🛠 Tech Stack

| Frontend                                       | Backend                                   | Database                                | Authentication                                     |
| ---------------------------------------------- | ----------------------------------------- | --------------------------------------- | -------------------------------------------------- |
| ![React][React.js]                             | ![Node.js][Node.js]                       | ![MongoDB][MongoDB]                     | ![JWT](https://img.shields.io/badge/JWT-black?logo=jsonwebtokens) |
| ![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white) | ![Express.js][Express.js]                 | ![Mongoose](https://img.shields.io/badge/Mongoose-880000?logo=mongoose&logoColor=white) | ![Nodemailer](https://img.shields.io/badge/Nodemailer-22B573?logo=minutemailer&logoColor=white) |
| ![TailwindCSS][TailwindCSS]                    |                                           |                                         | ![Bcrypt](https://img.shields.io/badge/Bcrypt-4A90E2?logo=shield&logoColor=white) |


---

## 📂 Folder Structure

A brief look at the project's directory structure.

MERN-AUTHENTICATION/
│
├── client/             # React Frontend (Vite + TailwindCSS)
│   ├── src/
│   │   ├── assets/
│   │   ├── components/     # Reusable UI Components
│   │   ├── context/        # React Context API for state management
│   │   ├── pages/          # Login, Register, Reset, etc.
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── ...
│
├── server/             # Node.js Backend (Express + MongoDB)
│   ├── config/         # DB connection, Email templates
│   ├── controllers/    # Business logic (Auth, User)
│   ├── middleware/     # Auth middleware (JWT verification)
│   ├── models/         # Mongoose User model
│   ├── routes/         # API routes
│   ├── server.js       # Application entry point
│   └── .env.example    # Environment variables template
│
├── .gitignore
├── package.json
└── README.md


---

## ⚙️ Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

You need to have the following software installed on your machine:
-   [Node.js](https://nodejs.org/) (v18.x or higher)
-   [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
-   A free [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account
-   A free [Brevo (formerly Sendinblue)](https://www.brevo.com/) account for SMTP services

### 1. Clone the Repository

```bash
git clone [https://github.com/](https://github.com/)[YOUR-USERNAME]/mern-authentication-system.git
cd mern-authentication-system
2. Backend Setup (server)
Navigate to the server directory and install dependencies.

Bash

cd server
npm install
Create a .env file in the server folder and add the following configuration.

Code snippet

# MongoDB Connection
MONGODB_URI='mongodb+srv://<username>:<password>@cluster0.gwhfllp.mongodb.net'

# JWT
JWT_SECRET='your_jwt_secret_here'

# Server Configuration
NODE_ENV='development'
PORT=4000

# Brevo (Sendinblue) SMTP Credentials
SMTP_USER="your_smtp_username"
SMTP_PASS="your_smtp_password"
SENDER_EMAIL="your_email@example.com"
How to Generate .env Values:
MONGODB_URI:

Go to MongoDB Atlas and create a free cluster.

Navigate to Database → Connect → Connect your application.

Copy the connection string and replace <username> and <password> with your database credentials.

JWT_SECRET:

Generate a random, secure string using a tool like randomkeygen.com.

SMTP_USER / SMTP_PASS:

Go to Brevo and create a free account.

Navigate to SMTP & API → SMTP → Generate New Credentials.

Copy your credentials into the .env file.

SENDER_EMAIL:

The email you want to send verification/reset links from (must be a verified sender with Brevo).

Now, start the backend server:

Bash

npm start
✅ Your server should now be running on http://localhost:4000

3. Frontend Setup (client)
Open a new terminal, navigate to the client directory, and install dependencies.

Bash

# From the root directory
cd client
npm install
Now, start the frontend development server:

Bash

npm run dev
✅ Your frontend application should now be running on http://localhost:5173

📋 API Endpoints
The following are the available API routes:

Method	Endpoint	Description	Access
POST	/api/auth/register	Register a new user	Public
POST	/api/auth/login	Login user & return JWT	Public
GET	/api/auth/verify/:id	Verify user's email address	Public
POST	/api/auth/reset	Request a password reset link	Public
POST	/api/auth/new-pass	Set a new password with a token	Public
GET	/api/user/profile	Get logged-in user's profile	Protected


🚀 Roadmap
[ ] Google/GitHub OAuth login

[ ] Refresh tokens for long-lived sessions

[ ] Role-based authentication (Admin/User)

[ ] Unit & Integration Tests (Jest/Mocha)

See the open issues for a full list of proposed features and known issues.

👨‍💻 Author
Developed with ✨ by Akshat Sharma

GitHub: https://github.com/AkshatSharma555

LinkedIn: www.linkedin.com/in/akshat-sharma-6664422b3

This is a prototype project for learning & demonstration purposes.
