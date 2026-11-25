---
title: DeFi, AMM & KVP-106 RWA
tags:
  - defi
  - rwa
---

# 05 · DeFi, AMM & KVP-106 RWA

Back to [[00 - Kovanica Protocol MOC]]

## Native AMM DEX (`Trade` Tab)

- **AMM Swap (`/swap`):** Constant-product `x·y=k` swaps with slippage presets, Wave A 1-tx atomic `Approve → Swap` batches, live Wave B base-fee telemetry, and transparent interface-fee breakdown (`0.00%` on testnet; configurable via `VITE_SWAP_INTERFACE_FEE_BPS`).
- **AMM Liquidity Pools (`/pools`):** Wave A 1-tx `Add Liquidity`, LP share burn/withdrawal, **plus** the on-chain KVP-102 `PoolView` explorer & exact quote calculator (cleanly separated from Stratum Mining Pool `/pool`).
- **Orderbook DEX (`/wallet/dex`) & Atomic Swaps (`/wallet/atomic-swap`):** Reachable in 1 click from the **Trade** tab and contextual Trade sub-nav strip.

## Institutional KVP-106 RWA (`Assets` Tab)

- **Public RWA Registry (`/rwa` & `/explorer/rwa/$assetId`):** Browse verified real-world assets (`RE`, `BOND`, `INVOICE`, `COMMODITY`, `FUND`, `OTHER`) and inspect compliance metadata.
- **Deterministic Issuance (`/wallet/rwa-issue`):** Server-backed `POST /api/rwa/derive` computing exact BLAKE3 `kvp106:rwa:v1` asset IDs matching `kovanica-l1`.
- **Issuer Compliance Portal (`/wallet/rwa-manage`):** Allowlist management, freeze/unfreeze controls, and automated coupon/dividend scheduling — forming the core of Kovanica's B2B SaaS offering (see [[11 - Revenue & Non-Token Monetization]]).

## Related Notes
- [[04 - Wave A-D Protocol Features]]
- [[07 - Web Properties & 5-Tab IA]]
- [[11 - Revenue & Non-Token Monetization]]
