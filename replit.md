# Workspace

## Overview

LTGPay — a full-stack crypto investment platform built with React + Vite frontend and Express backend.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Frontend**: React + Vite, TanStack React Query, Recharts, Framer Motion, Tailwind CSS
- **Auth**: express-session + bcrypt
- **Build**: esbuild (CJS bundle)

## Structure

```text
artifacts-monorepo/
├── artifacts/              # Deployable applications
│   ├── api-server/         # Express API server
│   └── ltgpay/             # React + Vite frontend
├── lib/                    # Shared libraries
│   ├── api-spec/           # OpenAPI spec + Orval codegen config
│   ├── api-client-react/   # Generated React Query hooks
│   ├── api-zod/            # Generated Zod schemas from OpenAPI
│   └── db/                 # Drizzle ORM schema + DB connection
├── scripts/                # Utility scripts
├── pnpm-workspace.yaml     
├── tsconfig.base.json      
├── tsconfig.json           
└── package.json            
```

## Features

1. **Landing Page** — Hero, features, investment plans preview
2. **User Auth** — Register, Login, Logout (session-based)
3. **Dashboard** — Balance, earnings, charts, transactions
4. **Investment Plans** — 3 plans (Starter, Growth, Elite), invest modal
5. **My Investments** — Active/completed investments table
6. **Deposit System** — Crypto wallet deposits (BTC, ETH, USDT, LTC)
7. **Withdraw System** — Withdrawal requests with balance check
8. **Referral System** — Referral links, 5% commission tracking
9. **Admin Panel** — Users, deposits, withdrawals, plans management

## Admin Access

- Email: `admin@ltgpay.com`
- Password: `admin123`

## Investment Plans

| Plan | Min | Max | Daily Return | Duration | Total Return |
|------|-----|-----|-------------|---------|-------------|
| Starter | $50 | $999 | 1.5% | 30 days | 45% |
| Growth | $1,000 | $4,999 | 2.5% | 45 days | 112.5% |
| Elite | $5,000 | $50,000 | 4.0% | 60 days | 240% |

## Crypto Wallet Addresses

- BTC: bc1qxy2kgdygjrsqtzq2n0yrf2493p83kkfjhx0wlh
- ETH: 0x742d35Cc6634C0532925a3b8D4C9C5e6c6e9e3b1
- USDT: TN9RQjATsDLBhBbW5wuqEjEHAceBHLhWAP
- LTC: LhyLmD7TbhEFPBpKaBSmybsYK7ZLVS1AcK

## DB Schema

- `users` — user accounts, balances, referral codes, roles
- `investment_plans` — platform investment plans
- `investments` — user investments with earnings tracking
- `deposits` — deposit requests with status
- `withdrawals` — withdrawal requests with status
- `referral_earnings` — referral commission records

## Referral System

5% commission credited to referrer when a referred user's deposit is approved.
