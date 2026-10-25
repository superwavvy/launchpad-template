# Launchpad Template

A production-ready, white-label launchpad frontend for Solana tokens. It provides teams with a secure, pre-built interface to launch SPL tokens, handle trust scoring, and display live analytics.

## The Problem

Launching a token on Solana requires integrating with multiple complex protocols for liquidity, security scoring, and data indexing. Building a reliable frontend for this takes weeks. This template solves that by providing a battle-tested UI and backend integration out of the box.

## Features

- **Token Creation:** Direct integration with SPL Token program for Devnet token creation.
- **Trust Scoring:** On-chain analytics to evaluate token health and deployer history.
- **Market Data:** Curated feeds from DexScreener to show live price and volume.
- **Analytics:** Custom Solana indexer for tracking holder growth and transaction volume.

## Architecture

- **Frontend:** Next.js (App Router) and Tailwind CSS.
- **Blockchain:** Solana Web3.js and SPL Token.
- **Indexer:** Helius API for real-time transaction parsing and webhooks.
- **Database:** Supabase (PostgreSQL) for token metadata and caching.
- **Data Provider:** DexScreener API for market pricing.

## Quick Start

### 1. Clone the repository

```bash
git clone git@github.com:superwavvy/launchpad-template.git
cd launchpad-template
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

```bash
cp .env.example .env
```

Populate the `.env` file with your `HELIUS_API_KEY`, `SUPABASE_URL`, and `SUPABASE_ANON_KEY`.

### 4. Run the development server

```bash
npm run dev
```

## Limitations

The template is currently configured for Solana Devnet to prevent accidental mainnet deployments during testing. Before moving to production, the RPC endpoints and SPL Token program IDs must be updated to Mainnet-Beta.
