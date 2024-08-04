
# My Auth App

This project is a simple authentication system with signup, login, and forgot password functionality, built with React for the frontend and MongoDB Atlas for the backend.

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Setup and Configuration](#setup-and-configuration)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [Environment Variables](#environment-variables)

## Features

- User signup
- User login
- Password reset functionality
- Protected dashboard

## Project Structure

```plaintext
my-auth-app/
├── backend/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   ├── authController.js
│   ├── models/
│   │   └── User.js
│   ├── routes/
│   │   └── authRoutes.js
│   ├── server.js
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Dashboard.js
│   │   │   ├── ForgotPassword.js
│   │   │   ├── Login.js
│   │   │   ├── Signup.js
│   │   ├── App.js
│   │   ├── index.js
│   ├── package.json
├── package.json
├── .env
```

## Setup and Configuration

### 1. MongoDB Atlas Setup

1. **Create a MongoDB Atlas Account**:
   - Go to the [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) website and sign up for a free account.

2. **Create a New Cluster**:
   - Follow the instructions to create a new cluster. Choose the free tier if you're just starting out.

3. **Whitelist Your IP Address**:
   - In the Network Access section, add your IP address to the whitelist so you can connect to the cluster.

4. **Create a Database User**:
   - In the Database Access section, create a new database user with a username and password.

5. **Get the Connection String**:
   - In the Clusters view, click on the "Connect" button for your cluster. Follow the prompts to get your connection string. It will look something like this:

     ```
     mongodb+srv://<username>:<password>@cluster0.mongodb.net/myFirstDatabase?retryWrites=true&w=majority
     ```

### 2. Configure Environment Variables

Create a `.env` file in the root of your `backend` directory to store your MongoDB connection URI securely.

```plaintext
MONGO_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/myFirstDatabase?retryWrites=true&w=majority
JWT_SECRET=your_jwt_secret
```

Replace `<username>`, `<password>`, and `myFirstDatabase` with your actual MongoDB Atlas username, password, and database name.

## Installation

### Backend

1. Navigate to the `backend` directory:

```bash
cd backend
```

2. Install the backend dependencies:

```bash
npm install
```

### Frontend

1. Navigate to the `frontend` directory:

```bash
cd frontend
```

2. Install the frontend dependencies:

```bash
npm install
```

## Running the Application

### Backend

1. Ensure you are in the `backend` directory.
2. Start the backend server:

```bash
nodemon server.js
```

### Frontend

1. Ensure you are in the `frontend` directory.
2. Start the frontend development server:

```bash
npm start
```

## Environment Variables

- `MONGO_URI`: MongoDB connection URI.
- `JWT_SECRET`: Secret key for JWT token generation.

## Code Overview

### Backend

- `config/db.js`: MongoDB connection configuration.
- `controllers/authController.js`: Authentication logic (signup, login, forgot password).
- `models/User.js`: Mongoose User model with password hashing.
- `routes/authRoutes.js`: Authentication routes.
- `server.js`: Express server setup.

### Frontend

- `src/components/Signup.js`: Signup form component.
- `src/components/Login.js`: Login form component.
- `src/components/ForgotPassword.js`: Forgot password form component.
- `src/components/Dashboard.js`: Dashboard component.
- `src/App.js`: React Router setup.
- `src/index.js`: React entry point.

## License

This project is licensed under the MIT License.
