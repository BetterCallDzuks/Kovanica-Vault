---
title: Wave A-D Protocol Features
tags:
  - defi
  - rwa
  - wave
---

# 04 · Wave A–D Protocol Features

Back to [[00 - Kovanica Protocol MOC]]

Kovanica ships four coordinated protocol & UX waves across `kovanica-l1`, `kovanica-sdk v0.9.0`, `kovanica-web`, `kovanica-apps`, and `kovanica-playground`:

| Wave | Capabilities | Where It Lives |
| :--- | :--- | :--- |
| **Wave A** | **Atomic 1-Tx Batches** (`Deploy+Call`, `Approve+Swap`, `Approve+AddLiquidity`) | `/swap`, `/pools`, `browser-extension` (`window.kovanica`), `android` (`BatchTokenDeployHelper`), `kovanica-playground` |
| **Wave B** | **EIP-1559 Base Fee & Storage Deposit** (`kovanica_getBaseFee`, `kovanica_getStorageDeposit`, `kovanica_mempoolStats`) | Live fee banners on `/swap`, `/pools`, `/explorer` (`LiveDagDrawer`) & `wallet-web` |
| **Wave C** | **WebAuthn Passkeys, Session Keys & Scheduler Keeper** | `/wallet/ecosystem-tools`, `kovanica-l1` keeper unit, `WaveARwaStudio` |
| **Wave D** | **BTC / Solana / All-EVM Bridge Registry & KVP-106 RWA Compliance** | `/rwa`, `/wallet/rwa-issue`, `/wallet/rwa-manage`, `/wallet/ecosystem-tools` |

## Related Notes
- [[05 - DeFi, AMM & KVP-106 RWA]]
- [[07 - Web Properties & 5-Tab IA]]
- [[08 - Client Applications & Browser Extension]]
- [[09 - Developer SDK & Playground]]
