---
title: DeFi, AMM & KVP-106 RWA
tags:
  - defi
  - rwa
---

# 05 · DeFi, AMM & KVP-106 RWA

Back to [[00 - Kovanica Protocol MOC]]

## Native AMM DEX (`Trade` Tab)

- **AMM Swap (`/swap`):** End-to-end client-signed constant-product `x·y=k` swaps with slippage presets, Wave A 1-tx atomic `Approve → Swap` batches, official KVNC/KSMOKE token artwork, live Wave B base-fee telemetry, and transparent interface-fee breakdown (`0.00%` on testnet; configurable via `VITE_SWAP_INTERFACE_FEE_BPS`).
- **AMM Liquidity Pools (`/pools`):** End-to-end client-signed pool initialization, Wave A 1-tx `Add Liquidity`, LP share burn/withdrawal, wallet token watchlist sync, **plus** the on-chain KVP-102 `PoolView` explorer & exact quote calculator (cleanly separated from Stratum Mining Pool `/pool`).
- **Orderbook DEX (`/wallet/dex`) & Atomic Swaps (`/wallet/atomic-swap`):** Reachable in 1 click from the **Trade** tab and contextual Trade sub-nav strip.

## KVP-102 Tokens, Native NFTs & Institutional KVP-106 RWA (`Assets` Tab)

- **Create Token (`/multi-asset`, KVP-102):** End-to-end browser token creation (`Deploy` `kovanica-token.wasm` + `token_create` `Call`) signed client-side via unlocked Web Wallet (canonical BIP-44 SLIP-0010 `m/44'/3007'/0'/0'/0'`) or `window.kovanica` extension and broadcast via `kovanica_sendRawTransaction` (`/api/submit_tx`). Displays Balanced fixed fees (`5 KVNC` `token_create` + `1 KVNC` deploy), derived contract address, 1-click **Watch token**, and Explorer link.
- **Create Collection & Mint NFT (`/nft`, KVP-106):** Live interactive collection creation (`Deploy` + `nft_create_collection`) and NFT minting (`nft_mint` for new or existing collections) with Balanced fee display (`2 KVNC` collection / `0.1 KVNC` mint), client-side signing, and direct links to `/wallet/nft/$assetId` and `/explorer`.
- **Public RWA Registry (`/rwa` & `/explorer/rwa/$assetId`):** Browse verified real-world assets (`RE`, `BOND`, `INVOICE`, `COMMODITY`, `FUND`, `OTHER`) and inspect compliance metadata.
- **Deterministic & Client-Signed RWA Issuance (`/wallet/rwa-issue`):** Auto pre-fills Issuer & Recipient from the active wallet, computes exact BLAKE3 `kvp106:rwa:v1` asset IDs (`POST /api/rwa/derive` + client fallback), supports flexible `https://` / `ipfs://` metadata URIs or automatic inline JSON SHA-256 hash fallback when public IPFS gateways rate-limit, and signs/broadcasts real `Deploy` + `rwa_create` (+ optional `rwa_mint`) transactions to Testnet Chain 2 via `kovanica_sendRawTransaction`.
- **Issuer Compliance Portal (`/wallet/rwa-manage`):** Allowlist management, freeze/unfreeze controls, and automated coupon/dividend scheduling — forming the core of Kovanica's B2B SaaS offering (see [[11 - Revenue & Non-Token Monetization]]).

## Related Notes
- [[04 - Wave A-D Protocol Features]]
- [[07 - Web Properties & 5-Tab IA]]
- [[11 - Revenue & Non-Token Monetization]]
