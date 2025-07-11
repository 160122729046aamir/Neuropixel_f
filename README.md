# NeuroPixel

A full-stack AI-powered text-to-image generator web application.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Frontend Structure](#frontend-structure)
- [Backend Structure](#backend-structure)
- [Setup & Installation](#setup--installation)
- [Usage](#usage)
- [License](#license)

---

## Project Overview
NeuroPixel is a modern web application that allows users to generate images from text prompts using AI (powered by ClipDrop). It features a beautiful, responsive frontend and a robust backend with authentication, credit management, Razorpay payment integration, and image generation APIs.

## Features
- AI-powered text-to-image generation (via ClipDrop API)
- User authentication (login/signup)
- Credit-based usage system
- Purchase credits with different plans
- Razorpay payment integration for secure transactions
- Responsive, modern UI/UX
- Download generated images
- Testimonials and onboarding steps

## Tech Stack
- **Frontend:** React, Vite, Tailwind CSS, Motion (Framer Motion), Razorpay Web Integration
- **Backend:** Node.js, Express.js, MongoDB, ClipDrop API, Razorpay Node Integration

---

## Project Structure
```
NeuroPixel/
│
├── frontend/         # React frontend (Vite + Tailwind)
├── backend/          # Node.js/Express backend
└── README.md         # Project documentation
```

---

## Frontend Structure
```
frontend/
│
├── public/           # Static assets (favicons, SVGs)
├── src/
│   ├── assets/       # Images, icons, and asset definitions
│   ├── components/   # Reusable React components (Navbar, Footer, etc.)
│   ├── context/      # React context for global state (AppContext)
│   ├── pages/        # Main pages (Home, BuyCredit, Result)
│   ├── App.jsx       # Main app component
│   ├── App.css       # Global styles
│   ├── index.css     # Tailwind and base styles
│   └── main.jsx      # Entry point
├── package.json      # Frontend dependencies and scripts
├── vite.config.js    # Vite configuration
└── eslint.config.js  # Linting configuration
```

### Key Files & Folders
- **assets/**: Contains all SVGs, PNGs, and the `assets.js` file for asset imports.
- **components/**: UI components like `Navbar`, `Footer`, `Header`, `Login`, `Steps`, `Testimonials`, `GenerateBtn`, and `Description`.
- **context/AppContext.jsx**: Provides global state (user, login modal, etc.).
- **pages/**: Main pages (`Home`, `BuyCredit`, `Result`).
- **App.jsx**: Main routing and layout.

---

## Backend Structure
```
backend/
│
├── config/           # Database configuration (dbConfig.js)
├── controllers/      # Route controllers (user, image generation)
├── middlewares/      # Express middlewares (auth, etc.)
├── models/           # Mongoose models (User, Transaction)
├── routes/           # Express routes (userRoutes, gntImageRoutes)
├── server.js         # Main Express server entry point
├── package.json      # Backend dependencies and scripts
└── .env              # Environment variables
```

### Key Files & Folders
- **config/dbConfig.js**: MongoDB connection setup.
- **models/**: Mongoose models for users and transactions.
- **controllers/**: Business logic for user and image generation.
- **middlewares/AuthMiddleware.js**: Authentication middleware.
- **routes/**: API endpoints for users and image generation.
- **server.js**: Express app setup and server start.

---

## Setup & Installation

### Prerequisites
- Node.js (v16+ recommended)
- npm or yarn
- MongoDB instance (local or cloud)

### 1. Clone the repository
```sh
git clone <repo-url>
cd NeuroPixel
```

### 2. Setup Backend
```sh
cd backend
npm install
# Create a .env file with your MongoDB URI and other secrets
npm start
```

### 3. Setup Frontend
```sh
cd frontend
npm install
npm run dev
```

### 4. Open in Browser
Visit `http://localhost:5173` (or the port shown in your terminal).

---

## Usage
- Register or log in to your account.
- Purchase credits to generate images.
- Enter a text prompt and generate images using AI.
- Download your generated images.

---

## License
This project is licensed under the MIT License.
