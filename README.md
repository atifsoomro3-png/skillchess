# SkillChess

Full-stack crypto-first chess platform with:

- USDT-only wallet accounting
- JWT auth with separate admin login
- Admin-reviewed P2P deposits with chat threads
- Withdrawal approvals
- Real chess.js match engine with checkmate, timeout, resign, disconnect, and draw settlement
- Transaction logs, notifications, leaderboard, and disputes

## Stack

- Frontend: React, Vite, React Router, Framer Motion, Socket.IO client
- Backend: Express, Socket.IO, bcrypt, JWT, Zod
- Local database: embedded SQLite via Node's `node:sqlite`
- Production schema snapshot: [server/data/postgres-schema.sql](/C:/Users/Administrator/Documents/Codex/2026-04-24/files-mentioned-by-the-user-chess/server/data/postgres-schema.sql)

## Run

```bash
npm install
npm run dev
```

Frontend: `http://localhost:5173`

Backend: `http://localhost:4000`

## Seeded Accounts

- Player: `player@skillchess.gg` / `Password123!`
- Admin: `admin@skillchess.gg` / `Admin123!`

## Key Routes

- `/login`
- `/register`
- `/admin/login`
- `/app`
- `/admin`

## Notes

- Wallet balances are stored in USDT only.
- Local currency values are UI-only for deposit entry and display conversion.
- Uploaded screenshots and attachments are stored under `server/uploads`.
- The local dev database is stored at `server/data/skillchess.db`.

## Vercel Deployment

This repo is prepared for a frontend deployment on Vercel using [vercel.json](/C:/Users/Administrator/Documents/Codex/2026-04-24/files-mentioned-by-the-user-chess/vercel.json).

- Build command: `npm run build --workspace client`
- Output directory: `client/dist`
- SPA routing is handled with a rewrite to `index.html`

Important:

- The current backend is not fully Vercel-compatible as-is because it uses local SQLite storage and in-process Socket.IO realtime state.
- For a full production deployment, keep the frontend on Vercel and move the backend/database/uploads to external infrastructure.
"# Skillchess" 
"# Skillchess" 
"# Skillchess" 
