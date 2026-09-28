# EventSphere

A full-stack event management platform for organizing festivals and technical events, with registrations, leaderboards, and participant tracking.

## Features

- User signup and login with JWT authentication
- Organizer and participant dashboards
- Browse events and sub-events, with a schedule view
- Event registration and check-in
- Leaderboard

## Tech Stack

- **Frontend:** React, Vite, Tailwind CSS
- **Backend:** Node.js, Express
- **Database:** MongoDB Atlas (Mongoose)
- **Auth:** JSON Web Tokens (JWT)

## Project Structure

```
Event_Sphere/
├── backend/    # Express API
└── frontend/   # React app (Vite)
```

## Getting Started

### Prerequisites

- Node.js (v18 or later)
- A MongoDB Atlas account (or a local MongoDB)

### 1. Clone the repository

```bash
git clone https://github.com/shuklaaryan586/Event_Sphere.git
cd Event_Sphere
```

### 2. Set up the backend

```bash
cd backend
npm install
cp .env.example .env
```

On Windows PowerShell, use `Copy-Item .env.example .env` instead of `cp`.

Open `.env` and fill in your values:

```
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=a_long_random_string
CLIENT_URL=http://localhost:5173
```

Start the server:

```bash
npm run dev
```

You should see `MongoDB connected` and `EventSphere API running on port 5000`.

### 3. Set up the frontend

Open a second terminal:

```bash
cd frontend
npm install
cp .env.example .env
npm run dev
```

The default `.env` already points to the backend:

```
VITE_API_URL=http://localhost:5000/api
```

Open http://localhost:5173 in your browser.

## API Overview

| Area | Endpoints |
|---|---|
| Auth | `POST /api/auth/signup`, `POST /api/auth/login`, `GET /api/auth/me` |
| Sub-events | `/api/subevents` |
| Registrations | `/api/registrations` |
| Leaderboard | `/api/leaderboard` |
| Health check | `GET /api/health` |

## Environment Variables

Real `.env` files are never committed. Use the `.env.example` files in `backend` and `frontend` as templates.

## Author

Aryan Shukla