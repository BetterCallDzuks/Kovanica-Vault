---
title: Mining Pool & Stratum V1 TLS
tags:
  - mining
  - l1
route: /pool
---

# 10 · Mining Pool & Stratum V1 TLS

Back to [[00 - Kovanica Protocol MOC]]

## Dedicated Mining Pool Surface (`/pool`)

Cleanly separated from AMM Liquidity Pools (`/pools`), the `/pool` route under the **Explore** tab provides everything CPU/GPU miners need:

- **Stratum V1 over TLS (required):** Encrypted share submission with adaptive VarDiff and graceful `client.reconnect` draining.
- **Frozen Consensus Spec Strip:** `KovanicaHash` PoW · `GHOSTDAG K=5` · `4s` target block time · `2.5 KVNC` initial reward · `8,200,000` blocks/era (`3/4` decay) · `3/4` burn / `1/4` miner fee split.
- **Interactive `MinerCommandBuilder` (expanded by default):** Validates PRO-21 payout addresses (`kvnc…dag` / `tknc…dag`), worker names, thread counts, and TLS cert flags to generate shell-safe `kovanica mine ...` commands for both Stratum TLS and Solo RPC.
- **Transparent Pool Fee:** `0%` on Testnet · `1.0%` planned on Mainnet (configurable via `VITE_MINING_POOL_FEE_PCT`) — see [[11 - Revenue & Non-Token Monetization]].

## Related Notes
- [[01 - Consensus & L1 Architecture]]
- [[02 - Tokenomics & Frozen Emission]]
- [[07 - Web Properties & 5-Tab IA]]
- [[11 - Revenue & Non-Token Monetization]]
