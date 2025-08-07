# MERN Real-Time Chat Application

This is a full-stack real-time chat application built using the MERN stack (MongoDB, Express.js, React.js, Node.js). It features secure user authentication with JWT and bcrypt, real-time one-to-one messaging via Socket.io, and a responsive UI styled with Tailwind CSS and DaisyUI. The backend handles RESTful APIs and WebSocket events, while the frontend delivers dynamic rendering with Vite. Messages and user data are efficiently managed in MongoDB. The application supports online status indicators and smooth user experience across devices. It is fully deployed on Render with environment variable support and a production-ready build process.

## Screenshots

<img align="center" src="https://github.com/BadshahYadav/MERN-Chat-App/blob/main/frontend/public/Screenshot%202025-08-07%20105443.png" width="1200" >
<img align="center" src="https://github.com/BadshahYadav/MERN-Chat-App/blob/main/frontend/public/Screenshot%202025-08-07%20105547.png" width="1200" >


## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Used](#technologies-used)
- [File Structure](#file-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Project](#running-the-project)
- [Environment Variables](#environment-variables)
- [Deployment](#deployment)
- [Contact](#contact)
- [License](#license)

## Overview

This project is a real-time chat application built using the MERN stack (MongoDB, Express.js, React.js, Node.js). It enables seamless one-to-one messaging with secure authentication, efficient message storage, and dynamic frontend rendering. The application leverages WebSockets via Socket.io to provide instant communication between users.

Key functionalities include user registration and login with hashed passwords, JWT-based authentication, real-time chat messaging with automatic updates, online/offline status indicators, and responsive UI design using Tailwind CSS and DaisyUI.

The backend is structured with a modular Express API, connecting to a MongoDB database hosted on the cloud. The app is deployed on Render for full-stack deployment, with environment variable support and production-ready build optimization using Vite.

The app focuses on delivering a smooth, responsive, and user-friendly experience, making learning and self-assessment both fun and engaging.
You can view the live portfolio at: [LIVE PREVIEW](https://mern-chat-app-yyo6.onrender.com)

## Features

**Real-Time Chat**: Instantly send and receive messages using Socket.io for seamless real-time communication.
**Authentication**: Secure user signup, login, and JWT-based authentication with protected routes.
**Profile Management**: Users can update their profile information and upload profile pictures (with image upload to Cloudinary).
**Responsive Design**: Fully responsive UI built with React, Tailwind CSS, and daisyUI—works great on desktop and mobile.
**Project Structure**: Clean, modular codebase with separate backend (Express, MongoDB) and frontend (React) folders.
**State Management**: Uses Zustand and React hooks for efficient and scalable state management.
**File Uploads**: Supports image uploads in chat and profile, with file size validation.
**Error Handling**: User-friendly error messages and robust backend validation.
**Easy Deployment**: Simple deployment process for both frontend and backend (supports platforms like Render).
**Environment Variables**: Secure configuration using .env files for sensitive data.
**Modern UI**: Clean, modern interface with smooth navigation and interactive components.

## Tech Stack

- **Frontend**: React.js, Tailwind CSS, DaisyUI, Vite.
- **Backend**: Node.js, Express.js.
- **Database**: MongoDB (Mongoose ODM)
- **Authentication**: JWT, bcrypt.
- **Real-time Communication**: Socket.io. 
- **Deployment**: Render.
- **State Mangement** : React Hooks (useState, useEffect).
- **Dev Tools**: dotenv, concurrently, ESLint.

## File Structure

Here's an overview of the project's file structure:

```plaintext
MERN-Chat-App/
├── README.md
├── backend/
│   ├── package.json
│   ├── .env
│   └── src/
│       ├── index.js
│       ├── controllers/
│       │   ├── auth.controller.js
│       │   └── message.controller.js
│       ├── lib/
│       │   ├── cloudinary.js
│       │   ├── db.js
│       │   └── utils.js
│       ├── middleware/
│       │   └── auth.middleware.js
│       ├── models/
│       │   ├── message.model.js
│       │   └── user.model.js
│       └── routes/
│           ├── auth.route.js
│           └── message.route.js
├── frontend/
│   ├── package.json
│   ├── README.md
│   ├── index.html
│   ├── tailwind.config.js
│   ├── vite.config.js
│   ├── eslint.config.js
│   ├── public/
│   │   ├── avatar.png
│   │   └── vite.svg
│   └── src/
│       ├── App.jsx
│       ├── index.css
│       ├── main.jsx
│       ├── components/
│       │   ├── AuthImagePattern.jsx
│       │   ├── Navbar.jsx
│       │   └── MessageInput.jsx
│       ├── lib/
│       │   └── axios.js
│       ├── pages/
│       │   ├── HomePage.jsx
│       │   ├── LoginPage.jsx
│       │   ├── ProfilePage.jsx
│       │   ├── SettingsPage.jsx
│       │   └── SignUpPage.jsx
│       └── store/
│           ├── useAuthStore.js
│           └── useThemeStore.js                   # Node modules (generated after running npm install)
```

## Getting Started
# .env
PORT=5001

MONGODB_URI=your_mongodb_connection_string

JWT_SECRET=your_strong_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

NODE_ENV=development

### Prerequisites

Ensure you have the following tools installed on your development machine:

**Node.js** (Latest LTS recommended)
**npm** (comes with Node.js) or **yarn**
**MongoDB Atlas** account (for cloud database)
**Cloudinary** account (for image uploads)

- **React.js** (Use current version)
- **npm** or **yarn**

### Installation

Clone the repository to your local machine:

```bash
https://github.com/BadshahYadav/MERN-Chat-App
cd MERN-Chat-App
```

Install the dependencies:

```bash
npm install
# or
yarn install
```

### Running the Project

To start the development server, run:

```bash
npm run start
# or
yarn start
```

By default, the backend runs on http://localhost:5001 and the frontend on http://localhost:5173.

## Environment Variables Setup

The project requires the following environment variables. Create a .env file in the backend directory and add your values:

```plaintext
PORT=5001
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_strong_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
NODE_ENV=development
```
Note: Do not include spaces around the = sign. Never commit your .env file to version control.

## How to use environment variables in the frontend (Vite):

If you need custom environment variables in the frontend, create a .env file in the frontend directory and prefix variables with VITE_:
```plaintext
VITE_API_URL=http://localhost:5001/api
```

In your React code:
```plaintext
const apiUrl = import.meta.env.VITE_API_URL;
console.log(apiUrl);  // Outputs: http://localhost:5001/api
```
## Deployment (GitHub Pages)

**1. Prepare Your Project** :
- Make sure your backend serves the frontend’s static files in production (your backend index.js already does this).
- Ensure your .env file is not committed to GitHub. You will add environment variables in the Render dashboard.

**2. Push Your Code to GitHub** :
- Commit and push all your latest changes to your GitHub repository.
 

**3. Create a New Web Service on Render** :
- Go to https://dashboard.render.com/ and log in.
- Click New + → Web Service.
- Connect your GitHub account and select your repository.

**4. Configure Build & Start Commands** :
- **Root Directory**: (leave blank or / if your backend is at the root).
- **Build Command** : 
```bash
npm run build
```
- **Start Command** :
 ```bash
npm start
```

**5. Add Environment Variables** :
- In the Render dashboard, go to the "Environment" section and add the following (from your backend .env):

 ```bash
PORT=5001
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_strong_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
NODE_ENV=production
```
**NOTE** : Do not include quotes or spaces around the = sign.

**6. Deploy** :
- Click Create Web Service.
- Render will install dependencies, build your frontend, and start your backend server.
- Once deployed, you’ll get a public URL for your app.

**7. (Optional) Update CORS** :
- In your backend, set the CORS origin to your Render URL for production:

```bash
origin: process.env.CLIENT_URL || "http://localhost:5173"
```
**NOTE** : Add CLIENT_URL to your Render environment variables if needed.

Follow the prompts to deploy your application.

## Contact

If you have any questions or feedback, feel free to contact me via the [contact form](https://badshahyadav.github.io/Portfolio/) on my portfolio website or connect with me through my social profiles.

## 🔗 Links
[![instagram](https://img.shields.io/badge/instagram-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/BadshahYadav)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/badshah-kumar-830146234/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/_Emperor_4k)

## License

This project is open-source and available under the [MIT License](https://github.com/BadshahYadav/MERN-Chat-App/blob/main/LICENSE)




