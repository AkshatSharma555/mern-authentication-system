# MERN Authentication System 🔐

<br />
<div align="center">
  <img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/shield-halved.svg" alt="Logo" width="80" height="80">

  <h3 align="center">MERN Authentication System</h3>

  <p align="center">
    A production-grade authentication system built with the MERN stack and modern best practices.
    <br />
    <br />
    <a href="https://github.com/AkshatSharma555/mern-authentication-system/issues">Report Bug</a>
    ·
    <a href="https://github.com/AkshatSharma555/mern-authentication-system/issues">Request Feature</a>
  </p>
</div>


> This system includes JWT-based authentication, secure password hashing, email verification, password reset, and protected API routes.

---

<details>
  <summary>📑 Table of Contents</summary>
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

- 🔑 User Registration with **Email Verification**
- 🔒 Secure Login using **JWT (JSON Web Token)**
- 🔐 Password Hashing with **bcrypt**
- 📧 Forgot Password & Reset Password (via Email)
- 🛡️ Middleware-protected API routes
- 🧩 Modular **MVC architecture**
- ⚛️ Context-based state management in React
- 🎨 **TailwindCSS + Vite** frontend for a modern UI
- ⚙️ Environment-based configuration using `.env`

---

## 🛠 Tech Stack

| Frontend                                       | Backend                                   | Database                                | Authentication                                     |
| ---------------------------------------------- | ----------------------------------------- | --------------------------------------- | -------------------------------------------------- |
| ![React][React.js]                             | ![Node.js][Node.js]                       | ![MongoDB][MongoDB]                     | ![JWT](https://img.shields.io/badge/JWT-black?logo=jsonwebtokens) |
| ![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white) | ![Express.js][Express.js]                 | ![Mongoose](https://img.shields.io/badge/Mongoose-880000?logo=mongoose&logoColor=white) | ![Nodemailer](https://img.shields.io/badge/Nodemailer-22B573?logo=minutemailer&logoColor=white) |
| ![TailwindCSS][TailwindCSS]                    |                                           |                                         | ![Bcrypt](https://img.shields.io/badge/Bcrypt-4A90E2?logo=shield&logoColor=white) |

---

## 📂 Folder Structure

MERN-AUTHENTICATION/
│
├── client/ # React Frontend (Vite + TailwindCSS)
│ ├── src/
│ │ ├── assets/
│ │ ├── components/ # Reusable UI Components
│ │ ├── context/ # React Context API for state management
│ │ ├── pages/ # Login, Register, Reset, etc.
│ │ ├── App.jsx
│ │ └── main.jsx
│ └── ...
│
├── server/ # Node.js Backend (Express + MongoDB)
│ ├── config/ # DB connection, Email templates
│ ├── controllers/ # Business logic (Auth, User)
│ ├── middleware/ # Auth middleware (JWT verification)
│ ├── models/ # Mongoose User model
│ ├── routes/ # API routes
│ ├── server.js # Application entry point
│ └── .env.example # Environment variables template
│
├── .gitignore
├── package.json
└── README.md


## ⚙️ Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

- [Node.js](https://nodejs.org/) (v18.x or higher)  
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)  
- Free [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account  
- Free [Brevo (Sendinblue)](https://www.brevo.com/) account for SMTP services  

---

### '
1. Clone the Repository

git clone https://github.com/AkshatSharma555/mern-authentication-system.git
cd mern-authentication-system

2. Backend Setup (server)

cd server
npm install
Create a .env file inside the server folder and add the following:

env

# MongoDB Connection
MONGODB_URI='mongodb+srv://<username>:<password>@cluster0.gwhfllp.mongodb.net'

# JWT Secret
JWT_SECRET='your_jwt_secret_here'

# Server Config
NODE_ENV='development'
PORT=4000

# SMTP (Brevo)
SMTP_USER="your_smtp_username"
SMTP_PASS="your_smtp_password"
SENDER_EMAIL="your_email@example.com"

🔑 How to Generate Values:

MONGODB_URI → Create cluster in MongoDB Atlas → Database → Connect → Copy connection string.

JWT_SECRET → Generate secure random string from randomkeygen.com.

SMTP_USER / SMTP_PASS → Login to Brevo → SMTP & API → Generate credentials.

SENDER_EMAIL → Your verified sender email in Brevo.

Start backend:

npm run server
✅ Server running at: http://localhost:4000

3. Frontend Setup (client)

cd client
npm install
npm run dev
✅ Frontend running at: http://localhost:5173

📋 API Endpoints
Method	Endpoint	Description	Access
POST	/api/auth/register	Register a new user	Public
POST	/api/auth/login	Login user & return JWT	Public
GET	/api/auth/verify/:id	Verify user’s email	Public
POST	/api/auth/reset	Request password reset link	Public
POST	/api/auth/new-pass	Set a new password with token	Public
GET	/api/user/profile	Get logged-in user’s profile	Protected

🚀 Roadmap
 Google/GitHub OAuth login

 Refresh tokens for long-lived sessions

 Role-based authentication (Admin/User)

 Unit & Integration Tests (Jest/Mocha)

See the open issues for more.

👨‍💻 Author
Developed with ❤️ by Akshat Sharma

GitHub: @AkshatSharma555

LinkedIn: www.linkedin.com/in/akshat-sharma-6664422b3
