---
title: Web Properties & 5-Tab IA
tags:
  - web
  - ux
repo: BetterCallDzuks/kovanica-web
routes: 38
---

# 07 · Web Properties & 5-Tab IA

Back to [[00 - Kovanica Protocol MOC]] · See [[Kovanica Architecture & Ecosystem.canvas]]

## Live Subdomains (`kovanica.online`)

| Subdomain | Role | Status |
| :--- | :--- | :--- |
| `https://kovanica.online` | Apex Landing (`LandingChrome`) & `/privacy` | Live (`200`) |
| `https://testnet.kovanica.online` | Primary Testnet Hub (`Shell` · 38 routes) | Live (`200`) |
| `https://docs.kovanica.online` | Protocol Documentation (`/docs`) | Live (`200`) |
| `https://playground.kovanica.online` | Built-in Playground (`/playground`) | Live (`200`) |
| `https://dash.kovanica.online` | Network Dashboard (`/dash`) | Live (`200`) |
| `https://rpc-testnet.kovanica.online/rpc` | Public Testnet JSON-RPC (Chain `2`) | Live (`200`) |
| `https://mainnet.kovanica.online` | Mainnet Gate (`1.1.2027`, Let's Encrypt TLS) | Live TLS (`200` · Launching) |

## 5 Standardized Pure Function Tabs

A single-source-of-truth `NAV_GROUPS` in `Shell` (shared with `HomeTestnet` and the Mobile More sheet) keeps every route ≤ 2 clicks away with zero duplicate labels:

1. **Explore:** `Explorer` (left-to-right multi-lane BlockDAG card graph with plain-English colour legend, directional merge/fork arrows & hover tooltips), `Network`, `Mining Pool` (`/pool`), `Origins Map`, `Dashboard`, `Roadmap`
2. **Trade:** `Swap` (`/swap`), `Liquidity Pools` (`/pools`), `Orderbook DEX`, `Atomic Swaps`
3. **Assets:** `RWA Registry` (`/rwa`), `Issue RWA`, `Manage RWA`, `Multi-Asset`, `Native NFTs`, `Token Listings`
4. **Wallet:** `Wallet`, `Faucet`, `Airdrops`, `CoinJoin`, `Ecosystem Tools`
5. **Build:** `Multisig`, `HTLC`, `Vaults`, `Stealth`, `Docs`, `API Reference`, `Playground`, `Pricing & Services` (`/pricing`), `Privacy Policy` (`/privacy`)

> [!TIP] Design Preservation
> Every surface preserves Kovanica's dark zinc (`#09090b`), surface (`#121214` / `#1a1a1e`), gold (`#F2A900`), teal (`#2fbaa4`), blue (`#8aa0b4`), and `Fraunces` / `IBM Plex Sans` / `IBM Plex Mono` typography.

## Related Notes
- [[05 - DeFi, AMM & KVP-106 RWA]]
- [[06 - Five-Repository Ecosystem]]
- [[10 - Mining Pool & Stratum V1 TLS]]
- [[11 - Revenue & Non-Token Monetization]]
