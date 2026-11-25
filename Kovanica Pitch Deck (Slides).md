---
title: Kovanica Protocol — Pitch Deck
tags:
  - hub
  - slides
  - kovanica
---

# Kovanica Protocol (KVNC)

**Hybrid PoW + GHOSTDAG Layer-1**
*Fast BlockDAG finality · Deterministic Wasmi Smart Contracts · Institutional KVP-106 RWA*

- **Live Testnet:** `https://testnet.kovanica.online` (Chain ID `2`)
- **Mainnet Launch:** **1.1.2027** (Chain ID `1`, audit-frozen RC)

---

## 1. The Problem

- **Proof-of-Stake centralization:** Validator cartels, slashing complexity, and governance capture.
- **Slow linear PoW:** 10-minute confirmation times and high orphan rates prevent modern DeFi & RWA UX.
- **Fragmented RWA tooling:** Issuers stitch together incompatible contracts, compliance spreadsheets, and multi-tx approval flows.

---

## 2. The Kovanica Architecture

- **Pure Hybrid PoW + GHOSTDAG (`K=5`, `4s` target block time)**
  - **Zero stake on consensus** — no validator committee, no staking cartels.
  - **KovanicaHash** (BLAKE3 + 2 MiB memory mix) — runs lean on 2–4 GB RAM VPS nodes.
  - Non-blue blocks are safely recycled to mempool with **zero transaction loss**.
- **Deterministic Wasmi WebAssembly Runtime**
  - Predictable gas/storage metering with native KVP-102 tokens & KVP-106 RWA primitives.

---

## 3. Frozen Tokenomics (KVNC)

- **Ticker:** `KVNC` (`9` decimals = `1,000,000,000` atoms)
- **Initial Block Reward:** `2.5 KVNC`
- **Subsidy Era:** `8,200,000` blocks per era with **`3/4` geometric decay**
- **Fee Split:** **`3/4` burned** (deflationary pressure) · **`1/4` to miner**
- **EIP-1559 Dynamic Base Fee + Storage Deposit** (Wave B)

---

## 4. Security & PRO-21 Identity

- **PRO-21 Canonical Address:** `kvnc` + 57 base32 chars + `dag` (`64` chars, 29-bit BLAKE3 checksum)
  - Strictly enforced on Mainnet (Chain `1`) and Testnet (Chain `2`) — legacy hex rejected.
- **Modern Cryptography:**
  - Ed25519 native accounts + **P-256 WebAuthn Passkeys** + **ML-DSA-65** post-quantum verification.
  - Air-gap `kvnc-tx:v1:` BLAKE3-checksummed signing envelopes.

---

## 5. Wave A–D Feature Suite

- **Wave A — Atomic Batches:** 1-transaction `Deploy+Call` & `Approve+Swap` / `Approve+AddLiquidity`.
- **Wave B — Fee Market:** Dynamic base fee (`kovanica_getBaseFee`) + storage deposit telemetry.
- **Wave C — Account UX:** WebAuthn passkeys, session keys, on-chain scheduler jobs & keeper unit.
- **Wave D — Interoperability:** BTC, Solana & EVM bridge registry + institutional KVP-106 RWA compliance.

---

## 6. Native DeFi & KVP-106 RWA

- **Native AMM DEX (`/swap`, `/pools`):**
  - Constant-product `x·y=k` swaps, 1-tx Wave A liquidity batches, and on-chain KVP-102 quote calculator.
- **Institutional RWA (`/rwa`, `/wallet/rwa-issue`, `/wallet/rwa-manage`):**
  - Deterministic BLAKE3 asset derivation (`kvp106:rwa:v1`).
  - Built-in allowlists, freeze controls, and automated coupon/dividend scheduling.

---

## 7. Five-Repository Ecosystem

1. **`kovanica-l1`** — Rust L1 node, consensus, Wasmi, RPC, Stratum, Faucet, Indexer, CLI
2. **`kovanica-sdk` (`v0.9.0`)** — TypeScript browser/Node SDK, failover RPC/WS, offline codecs
3. **`kovanica-web`** — Public portal (`kovanica.online`), 37 routes, 5 pure function tabs
4. **`kovanica-apps`** — `wallet-web`, MV3 `browser-extension` (`window.kovanica`), Desktop & Mobile
5. **`kovanica-playground`** — Interactive RPC console & 4-group developer studio

---

## 8. Unified Web Experience (`kovanica.online`)

**5 Pure Function Tabs** across every route (zero duplicates, zero tracking cookies):

- **Explore:** Explorer (8 tabs), Network, Mining Pool (`/pool`), Origins Map, Dashboard, Roadmap
- **Trade:** Swap (`/swap`), Liquidity Pools (`/pools`), Orderbook DEX, Atomic Swaps
- **Assets:** RWA Registry (`/rwa`), Issue RWA, Manage RWA, Multi-Asset, Native NFTs, Token Listings
- **Wallet:** Web Wallet, Faucet, Airdrops, CoinJoin, Ecosystem Tools
- **Build:** Multisig, HTLC, Vaults, Stealth, Docs, API Reference, Playground, Pricing & Services

---

## 9. Non-Token Revenue Model (`/pricing`)

Six sustainable revenue streams **independent of KVNC token price**:

1. **Managed RPC, WebSocket & Indexer SaaS** (`$49–$249/mo` + Dedicated SLA)
2. **RWA Issuer & Compliance SaaS** (`$299–$999/mo` + White-Label)
3. **Front-End Swap / Bridge Interface Fee** (`0%` testnet · configurable for mainnet)
4. **Official Stratum V1 TLS Mining Pool** (`0%` testnet · `1.0%` planned mainnet)
5. **Verified Listings & Zero-Cookie Sponsorships** (`$250–$500` reviews · `$400/mo` static slots)
6. **Exchange & Enterprise Integration Support** (custom deployments & SDK retainers)

---

## 10. Roadmap to Mainnet `1.1.2027`

- **Now (Live on Testnet Chain 2):**
  - Full L1 + Wasmi + Wave A–D + MV3 Browser Extension + 37-route Web Portal + `/pricing` live on VPS.
- **Pre-Mainnet Gate:**
  - External cryptographic & consensus security audit of `kovanica-l1` (`v1.0.0-mainnet` freeze).
  - 3-node bridge & Stratum TLS dress rehearsals.
- **T0 Genesis (`1.1.2027`):**
  - Mainnet Chain `1` (`1-f35df34c92001436`) activation.

---

## Thank You — Explore Live

- **Web Portal:** `https://kovanica.online`
- **Testnet Hub:** `https://testnet.kovanica.online`
- **Pricing & Services:** `https://testnet.kovanica.online/pricing`
- **GitHub:** `https://github.com/BetterCallDzuks`

*Press `Esc` to exit presentation and inspect [[00 - Kovanica Protocol MOC]] or [[Kovanica Architecture & Ecosystem.canvas]].*
