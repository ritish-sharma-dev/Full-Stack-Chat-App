# Full-Stack-Chat-App

> A high-performance, real-time messaging platform engineered with the MERN stack and WebSockets.

Welcome to the **Full-Stack-Chat-App**, a comprehensive communication solution designed for seamless, instantaneous interaction. Built utilizing modern web technologies—MongoDB, Express.js, React, and Node.js—alongside Socket.io for bi-directional communication, this application delivers a robust and scalable chatting experience. From secure user authentication to real-time image sharing, it encompasses all the essential features expected of a modern chat application.

## ✨ Key Features

- **Robust Authentication Architecture**: Secure user onboarding and session management using JSON Web Tokens (JWT) stored safely in HTTP-only cookies, combined with bcryptjs for rigorous password cryptography.
- **Instantaneous Real-Time Messaging**: Experience zero-latency communication. Powered by `Socket.io`, messages are dispatched and received in true real-time.
- **Seamless Media Sharing**: Enhance conversations with visual context. Users can effortlessly upload and share images within chats and personalize their profiles, backed by reliable `Cloudinary` integration.
- **Secure Protected Routing**: Strict client-side access control via React Router guarantees that private interfaces and conversations remain completely inaccessible to unauthenticated users.
- **Premium Responsive Interface**: A meticulously crafted, mobile-first User Interface developed with `TailwindCSS` and `React`, ensuring a flawless experience across all devices and screen sizes.
- **Interactive UI Feedback**: Integrated, elegant toast notifications using `react-hot-toast` provide immediate and unobtrusive feedback for user actions and system events.
- **Optimized Data Persistence**: Efficient and scalable data modeling powered by `Mongoose` schemas over a `MongoDB` database infrastructure.

## 🛠️ Technology Stack

### Frontend (Client Application)
- **Framework**: React 19 (Bootstrapped with Vite for optimal build performance)
- **Routing**: React Router v7
- **Styling**: TailwindCSS v4
- **Real-Time Engine**: Socket.io-client
- **HTTP Client**: Axios
- **State Management**: React Context API

### Backend (Server Architecture)
- **Runtime Environment**: Node.js
- **API Framework**: Express.js
- **Database**: MongoDB with Mongoose ODM
- **Real-Time Server**: Socket.io
- **Security**: JSON Web Token (JWT) & BcryptJS
- **Media Management**: Cloudinary
- **Middleware**: Cookie Parser

---

## 🚀 Getting Started

Follow this guide to get a local development environment up and running.

### Prerequisites

Ensure your system meets the following requirements:
- **Node.js**: v18.0.0 or higher recommended.
- **MongoDB**: A local instance or a cloud-hosted MongoDB Atlas cluster.
- **Cloudinary**: An active account to retrieve API credentials for image processing.

### 1. Repository Setup

Clone the repository to your local machine:

```bash
git clone https://github.com/ritish-sharma-dev/Full-Stack-Chat-App.git
cd Full-Stack-Chat-App
```

### 2. Backend Initialization (Server)

Navigate to the server directory and install the necessary dependencies:

```bash
cd server
npm install
```

Create a `.env` configuration file in the root of the `server` directory and populate it with your environment-specific variables:

```env
# Database Configuration
MONGODB_URI=your_mongodb_connection_string

# Server Configuration
PORT=5000
NODE_ENV=development

# Security Configuration
JWT_SECRET=your_super_secret_jwt_key
CLIENT_URL=http://localhost:5173

# Cloudinary Storage Configuration
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

Launch the backend server in development mode:

```bash
npm run dev
```

*The API server will now be listening for requests, typically on `http://localhost:5000`.*

### 3. Frontend Initialization (Client)

Open a secondary terminal, navigate to the client directory, and install its dependencies:

```bash
cd client
npm install
```

Create a `.env` configuration file in the root of the `client` directory:

```env
# API Endpoint Mapping
VITE_BACKEND_URL=http://localhost:5000
MODE=development
```

Start the frontend development server:

```bash
npm run dev
```

*The React application will compile and launch, accessible via `http://localhost:5173`. Open this address in your preferred web browser to interact with the Full-Stack-Chat-App.*

---

## 📁 System Architecture

A high-level overview of the repository's structural organization:

```text
Full-Stack-Chat-App/
├── client/                 # Frontend React Application Workspace
│   ├── src/
│   │   ├── assets/         # Static media assets (e.g., SVG backgrounds)
│   │   ├── components/     # Modular, reusable UI components (Sidebar, Chat Window)
│   │   ├── context/        # Global state management providers (AuthContext)
│   │   ├── lib/            # Utility functions and external service configurations (Axios)
│   │   ├── pages/          # Top-level view components (Home, Authentication, Profile)
│   │   ├── App.jsx         # Application root defining routing logic
│   │   └── main.jsx        # Frontend entry point and DOM mounting
│   ├── index.html
│   ├── package.json
│   └── vite.config.js
│
└── server/                 # Backend Express Application Workspace
    ├── src/
    │   ├── controllers/    # Request handling and business logic (Auth, Messaging)
    │   ├── lib/            # Core configuration (Database connection, Socket setup)
    │   ├── middleware/     # Request interception (Authentication verification)
    │   ├── models/         # Database schema definitions (User, Message)
    │   ├── routes/         # API endpoint definitions and controller mapping
    │   └── index.js        # Backend entry point and server initialization
    └── package.json
```
