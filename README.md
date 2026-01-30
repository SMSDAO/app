SMSDAO / Ethereum Follow Protocol Web App
⚡ The Social Portfolio Platform for On‑Chain Identity, Social Graphs & DAO Intelligence
<p align="center">
<img src="https://raw.githubusercontent.com/SMSDAO/app/main/public/icon.png" width="120" />
</p>

<p align="center">
<strong>Next‑gen social wallet platform built on Next.js  15, React 19, and multi‑chain identity.</strong><br/>
<em>Track portfolios, social activity, DAO governance, and creator ecosystems — all in one unified interface.</em>
</p>

🚀 Features
🧬 Unified On‑Chain Identity
ENS resolution

Multi‑chain address identity

Profile claiming (SIWE)

Avatar, bio, badges, social metadata

💰 Portfolio Intelligence
Multi‑chain token balances

NFT collections

Transaction history

Real‑time performance metrics

🟣 Social Graph Integrations
Farcaster profiles, casts, reactions

Lens Protocol profiles & publications

Zora creations, mints, collections

🏛 DAO Governance Analytics
Snapshot proposals, votes, spaces

Tally on‑chain governance

Delegations, voting power, participation

🔍 Search Engine
Profiles

DAOs

Tokens

NFTs

🎨 Neo Glow UI / AuraFX Animations
Tailwind CSS 4

React Spring / AuraFX

Dark/light mode

Smooth transitions

🏗 Tech Stack
Layer	Technology
Framework	Next.js 15 (App Router)
Runtime	Bun
UI	React 19 + Tailwind CSS 4
State	TanStack Query + React Context
Forms	React Hook Form + Valibot
Blockchain	Viem, Wagmi, RainbowKit
Solana	Helius, @solana/web3.js
DAO	Snapshot, Tally
Hosting	Vercel Edge Network
📦 Installation
sh
bun install
bun dev
Production build:

sh
bun run build
📁 Repository Structure
Code
src/
├── app/                # Next.js App Router
│   ├── api/            # Serverless API routes
│   ├── [user]/         # Profile pages
│   ├── leaderboard/    # Leaderboard
│   ├── swipe/          # Swipe UX
│   ├── team/           # Team page
│   ├── manifest.ts     # PWA manifest
│   ├── robots.ts       # robots.txt
│   └── sitemap.ts      # sitemap.xml
│
├── components/         # UI components
├── lib/                # Core libraries (redis, wagmi, viem, integrations)
├── utils/              # Helpers & utilities
├── data/               # CSV datasets
└── hooks/              # React hooks
📚 Documentation
Full documentation lives in:

Code
/docs
Key entries:
📘 ARCHITECTURE.md — High‑level system architecture

🧩 ARCHITECTURE_FULL_SPECS.md — Low‑level technical specs

🧠 specs/data-models.md — Canonical data contracts

🔌 integrations/ — Farcaster, Lens, Zora, Snapshot, Tally

🛠 api/ — API reference

⚙️ workflows/ — CI/CD, governance, release process

🔌 API Overview
The platform exposes a full suite of serverless API routes:

👤 Profile
Code
GET /api/profile/[address]
POST /api/profile/claim
💰 Wallet
Code
GET /api/wallet/[address]/tokens
GET /api/wallet/[address]/nfts
GET /api/wallet/[address]/transactions
🟣 Social
Code
GET /api/social/farcaster/[fid]
GET /api/social/lens/[handle]
GET /api/social/zora/[address]
🏛 DAO
Code
GET /api/dao/[address]/memberships
GET /api/dao/[address]/activity
🔍 Search
Code
GET /api/search?q=...
Full API documentation is in:

Code
docs/api/
🧪 CI/CD Pipeline
Every PR must pass:

Type checking

Linting

Tests

Build verification

Docs build

Security scan

AI review (advisory)

Deployment is automatic on merge to main.

Full workflow docs:

Code
docs/workflows/
🛡 Security
SIWE authentication

Rate limiting

Input validation

Secret scanning

External API safety checks

Zero‑trust architecture

🤝 Contributing
We follow a strict governance model:

Additive‑only changes unless approved

No silent logic removal

All features must include documentation

All API routes must define typed contracts

CI must remain green

See:

Code
docs/workflows/release-process.md
⭐ Roadmap
🔮 AI‑powered profile insights

🧠 On‑chain reputation scoring

🧵 Farcaster Frames v2 integration

📊 Portfolio analytics dashboard

🪩 Creator economy insights

🧭 DAO discovery engine

🛠 Maintainers
SMSDAO / Ethereum Follow Protocol  
Built with ❤️ by the SMSDAO ecosystem.

📜 License
MIT License.


This document defines the **canonical release workflow** for the SMSDAO Social Portfolio Platform.  
It mirrors the governance and CI discipline used in your other ecosystem repos (e.g. CyberAi).

##  Release Principles

- **Deterministic:** Same inputs → same build → same behavior.
- **Additive‑first:** Prefer additive changes; removals require explicit justification.
- **Documented:** Every meaningful change must be reflected in `docs/`.
- **Guarded:** Protected branches are only updated via PRs with passing checks.
- **Reversible:** Every release must be traceable and roll‑backable.

##  Checklist for Every Release

Before merging into `main`, confirm:

- [ ] All required CI checks are green
- [ ] Docs updated (`docs/` where relevant)
- [ ] No unreviewed breaking changes
- [ ] No stray debug logs or test code
- [ ] Contracts and APIs remain consistent
- [ ] Rollback path is clear (previous `main` commit)

This process is the **source of truth** for how changes move from idea → code → production in this repo.
