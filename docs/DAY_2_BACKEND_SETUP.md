# Day 2 – Backend Initialization

## Objective

Initialize the CreatorPulse backend using Node.js and Express.js.

## Work Completed

* Initialized the Node.js backend
* Installed Express.js
* Installed CORS
* Installed dotenv
* Installed nodemon as a development dependency
* Created the Express server
* Added environment variable configuration
* Added the /api/health endpoint
* Configured the development and production start scripts

## Backend Structure

* **`backend/src/server.js`**: The main entry point of the Express application. It initializes the server, configures CORS and JSON body-parsing middlewares, loads environment variables, defines the `/api/health` endpoint, and listens on the configured port.
* **`backend/.env`**: Stores local environment variable definitions (e.g. `PORT=5000`). This file is git-ignored to keep environment configurations local.
* **`backend/.env.example`**: A committed template file showing the required environment variables without exposing sensitive values.
* **`backend/package.json`**: Contains project metadata, installed dependencies (`express`, `cors`, `dotenv`, and `nodemon`), and start scripts (`npm start` and `npm run dev`).

## API

### GET /api/health

The `/api/health` endpoint is used to perform a health check on the backend server to confirm it is up and running properly.

**Expected JSON Response:**
```json
{
  "success": true,
  "message": "CreatorPulse backend is running"
}
```

## Running the Backend

1. Navigate to the `backend` folder and install dependencies:
   ```bash
   cd backend
   npm install
   ```

2. Start the backend in development mode:
   ```bash
   npm run dev
   ```

By default, the backend runs on port **5000** during local development (`http://localhost:5000`).
