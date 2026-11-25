---
title: Kovanica Protocol — Master Presentation Hub
aliases:
  - Kovanica MOC
  - Home
tags:
  - hub
  - kovanica
  - kvnc
status: live-testnet
mainnet_launch: 2027-01-01
sdk_version: 0.9.0
---

# Kovanica Protocol (KVNC) — Master Presentation Hub

> [!IMPORTANT] Three Ways to Explore This Vault
> 1. **Interactive Board (Canvas):** Open [[Kovanica Architecture & Ecosystem.canvas]] for the visual architecture map with embedded live notes and value-flow arrows.
> 2. **Bubble Graph (Graph View):** Press `Ctrl+G` (or click **Open graph view**) — pre-configured in `.obsidian/graph.json` with Kovanica brand colors (Gold = Hub/Tokenomics, Blue = L1/Consensus/Mining, Teal = DeFi/RWA, Purple = Apps/SDK/Playground, Emerald = Web/Revenue, Coral = Security/Roadmap).
> 3. **Slide Deck Presentation:** Open [[Kovanica Pitch Deck (Slides)]] and run **Slides: Start presentation** (`Ctrl+P` → `Slides`).

---

## Executive Snapshot

| Dimension | Canonical Value |
| :--- | :--- |
| **Protocol** | **Kovanica (KVNC)** — from-scratch Rust Layer-1 |
| **Consensus** | **Hybrid PoW + GHOSTDAG** (`KovanicaHash`, `K=5`, `4s` target block time, **zero stake on consensus**) |
| **Smart Contracts** | Deterministic **Wasmi** WebAssembly runtime |
| **Address Standard** | **PRO-21** (`kvnc` + 57 base32 chars + `dag`, 64 chars, 29-bit BLAKE3 checksum) |
| **Live Testnet** | Chain ID `2` · Tag `2-24cdb5fadd98b207` · `https://testnet.kovanica.online` |
| **Mainnet Launch** | Chain ID `1` · Tag `1-f35df34c92001436` · **1.1.2027** (audit-frozen RC) |
| **TypeScript SDK** | `kovanica-sdk v0.9.0` |
| **Public Web Hub** | `https://kovanica.online` (37 routes, 5 pure function tabs, zero tracking cookies) |

---

## Knowledge Graph Map

### 1. Core Layer-1 Protocol
- [[01 - Consensus & L1 Architecture]] — Hybrid PoW + GHOSTDAG (`K=5`, `4s`), Wasmi runtime, 2–4 GB VPS footprint
- [[02 - Tokenomics & Frozen Emission]] — `2.5 KVNC` initial subsidy, `8,200,000` blocks/era, `3/4` geometric decay, `3/4` fee burn
- [[03 - PRO-21 Address & Cryptography]] — Ed25519 + 29-bit BLAKE3, P-256 passkeys, ML-DSA-65 post-quantum verification
- [[10 - Mining Pool & Stratum V1 TLS]] — Encrypted Stratum V1 TLS, VarDiff, graceful drain, `MinerCommandBuilder`

### 2. Application Layer (Wave A–D, DeFi & RWA)
- [[04 - Wave A-D Protocol Features]] — Atomic 1-tx batches, EIP-1559 base fee, WebAuthn passkeys, scheduler, BTC/Solana/EVM bridge
- [[05 - DeFi, AMM & KVP-106 RWA]] — Native AMM `/swap` & `/pools`, KVP-106 RWA Registry `/rwa`, `/wallet/rwa-issue`, `/wallet/rwa-manage`

### 3. Five-Repository Ecosystem & Surfaces
- [[06 - Five-Repository Ecosystem]] — `kovanica-l1`, `kovanica-sdk`, `kovanica-web`, `kovanica-apps`, `kovanica-playground`
- [[07 - Web Properties & 5-Tab IA]] — `Explore · Trade · Assets · Wallet · Build`, 37 routes, cross-subdomain Ecosystem Switcher
- [[08 - Client Applications & Browser Extension]] — `wallet-web`, MV3 `browser-extension` (`window.kovanica`), `console-desktop`, `node-desktop`, Android & iOS
- [[09 - Developer SDK & Playground]] — `kovanica-sdk v0.9.0`, failover RPC/WS, 4-group developer console

### 4. Business, Revenue & Mainnet Governance
- [[11 - Revenue & Non-Token Monetization]] — 6 non-token revenue streams live on `/pricing` + `POST /api/inquiries` (zero tracking cookies)
- [[12 - Security, Audit & Mainnet 1.1.2027]] — Audit-freeze discipline, PR-only workflow, Chain ID isolation, launch checklist

---

## Live Ecosystem Links

- **Apex Landing:** [kovanica.online](https://kovanica.online)
- **Testnet Portal:** [testnet.kovanica.online](https://testnet.kovanica.online)
- **Documentation:** [docs.kovanica.online](https://docs.kovanica.online)
- **Built-in Playground:** [playground.kovanica.online](https://playground.kovanica.online)
- **Dashboard:** [dash.kovanica.online](https://dash.kovanica.online)
- **Pricing & Services:** [testnet.kovanica.online/pricing](https://testnet.kovanica.online/pricing)
- **Public Testnet RPC:** `https://rpc-testnet.kovanica.online/rpc`
- **GitHub Organization:** [github.com/BetterCallDzuks](https://github.com/BetterCallDzuks)
