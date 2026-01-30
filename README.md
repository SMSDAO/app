⚡ The Social Portfolio Platform for On‑Chain Identity, Social Graphs & DAO Intelligence
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
📦 Installation:

bun install
bun dev
bun run build

📁 Repository Structure:
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
/docs

Key entries:
📘 ARCHITECTURE.md — High‑level system architecture

🧩 ARCHITECTURE_FULL_SPECS.md — Low‑level technical specs

🧠 specs/data-models.md — Canonical data contracts

🔌 integrations/ — Farcaster, Lens, Zora, Snapshot, Tally

🛠 api/ — API reference

⚙️ workflows/ — CI/CD, governance, release process

API Overview
👤 Profile
GET /api/profile/[address]
POST /api/profile/claim

Wallet:
GET /api/wallet/[address]/tokens
GET /api/wallet/[address]/nfts
GET /api/wallet/[address]/transactions

🟣 Social:
GET /api/social/farcaster/[fid]
GET /api/social/lens/[handle]
GET /api/social/zora/[address]

🏛 DAO
GET /api/dao/[address]/memberships
GET /api/dao/[address]/activity

🔍 Search
GET /api/search?q=...
Full API documentation: docs/api/

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

Full workflow docs: docs/workflows/

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
