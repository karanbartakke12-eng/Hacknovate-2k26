
# Smart Pune Safety Dashboard

Full-stack civic safety platform for Pune with React, Node.js, Express, MongoDB, JWT auth, Socket.io live events, upload handling, analytics, admin-ready APIs, and production deployment config.

## Local Setup

1. Copy `.env.example` to `.env`.
2. Set `MONGO_URI`, `JWT_ACCESS_SECRET`, `JWT_REFRESH_SECRET`, and optional SMTP settings.
3. Install dependencies with `pnpm install` or `npm install`.
4. Start MongoDB locally, or run `docker compose up mongo`.
5. Seed the database with `pnpm seed` or `npm run seed`.
6. Start both frontend and backend with `pnpm dev:full` or `npm run dev:full`.

Frontend: `http://localhost:5173`
Backend: `http://localhost:5000/api/v1`
API docs: `http://localhost:5000/api/docs`

## Seed Accounts

- Admin: `admin@punesafety.local` / `Admin@12345`
- User: `priya.sharma@example.com` / `User@12345`

## Backend Coverage

- Authentication: signup, login, JWT session refresh, logout, email OTP verification, forgot/reset password, role-based access control.
- Complaints: categories, evidence uploads, status workflow, upvotes, views, pagination, search, filtering.
- Community: posts, comments, reactions, trending posts, moderation-ready status.
- Alerts: alert feed, severity filtering, read tracking, notification history.
- Emergency: SOS/unsafe/siren/location-share/safe-travel events with Socket.io operations broadcasts.
- Map: risk zones, emergency services, safe route scoring.
- Analytics/admin: dashboard metrics, event tracking, user activity logging.
- Security: Helmet, CORS, rate limiting, Mongo sanitization, HPP protection, password hashing, secure cookies, validation, centralized errors.

## Deployment

Docker, Docker Compose, Render, Railway, and Vercel config files are included. In production, the Express server can serve the Vite build from `dist` and the REST API from `/api/v1`.
  
