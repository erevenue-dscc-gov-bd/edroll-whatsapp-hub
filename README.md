# Edroll WhatsApp Hub

GitHub-ready starter for the Edroll multi-WhatsApp monitoring platform.

## Included
- Frontend dashboard prototype with login, central inbox, accounts, agent performance, reports, SLA, activity log and integrations.
- Node/Express backend scaffold for Meta WhatsApp Cloud API message sending.
- Environment-based Meta credentials.
- Webhook placeholder routes for later implementation.

## Demo Login
Email: `admin@edrolleducation.com`
Password: `admin123`

> Demo authentication is frontend-only. Do not use it as production authentication.

## Run Frontend
Open `frontend/index.html` in a browser, or serve the `frontend` directory with any static web server.

## Run Backend
```bash
cd backend
npm install
copy .env.example .env
npm run dev
```

Linux/macOS:
```bash
cp .env.example .env
npm install
npm run dev
```

Backend: `http://localhost:3000`

## Meta Configuration
Put secrets only in `backend/.env`:
- `META_PHONE_NUMBER_ID`
- `META_ACCESS_TOKEN`
- `META_VERIFY_TOKEN`
- `META_APP_SECRET`
- `META_GRAPH_VERSION`

Never commit `.env`.

## Current API
- `GET /api/health`
- `GET /api/config`
- `GET /api/health/db`
- `GET /api/webhook/status`
- `POST /api/messages/send`
- `GET /api/webhook/whatsapp` (placeholder)
- `POST /api/webhook/whatsapp` (placeholder)

## Important
This repository is a development scaffold, not production SaaS yet. For production add PostgreSQL/Supabase, real user authentication, password hashing, JWT/session management, RBAC enforcement on the server, multi-account Meta credential storage/secret management, webhook verification and event processing, message persistence, Socket.IO/WebSockets, response/SLA calculations, audit logs, HTTPS and deployment.
