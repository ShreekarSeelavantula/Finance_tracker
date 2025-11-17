# AI Finance Platform

A full-stack finance web app built with Node.js (app directory), Mangodb, Prisma, Tailwind CSS, Inngest, ArcJet and Shadcn UI , CSS. This repository contains the frontend, API routes, background functions, and Prisma schema for a personal finance dashboard and transaction manager.

**Status:** Work in progress

**Screenshot:** (see `public/` or project preview)

**Contents**
- **App:** Node.js app using the `app/` directory for pages and layouts.
- **API:** Serverless routes under `app/api/` and `actions/` for background jobs and helpers.
- **DB:** Prisma schema and migrations under `prisma/`.
- **Components:** Reusable UI primitives under `components/` and `components/ui/`.

**Features (examples)**
- Account and budget management
- Transaction creation, scanning receipts, and tables
- Dashboard with charts and overview cards
- Background jobs and event handlers using Inngest

**Tech stack**
- React.js
- Mango db
- CSS
- Node.js
- Inngest for background functions
- ArcJet for AI-assisted features

**Prerequisites**
- Node.js (v18+ recommended)
- A Mangodb Database
- Environment variables for Mangodb, database, and any third-party keys (Inngest, ArcJet)

Getting started (local)

1. Install dependencies

```bash
npm install
```

2. Create environment variables

Create a `.env.local` (or set env vars) with at least:

```
DATABASE_URL=...
NEXT_PUBLIC_SUPABASE_URL=...
NEXT_PUBLIC_SUPABASE_ANON_KEY=...
INNGEST_API_KEY=...
ARCJET_API_KEY=...
```

3. Run database migrations

```bash
npx prisma migrate dev --name init
```

4. (Optional) Seed the database

If a seed script exists, run it; otherwise use your preferred seeding method:

```bash
# Example, adjust if project exposes a seed action
node actions/seed.js
```

5. Start the development server

```bash
npm run dev
```

Build and production

```bash
npm run build
npm start
```

Notes
- The project uses the Node.js — pages live under `app/`.
- Check `prisma/schema.prisma` for the current data model and `prisma/migrations/` for migration history.
- Background functions and event handlers are in `actions/` and `lib/inngest/`.

Contributing
- Open issues or PRs for bug fixes and features.
- Keep changes small and focused; add tests where appropriate.

License
- This repository does not include a license file by default. Add one (for example, `MIT`) if you want others to reuse the code.

Questions or help
- If you want me to add a more detailed README (environment examples, `.env.example`, CI, or deployment steps), tell me what you'd like included and I will update it.