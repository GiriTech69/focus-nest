<h1 align="center">Focus-Nest ⏱️</h1>

<div align="center">

![Status](https://img.shields.io/badge/status-ongoing-orange)
![Built with Bun](https://img.shields.io/badge/Bun-F472B6?style=flat&logo=bun&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Plasmo](https://img.shields.io/badge/Plasmo-000000?style=flat&logo=plasmo&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat)
![Auth0](https://img.shields.io/badge/Auth0-EB5424?style=flat&logo=auth0&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue)

</div>



Welcome to **Focus nest - Our Time Tracker**—a unified time-tracking platform combining a **React + Plasmo browser extension**, a **React + Vite app**, and a **Node.js + Express** backend with **PostgreSQL**. 

## 🛠️ Tech Stack Overview

| Layer | Technology | Purpose |
| :-- | :-- | :-- |
| Backend API | Node.js + Express | RESTful API server managing business logic |
| Frontend (Extension) | React + Plasmo | Browser extension UI \& logic |
| Frontend (Website) | React + Vite | Web app user interface |
| Database | PostgreSQL | Reliable relational database for all data |
| Styling | Tailwind CSS | Utility-first CSS for consistent styling |
| State \& Data Fetch | TanStack Query | Efficient data fetching, caching, and syncing |
| Authentication | Auth0 | OAuth2 \& JWT-based secure user authentication |

## 📁 Project Structure

```plaintext
focus-nest/
│
├── apps/
│   ├── extension/                 # Browser extension React app using Plasmo
│   │   ├── public/                Static assets (icons, manifest.json, etc.)
│   │   ├── src/
│   │   │   ├── components/        # Extension-specific React components
│   │   │   ├── hooks/             # Extension-specific hooks (can import shared hooks)
│   │   │   ├── styles/            # Tailwind CSS styles for extension
│   │   │   ├── background.ts      # Background/service-worker script
│   │   │   ├── popup.tsx          # Extension popup React entrypoint
│   │   │   ├── options.tsx        # Extension options/settings page
│   │   │   └── index.tsx          # React app bootstrap file
│   │   ├── tests/                 # Extension unit/integration tests
│   │   ├── package.json
│   │   ├── tsconfig.json
│   │   └── plasmo.config.ts       # Plasmo config file for extension builds
│
│   └── web/                       # Website React app (Vite)
│       ├── public/                # Static assets (images, favicon, robots.txt)
│       ├── src/
│       │   ├── components/        # Website-specific React components
│       │   ├── hooks/             # Website hooks (can reuse shared hooks)
│       │   ├── styles/            # Tailwind CSS styles for website
│       │   ├── pages/             # SPA pages (React Router)
│       │   ├── App.tsx            # Main React app component
│       │   └── main.tsx           # React entrypoint for Vite build
│       ├── tests/                 # Website unit/E2E tests
│       ├── package.json
│       ├── tsconfig.json
│       └── vite.config.ts         # Vite config file for web app
│
├── packages/                     # Shared libraries for extension and website
│   ├── ui/                       # Shared UI components (buttons, modals, inputs, etc.)
│   │   ├── src/
│   │   │   ├── Button.tsx
│   │   │   ├── Modal.tsx
│   │   │   └── …
│   │   ├── package.json
│   │   └── tsconfig.json
│   │
│   ├── hooks/                    # Shared React hooks (e.g., useAuth, useTimer)
│   │   ├── src/
│   │   │   ├── useAuth.ts
│   │   │   ├── useTimer.ts
│   │   │   └── …
│   │   ├── package.json
│   │   └── tsconfig.json
│   │
│   ├── api/                      # API client logic & TanStack Query hooks
│   │   ├── src/
│   │   │   ├── apiClient.ts
│   │   │   ├── timersApi.ts
│   │   │   └── …
│   │   ├── package.json
│   │   └── tsconfig.json
│   │
│   ├── utils/                    # Shared utilities/helpers (date formatting, validation)
│   │   ├── src/
│   │   │   ├── dateUtils.ts
│   │   │   ├── validation.ts
│   │   │   └── …
│   │   ├── package.json
│   │   └── tsconfig.json
│   │
│   └── types/                    # Shared TypeScript types/interfaces
│       ├── src/
│       │   ├── user.ts
│       │   ├── timeEntry.ts
│       │   └── …
│       ├── package.json
│       └── tsconfig.json
│
├── backend/                      # Node.js + Express backend API server
│   ├── src/
│   │   ├── controllers/          # Express route handlers and business logic
│   │   ├── models/               # ORM models (e.g., Prisma)
│   │   ├── routes/               # Express route definitions
│   │   ├── services/             # Service layer (DB access, auth verification)
│   │   ├── utils/                # Helper utilities
│   │   ├── app.ts                # Express app initialization
│   │   └── server.ts             # Server bootstrap (listen, middleware setup)
│   ├── tests/                    # Backend unit/integration tests
│   ├── package.json
│   ├── tsconfig.json
│   ├── prisma/                   # Prisma schema & migrations
│   │   ├── schema.prisma
│   │   ├── migrations/
│   │   └── …
│   └── .env                      # Environment variables (DB connection, JWT secrets)
│
├── .gitignore
├── package.json                 # Root workspaces: ["apps/*","packages/*","backend"]
├── bun.lockb                    # Bun lockfile
├── tsconfig.json                # Root TypeScript config referencing all workspaces
└── README.md                    # Project README documentation
```


## 🚀 Getting Started

### Prerequisites

- Node.js (v18+)
- Bun (https://bun.sh/)
- PostgreSQL instance
- Auth0 tenant


### Installation \& Setup

1. **Clone repository**
`git clone https://your-repo-url.git && cd focus-nest`
2. **Install dependencies**
`bun install`
3. **Configure environment**
Create `backend/.env` with:

```env
DATABASE_URL=postgresql://user:password@host:port/dbname
AUTH0_DOMAIN=your-auth0-domain
AUTH0_CLIENT_ID=your-auth0-client-id
AUTH0_CLIENT_SECRET=your-auth0-client-secret
JWT_SECRET=your-own-jwt-secret
```

4. **Run database migrations**

```bash
cd backend
npx prisma migrate deploy
```

5. **Start services**
    - Backend: `bun run dev --cwd backend`
    - Web app: `bun run dev --cwd apps/web`
    - Extension: `bun run dev --cwd apps/extension`
6. **Load extension**
In Firefox/Chrome developer mode, load unpacked extension from `apps/extension`.

## 🧩 Key Features

- Quick time tracking via browser extension
- Full management, reporting, and admin on web app
- Real-time sync between extension \& website
- Secure Auth0 OAuth2 + JWT authentication
- Responsive UI with Tailwind CSS \& shared React components
- Robust data handling with TanStack Query


## 🛠️ Scripts

```bash
bun install
bun run dev --cwd backend
bun run dev --cwd apps/web
bun run dev --cwd apps/extension
bun test
```


## 🤝 Contributing

Contributions welcome! Open issues or PRs on the repo.

## 📜 License

MIT License

Thank you for building with us! 🌟
Empower productivity, one tracked second at a time ⏳

