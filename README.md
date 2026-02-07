# Social Portfolio Platform

[![Deploy](https://github.com/SMSDAO/app/workflows/Deploy/badge.svg)](https://github.com/SMSDAO/app/actions)
[![Test](https://github.com/SMSDAO/app/workflows/Test/badge.svg)](https://github.com/SMSDAO/app/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> **The comprehensive platform for Web3 identity, social graphs, and DAO intelligence.**

The Social Portfolio Platform aggregates on-chain identity, multi-chain portfolios, social activity, and DAO governance participation into a unified, searchable profile system. Built on Next.js 15 with React 19, optimized for performance and discoverability.

## ✨ Overview

- **Unified Identity**: ENS resolution, multi-chain addresses, SIWE authentication, customizable profiles
- **Portfolio Intelligence**: Real-time token balances, NFT galleries, transaction history, performance analytics
- **Social Integration**: Farcaster casts, Lens publications, Zora creations in one timeline
- **DAO Analytics**: Snapshot/Tally governance, voting power, delegation tracking, participation metrics
- **Search & Discovery**: SEO-optimized profiles, searchable by address/ENS/handle
- **Modern UI**: Neo Glow design system with AuraFX animations, Tailwind CSS 4, dark/light themes

## 🚀 Features

### 🧬 Unified On-Chain Identity

- **ENS Resolution**: Automatic ENS name resolution and reverse lookup
- **Multi-Chain Support**: Ethereum, Polygon, Arbitrum, Optimism, Base, Solana
- **Profile Claiming**: Sign-in with Ethereum (SIWE) for secure profile ownership
- **Rich Metadata**: Avatar, bio, badges, social links, verification status

### 💰 Portfolio Intelligence

- **Token Tracking**: Real-time balances across multiple chains with USD valuations
- **NFT Gallery**: Rich metadata display with collection grouping and rarity indicators
- **Transaction History**: Comprehensive activity timeline with categorization (send, receive, swap, mint)
- **Performance Metrics**: Portfolio value charts, ROI calculations, asset allocation breakdowns

### 🟣 Social Graph Integrations

- **Farcaster**: Profile data, casts, reactions, followers/following, channel membership
- **Lens Protocol**: Publications, collects, mirrors, social connections
- **Zora**: Minted NFTs, created collections, edition details, minting activity

### 🏛 DAO Governance Analytics

- **Snapshot**: Space memberships, proposal voting, voting power tracking
- **Tally**: On-chain governance participation, delegation management
- **Analytics**: Capital flow visualization, participation rates, voting history

### 🔍 Search & Discovery

- **Universal Search**: Find profiles by wallet address, ENS name, Lens handle, Farcaster username
- **SEO Optimization**: Structured data, Open Graph tags, auto-generated sitemaps
- **Background Indexing**: Automated portfolio updates and search engine pings

### 🎨 Neo Glow Design System

- **Modern UI**: Gradient effects, glassmorphism, smooth animations
- **AuraFX**: React Spring-powered transitions and interactions
- **Tailwind CSS 4**: Utility-first styling with custom design tokens
- **Theme Support**: Seamless dark/light mode with `next-themes`

## 🏗 Tech Stack

### Core Technologies

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Framework** | Next.js 15 (App Router) | Server-side rendering, routing, API routes |
| **Runtime** | Bun | Fast JavaScript runtime and package manager |
| **UI Framework** | React 19 | Component-based user interface |
| **Styling** | Tailwind CSS 4 | Utility-first CSS framework |
| **State Management** | TanStack Query | Server state management and caching |
| **Forms** | React Hook Form + Valibot | Form handling and validation |
| **Animations** | React Spring / AuraFX | Smooth transitions and interactions |
| **Theme** | next-themes | Dark/light mode support |

### Blockchain Integrations

| Chain | Technology | Purpose |
|-------|-----------|---------|
| **Ethereum/EVM** | Viem, Wagmi, RainbowKit | Blockchain interactions, wallet connection |
| **Indexing** | Alchemy | Token balances, NFTs, transactions |
| **Solana** | @solana/web3.js, Helius | Solana blockchain and NFT data |

### Social & DAO APIs

| Platform | Purpose |
|----------|---------|
| **Farcaster** | Social activity, casts, reactions |
| **Lens Protocol** | Publications, collects, social graph |
| **Zora** | NFT creations and minting activity |
| **Snapshot** | Off-chain governance voting |
| **Tally** | On-chain governance tracking |

### Infrastructure

| Service | Purpose |
|---------|---------|
| **Hosting** | Vercel Edge Network |
| **Monitoring** | Sentry |
| **Analytics** | Vercel Analytics |
| **CI/CD** | GitHub Actions |
## 📦 Quick Start

### Prerequisites

- **Bun**: Latest version (`curl -fsSL https://bun.sh/install | bash`)
- **Node.js**: v20.x LTS or higher
- **Git**: Latest version

### Installation

```bash
# Clone the repository
git clone https://github.com/SMSDAO/app.git
cd app

# Install dependencies
bun install

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys

# Start development server
bun dev
```

The application will be available at `http://localhost:3443`.

### Essential Commands

```bash
# Development
bun dev              # Start dev server on port 3443

# Building
bun run build        # Build for production
bun start            # Start production server

# Code Quality
bun lint             # Run ESLint
bun format           # Format with Prettier
bun typecheck        # TypeScript type checking
bun check            # Run all checks (lint + format + typecheck + build)

# Maintenance
bun clean            # Clean build artifacts
```

## 🗂 Project Structure

```
app/
├── src/
│   ├── app/                    # Next.js App Router
│   │   ├── api/                # API routes (serverless functions)
│   │   ├── [user]/             # Dynamic profile pages
│   │   ├── leaderboard/        # Leaderboard page
│   │   ├── swipe/              # Swipe interface
│   │   ├── team/               # Team page
│   │   ├── manifest.ts         # PWA manifest
│   │   ├── robots.ts           # robots.txt generator
│   │   └── sitemap.ts          # Dynamic sitemap
│   │
│   ├── components/             # React components
│   │   ├── ui/                 # Reusable UI components
│   │   ├── wallet/             # Wallet connection components
│   │   ├── social/             # Social feed components
│   │   └── dao/                # DAO analytics components
│   │
│   ├── lib/                    # Core libraries & integrations
│   │   ├── wagmi/              # Wagmi configuration
│   │   ├── viem/               # Viem utilities
│   │   └── redis/              # Redis/cache utilities
│   │
│   ├── hooks/                  # Custom React hooks
│   ├── utils/                  # Helper functions
│   └── data/                   # Static data & CSV datasets
│
├── docs/                       # Documentation
│   ├── ARCHITECTURE.md         # System architecture
│   ├── FEATURES.md            # Feature specifications
│   ├── API.md                 # API documentation
│   ├── CONTRIBUTING.md        # Contribution guidelines
│   ├── DEPLOYMENT.md          # Deployment guide
│   ├── WORKFLOWS.md           # CI/CD workflows
│   ├── MONITORING.md          # Monitoring & observability
│   └── SEO.md                 # SEO strategy
│
├── public/                     # Static assets
├── .github/                    # GitHub Actions workflows
└── sentry.*.config.ts          # Sentry error tracking
```

## 🔌 API Overview

The platform provides comprehensive APIs for profiles, wallets, social integrations, and DAO analytics.

### Profile APIs

```bash
# Get profile data
GET /api/profile/[address]

# Claim profile with wallet signature
POST /api/profile/claim
```

### Wallet APIs

```bash
# Get token balances across chains
GET /api/wallet/[address]/tokens?chains=ethereum,polygon

# Get NFT collection
GET /api/wallet/[address]/nfts

# Get transaction history
GET /api/wallet/[address]/transactions
```

### Social APIs

```bash
# Farcaster profile and casts
GET /api/social/farcaster/[fid]

# Lens Protocol profile
GET /api/social/lens/[handle]

# Zora creations and mints
GET /api/social/zora/[address]
```

### DAO APIs

```bash
# Get DAO memberships
GET /api/dao/[address]/memberships

# Get governance activity
GET /api/dao/[address]/activity
```

### Search API

```bash
# Universal search
GET /api/search?q=vitalik&type=profile
```

**Full API documentation**: [docs/API.md](docs/API.md)

## 🏛 Architecture

The platform uses a modern, serverless architecture built on Next.js 15 with the App Router pattern.

### High-Level Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        Client Layer                          │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │  Next.js 15  │  │  React 19    │  │  TailwindCSS │      │
│  │  App Router  │  │  Components  │  │  Styling     │      │
│  └──────────────┘  └──────────────┘  └──────────────┘      │
└─────────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                    Application Layer                         │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │   API Routes │  │  Server      │  │  Middleware  │      │
│  │              │  │  Components  │  │              │      │
│  └──────────────┘  └──────────────┘  └──────────────┘      │
└─────────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                   Integration Layer                          │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │  Blockchain  │  │   Social     │  │     DAO      │      │
│  │   APIs       │  │   APIs       │  │    APIs      │      │
│  └──────────────┘  └──────────────┘  └──────────────┘      │
│                                                              │
│  • Viem/Wagmi (Ethereum)    • Farcaster API                 │
│  • Solana Web3.js           • Lens Protocol                 │
│  • Alchemy/Helius           • Zora API                      │
│  • RainbowKit               • Snapshot API                  │
└─────────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                      Data Layer                              │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │   Cache      │  │   Indexing   │  │  On-Chain    │      │
│  │  (Browser)   │  │   Workers    │  │    Data      │      │
│  └──────────────┘  └──────────────┘  └──────────────┘      │
└─────────────────────────────────────────────────────────────┘
```

### Key Architecture Principles

- **Server Components First**: Default to server-side rendering for optimal performance
- **Edge Computing**: Leverage Vercel Edge Network for global distribution
- **Caching Strategy**: Multi-layer caching (browser, TanStack Query, API, on-chain)
- **Code Splitting**: Route-based and dynamic component loading
- **Type Safety**: End-to-end TypeScript with strict mode

**Detailed architecture**: [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md)

## 🔐 Environment Variables

Create a `.env` file based on `.env.example`:

```bash
# Application
NEXT_PUBLIC_APP_URL=http://localhost:3443
NODE_ENV=development

# Wallet Connect
NEXT_PUBLIC_WALLET_CONNECT_PROJECT_ID=your_project_id

# Blockchain APIs
ALCHEMY_API_KEY=your_alchemy_key
HELIUS_API_KEY=your_helius_key

# Social Platform APIs
FARCASTER_API_KEY=your_farcaster_key
LENS_API_KEY=your_lens_key
ZORA_API_KEY=your_zora_key

# DAO APIs
SNAPSHOT_API_KEY=your_snapshot_key
TALLY_API_KEY=your_tally_key

# Monitoring (Optional)
SENTRY_DSN=your_sentry_dsn
SENTRY_AUTH_TOKEN=your_sentry_auth_token

# Analytics (Optional)
NEXT_PUBLIC_GOOGLE_ANALYTICS=your_ga_id
VERCEL_ANALYTICS_ID=your_vercel_analytics_id
```

See `.env.example` for a complete list of environment variables.

## 🧪 Development Workflow

### Code Quality Standards

```bash
# Before committing
bun lint              # Check for code issues
bun format            # Format code
bun typecheck         # Verify types
bun check             # Run all checks + build

# Fix issues automatically
bun fix               # Run lint and format with auto-fix
```

### Component Development

- Use **TypeScript** for all new code
- Follow **React 19** best practices (Server Components by default)
- Write **JSDoc comments** for complex functions
- Use **Tailwind CSS** for styling (utility-first approach)
- Implement **proper error boundaries** for robustness

### Testing Best Practices

While there's no test infrastructure currently, follow these guidelines when tests are added:
- Write unit tests for utilities and hooks
- Write integration tests for API routes
- Aim for 80%+ code coverage on critical paths

### Git Workflow

```bash
# Create feature branch
git checkout -b feature/your-feature

# Make changes and commit
git add .
git commit -m "feat(scope): description"

# Push and create PR
git push origin feature/your-feature
```

Follow [Conventional Commits](https://www.conventionalcommits.org/) format:
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` Code style changes
- `refactor:` Code refactoring
- `test:` Adding tests
- `chore:` Maintenance tasks
## 🚀 Deployment

### Vercel (Recommended)

The application is optimized for deployment on Vercel:

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy to preview
vercel

# Deploy to production
vercel --prod
```

Vercel automatically deploys when you push to:
- **Preview**: All pull requests
- **Production**: Main branch

### Self-Hosted

For self-hosted deployments, see the comprehensive guide in [docs/DEPLOYMENT.md](docs/DEPLOYMENT.md).

### CI/CD Pipeline

Every PR must pass:
- ✅ Type checking (TypeScript)
- ✅ Linting (ESLint)
- ✅ Code formatting (Prettier)
- ✅ Build verification
- ✅ Documentation validation
- ✅ Security scanning

Deployment is automatic on merge to `main`.

**Full workflow documentation**: [docs/WORKFLOWS.md](docs/WORKFLOWS.md)

## 🛡 Security & Best Practices

### Authentication & Authorization

- **SIWE (Sign-In with Ethereum)**: Wallet-based authentication
- **Session Management**: Secure HTTP-only cookies
- **CSRF Protection**: Built-in Next.js protections
- **Input Validation**: Valibot schema validation on all inputs

### Rate Limiting

- API endpoints: 100 requests/minute per IP
- Burst protection: 10 requests/second
- Automatic throttling on suspicious activity

### Data Protection

- **Environment Variables**: Never commit secrets
- **API Key Rotation**: Regular rotation recommended
- **Sanitization**: All user input sanitized before rendering
- **Security Headers**: Strict CSP, HSTS, X-Frame-Options

### Monitoring & Observability

- **Error Tracking**: Sentry integration for all environments
- **Performance Monitoring**: Core Web Vitals tracking
- **Health Checks**: `/api/health` endpoint for uptime monitoring
- **Logging**: Structured logging with Pino

**Monitoring guide**: [docs/MONITORING.md](docs/MONITORING.md)

## 📊 Performance

### Optimization Strategies

- **Server Components**: Reduced client-side JavaScript
- **Code Splitting**: Automatic route-based splitting
- **Image Optimization**: Next.js Image component with AVIF/WebP
- **Caching**: Multi-layer caching strategy (browser, query, API)
- **Edge Runtime**: Global distribution via Vercel Edge Network

### Performance Targets

- **LCP** (Largest Contentful Paint): < 2.5s
- **FID** (First Input Delay): < 100ms
- **CLS** (Cumulative Layout Shift): < 0.1
- **TTFB** (Time to First Byte): < 800ms

## 🔍 SEO Optimization

The platform is optimized for search engine discovery:

- **Dynamic Meta Tags**: Per-profile Open Graph and Twitter Cards
- **Structured Data**: JSON-LD schema markup for profiles
- **Sitemap Generation**: Automatic sitemap updates
- **Search Engine Pings**: Auto-submission to Google, Bing, IndexNow
- **Robots.txt**: Configured for optimal crawling

**SEO strategy**: [docs/SEO.md](docs/SEO.md)

## 🤝 Contributing

We welcome contributions from the community! Please follow these guidelines:

### Contribution Requirements

- **Additive-only changes** unless explicitly approved by maintainers
- **No silent logic removal** - all changes must be documented
- **Documentation required** for all new features
- **Type contracts** must be defined for all API routes
- **CI must remain green** - all checks must pass

### How to Contribute

1. **Fork the repository** and create a feature branch
2. **Read the guidelines**: [docs/CONTRIBUTING.md](docs/CONTRIBUTING.md)
3. **Make your changes** following the code style
4. **Write tests** if adding new functionality
5. **Submit a PR** with a clear description of changes
6. **Address review feedback** from maintainers

### Governance Model

We follow a strict governance model to ensure code quality and maintainability. All contributions are reviewed by core maintainers before merging.

**Full contribution guide**: [docs/CONTRIBUTING.md](docs/CONTRIBUTING.md)

## 📚 Documentation

Comprehensive documentation is available in the `/docs` directory:

- **[ARCHITECTURE.md](docs/ARCHITECTURE.md)**: System architecture and design patterns
- **[FEATURES.md](docs/FEATURES.md)**: Detailed feature specifications
- **[API.md](docs/API.md)**: Complete API reference and integration guides
- **[CONTRIBUTING.md](docs/CONTRIBUTING.md)**: Contribution guidelines and workflows
- **[DEPLOYMENT.md](docs/DEPLOYMENT.md)**: Deployment instructions for various platforms
- **[WORKFLOWS.md](docs/WORKFLOWS.md)**: CI/CD pipeline and GitHub Actions
- **[MONITORING.md](docs/MONITORING.md)**: Monitoring, logging, and observability
- **[SEO.md](docs/SEO.md)**: SEO strategy and implementation

## ⭐ Roadmap

Planned features and improvements:

- 🔮 **AI-powered profile insights**: Intelligent analysis of on-chain behavior
- 🧠 **On-chain reputation scoring**: Verifiable reputation system
- 🧵 **Farcaster Frames v2 integration**: Enhanced frame interactions
- 📊 **Portfolio analytics dashboard**: Advanced analytics and insights
- 🪩 **Creator economy insights**: Track and analyze creator activities
- 🧭 **DAO discovery engine**: Discover and explore DAOs

## 💬 Community & Support

- **Discord**: [Discord Server](https://discord.efp.app) - Join for discussions and support
- **GitHub Discussions**: [Discussions](https://github.com/SMSDAO/app/discussions) - Feature requests and community proposals
- **GitHub Issues**: [Issues](https://github.com/SMSDAO/app/issues) - Bug reports and feature requests
- **Email**: [encrypted@ethfollow.xyz](mailto:encrypted@ethfollow.xyz) - Direct support

🛠 Maintainers
SMSDAO / Ethereum Follow Protocol  
Built with ❤️ by the SMSDAO ecosystem.

📜 License
MIT License.
