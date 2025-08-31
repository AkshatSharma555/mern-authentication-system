# MERN Authentication System 🔒

A production-grade authentication system built with the **MERN stack** and modern best practices.

This system includes:
- JWT-based authentication  
- Secure password hashing  
- Email verification  
- Password reset  
- Protected API routes  

---

## 🚀 Tech Stack

| Frontend              | Backend                 | Database                     | Authentication         |
|-----------------------|-------------------------|------------------------------|-------------------------|
| React.js (Vite)       | Node.js, Express.js     | MongoDB (Mongoose)           | JWT, Bcrypt             |
| TailwindCSS           | Nodemailer              |                              |                         |

---

## 📂 Folder Structure

```
AUTHENTICATION/
│
├── client/                  # React Frontend (Vite + TailwindCSS)
│   └── src/
│       ├── assets/
│       ├── components/      # Reusable UI Components
│       ├── context/         # React Context API for state management
│       ├── pages/           # Login, Register, Reset, etc.
│       ├── App.jsx
│       └── main.jsx
│
├── server/                  # Node.js Backend (Express + MongoDB)
│   ├── config/              # DB connection, Email templates
│   ├── controllers/         # Business logic (Auth, User)
│   ├── middleware/          # Auth middleware (JWT verification)
│   ├── models/              # Mongoose User model
│   ├── routes/              # API routes
│   └── server.js            # Application entry point
│
├── .env.example             # Environment variables template
├── .gitignore
├── package.json
└── README.md
```

## 📌 Features

- User Registration & Login  
- JWT-based Authentication & Authorization  
- Secure Password Hashing with Bcrypt  
- Email Verification & Password Reset via Nodemailer  
- Protected API Routes  
- React Context API for Global State Management  
- TailwindCSS for Modern UI  

---

## 🛠️ Installation & Setup

1. Clone the repository:
 ```
   git clone https://github.com/AkshatSharma555/mern-authentication-system.git
 ```
Navigate into the project directory:
 ```
 cd authentication
 ```
Install dependencies for both frontend and backend:

For frontend
 ```
cd client && npm install
 ```
For backend
 ```
cd server && npm install
 ```
## ⚙️ Environment Setup

Create a `.env` file inside the **server/** folder and add the following configuration:

```bash
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
```
### 🔑 How to Generate `.env` Values

#### 1. `MONGODB_URI`
- Go to [MongoDB Atlas](https://www.mongodb.com/atlas/database) and **create a free cluster**.
- Navigate to:  
  **Database → Connect → Connect your application**  
- Copy the connection string and replace `<username>` and `<password>` with your database credentials.

---

#### 2. `JWT_SECRET`
- Generate a random, secure string using [randomkeygen.com](https://randomkeygen.com) or any password generator.  
- Example: `hsd82h3h2g3jsdf8723@##1`

---

#### 3. `SMTP_USER` / `SMTP_PASS`
- Go to [Brevo (Sendinblue)](https://www.brevo.com/) and **create a free account**.  
- Navigate to:  
  **SMTP & API → SMTP → Generate New Credentials**  
- Copy your **SMTP User** and **SMTP Password** into the `.env` file.

---

#### 4. `SENDER_EMAIL`
- Enter the email address you want to send **verification / reset links** from.  
- ⚠️ Must be a **verified sender email** in Brevo.

---


Start the development servers:

Frontend:

 ```
cd client
npm run dev
 ```
Backend:

 ```
cd server
npm run dev
 ```

Developed with ❤️ by Akshat Sharma

GitHub: https://github.com/AkshatSharma555

LinkedIn: www.linkedin.com/in/akshat-sharma-6664422b3
