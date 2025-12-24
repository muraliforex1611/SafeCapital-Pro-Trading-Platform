# SafeCapital Pro Trading Platform

**AI-Powered Forex Trading Platform for Indian Traders**

## Overview

SafeCapital Pro is a comprehensive forex trading platform that combines:
- 🤖 AI-powered trade signals (Claude AI)
- 📊 Real-time market analysis
- 🛡️ 8-layer capital protection system
- 📈 Automated trading with MT4/MT5
- 🇮🇳 Built specifically for Indian traders

## Tech Stack

### Frontend
- Next.js 14 (React framework)
- TypeScript
- Tailwind CSS (styling)
- Framer Motion (animations)
- Socket.io Client (real-time updates)

### Backend
- Node.js with Express
- TypeScript
- PostgreSQL (Supabase)
- Redis (Upstash)
- Socket.io (WebSocket server)

### AI & Integrations
- Anthropic Claude API
- MetaTrader 4/5 API
- Razorpay (payments)
- SendGrid (email)

## Project Status

**Phase:** Foundation & Setup
**Week:** 1
**Started:** December 24, 2025
**Target Launch:** April 2026 (16 weeks)

## Development Timeline

- **Weeks 1-4:** Foundation (Architecture, DB, API, MT4 integration)
- **Weeks 5-8:** Signal Detection & AI (FVG/BOS algorithm, Claude AI)
- **Weeks 9-12:** Testing & Polish (90%+ coverage, capital protection)
- **Weeks 13-14:** Beta Testing (50 users)
- **Weeks 15-16:** Deployment & Launch

## Quick Start

### Prerequisites
- Node.js v20+
- Supabase account (PostgreSQL)
- Upstash account (Redis)
- Claude API key

### Installation

```bash
# Clone repository
git clone <your-repo-url>

# Install frontend dependencies
cd frontend
npm install

# Install backend dependencies
cd ../backend
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your credentials
```

### Run Development Servers

```bash
# Terminal 1 - Backend
cd backend
npm run dev

# Terminal 2 - Frontend
cd frontend
npm run dev
```

Access the app at: http://localhost:3000

## Project Structure

```
SafeCapital-Pro-Trading/
├── frontend/              # Next.js frontend application
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── pages/         # Next.js pages (routes)
│   │   ├── styles/        # Global styles
│   │   ├── lib/           # Utilities and helpers
│   │   ├── hooks/         # Custom React hooks
│   │   ├── types/         # TypeScript type definitions
│   │   └── utils/         # Utility functions
│   └── public/            # Static assets
│
├── backend/               # Node.js backend API
│   ├── src/
│   │   ├── routes/        # API routes
│   │   ├── controllers/   # Request handlers
│   │   ├── services/      # Business logic
│   │   ├── models/        # Database models
│   │   ├── middleware/    # Express middleware
│   │   ├── utils/         # Utility functions
│   │   └── types/         # TypeScript types
│   └── tests/             # Backend tests
│
├── database/              # Database files
│   ├── migrations/        # SQL migration files
│   └── seeds/             # Test data seeds
│
├── docs/                  # Documentation
│   ├── PDR.md            # Product Design Requirements
│   ├── PLAYBOOK.md       # Operations Manual
│   └── API.md            # API Documentation
│
├── scripts/               # Automation scripts
│   ├── deployment/        # Deployment scripts
│   └── testing/           # Test automation
│
└── config/                # Configuration files
```

## Key Features (Roadmap)

### Phase 1 - MVP (Weeks 1-8)
- [x] Project setup
- [ ] User authentication (JWT)
- [ ] Real-time dashboard
- [ ] MT4/MT5 integration
- [ ] Signal detection (FVG + BOS)
- [ ] Claude AI integration
- [ ] Multi-channel alerts

### Phase 2 - Testing (Weeks 9-12)
- [ ] Comprehensive testing (90%+ coverage)
- [ ] Capital protection system
- [ ] Performance optimization
- [ ] Security audit

### Phase 3 - Beta (Weeks 13-14)
- [ ] Beta user program (50 users)
- [ ] Feedback collection
- [ ] Bug fixes and refinements

### Phase 4 - Launch (Weeks 15-16)
- [ ] Production deployment
- [ ] Payment integration (Razorpay)
- [ ] Public launch
- [ ] Marketing campaign

## Revenue Model

### Pricing Tiers
- **Basic (₹999/month):** AI signals only
- **Trader (₹2,999/month):** Signals + Auto trading
- **Pro (₹9,999/month):** Full suite + AI agent

### Year 1 Targets
- Month 3: 60 users, ₹1.9 lakhs revenue
- Month 6: 200 users, ₹6+ lakhs revenue
- Month 12: 400 users, ₹12+ lakhs revenue

## Contributing

This is a private project. For questions or issues, contact the development team.

## License

Proprietary - All rights reserved

## Support

- Documentation: `/docs`
- Issues: GitHub Issues
- Email: support@safecapitalpro.com (coming soon)

---

**Built with ❤️ for Indian Forex Traders**
