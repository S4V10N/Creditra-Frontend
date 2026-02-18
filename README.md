# Creditra Frontend

Lender and borrower dashboard for the Creditra adaptive credit protocol on Stellar.

## About

This app provides a simple UI to:

- View dashboard summary (credit limit, utilization, risk score)
- Browse and manage credit lines
- (Future) Connect wallet, request credit evaluation, draw and repay

It talks to the **creditra-backend** API for risk and credit data, and can be extended to interact with Soroban contracts via Stellar SDK.

## Tech Stack

- **React 18** + **TypeScript**
- **Vite** for build and dev server
- **React Router** for navigation

## Setup

### Prerequisites

- Node.js 18+
- npm or yarn

### Install and run

```bash
cd creditra-frontend
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173).

### Build for production

```bash
npm run build
npm run preview   # serve dist/
```

### Environment

Create a `.env` file if you need to point to a specific backend:

```env
VITE_API_URL=http://localhost:3000
```

Use `import.meta.env.VITE_API_URL` in the app.

## Project layout

- `src/` — React app (main, App, pages, styles)
- `src/pages/` — Dashboard, Credit Lines
- `index.html` — entry HTML
- `vite.config.ts` — Vite config and path alias `@/`

## Merging to remote

This repo is a standalone git repository. After adding your remote:

```bash
git remote add origin <your-creditra-frontend-repo-url>
git push -u origin main
```
