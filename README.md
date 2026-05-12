# Organizo

A modern personal finance and task management application built with React.js, Express, Clerk Authentication, and Supabase.

## Features

- 🔐 Secure authentication with Clerk
- 💰 Budget tracking and visualization
- ✅ Task management with priorities
- 📊 Interactive charts and statistics
- 🌓 Dark/Light mode support
- 📱 Responsive design

## Tech Stack

### Frontend

- React.js with Vite
- Chakra UI for styling
- React Router for navigation
- Chart.js for visualizations
- Clerk for authentication

### Backend

- Express.js
- Supabase for database
- Node.js

## Prerequisites

- Node.js (v18 or higher)
- npm
- Clerk account for authentication
- Supabase account for database

## Environment Setup

### Client (.env)

```
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_key
VITE_API_URL=http://localhost:3001
```

### Server (.env)

```
PORT=3001
SUPABASE_URL=your_supabase_url
SUPABASE_SERVICE_KEY=your_supabase_service_key
NODE_ENV=development
```

## Supabase Migration Checklist

When your old Supabase project expires, create a new Supabase project and update these values:

1. Copy the new project URL into `SUPABASE_URL` in `server/.env`.
2. Copy the new service role key into `SUPABASE_SERVICE_KEY` in `server/.env`.
3. Open the new project SQL editor and run `server/schema.sql` to recreate `tasks`, `transactions`, and `user_settings`.
4. Reapply any Row Level Security policies, indexes, and grants from `server/schema.sql` if they are not created by the import.
5. Update the backend deployment environment variables with the same new Supabase values.
6. Restart the backend, then restart the frontend so it picks up the API URL change.

### What changed in this repo

- The frontend API base URL now accepts `VITE_API_URL` and `VITE_API_BASE_URL`, so the app keeps working during migration.
- The client env example now uses `VITE_API_URL`, matching the actual app code.
- The README now reflects the current architecture: the client talks to the Express API, and the server talks to Supabase.

## Installation

1. Clone the repository

```bash
git clone https://github.com/yourusername/organizo.git
cd organizo
```

2. Install frontend dependencies

```bash
cd client
npm install
```

3. Install backend dependencies

```bash
cd ../server
npm install
```

## Development

1. Start the backend server

```bash
cd server
npm run dev
```

2. Start the frontend development server

```bash
cd client
npm run dev
```

## Features Overview

### Budget Buddy

- Track monthly income and expenses
- Categorize transactions
- Visualize spending patterns
- Set and track savings goals

### Task Manager

- Create and manage tasks
- Set priorities and due dates
- Track completion status
- Organize with categories

### Home Dashboard

- View daily tasks
- Track balance trends
- Quick access to key features

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
