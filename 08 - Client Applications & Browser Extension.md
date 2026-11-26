---
title: Client Applications & Browser Extension
tags:
  - apps
  - wallet
repo: BetterCallDzuks/kovanica-apps
---

# 08 · Client Applications & Browser Extension

Back to [[00 - Kovanica Protocol MOC]]

`kovanica-apps` delivers Kovanica across browser, desktop, and mobile — all aligned to canonical `rpc-testnet.kovanica.online/rpc` and cross-linked via the Ecosystem Switcher:

| App | Platform / Stack | Key Capabilities |
| :--- | :--- | :--- |
| **`wallet-web`** | React / TanStack Start + `kovanica-sdk v0.10.0` | Unified `kovanica.online` dark zinc + gold UI, multi-endpoint RPC failover, finality watcher, inline SVG Receive QR (`kvnc...dag` + KVP-103 `st:kvnc:...`), 3-sub-tab Contracts workspace, air-gap `kvnc-tx:v1:` envelopes |
| **`browser-extension`** | Chrome / Brave / Firefox **MV3** | Unified `kovanica.online` dark zinc + gold UI, KVNC coin branding, KVP-102 token watchlist & send, KVP-103 stealth meta-address receive (`window.kovanica.getStealthMetaAddress()`), offline inline-SVG QR receive, AMM/RWA/KVP-102 signing previews, dual Chrome/Firefox MV3 builds & refreshed dark zinc + gold Chrome Web Store / Firefox AMO submission kit (`store-assets/`) |

> [!TIP] Store Submission Readiness (Updated in `kovanica-apps#33–#37`, Privacy Live in `kovanica-web#42`)
> `browser-extension/store-assets/` ships review-ready **Chrome Web Store** & **Firefox AMO** copy, zero-telemetry `PRIVACY_POLICY.md` (live at `https://kovanica.online/privacy`, `HTTP/2 200`), step-by-step `SUBMISSION_CHECKLIST.md`, dark zinc + gold PNG icons (`16/32/48/128`), `440x280` promo tile, and `1280x800` screenshots — plus reproducible `.zip` + `.sha256` bundles (`33/33` Vitest passing).
| **`console-desktop`** | Tauri + React | Unified `kovanica.online` dark zinc + gold UI, operator node inspector, single-POST batch RPC health probe, cluster readiness aggregator |
| **`node-desktop`** | Tauri (Linux `.deb`) | Unified `kovanica.online` dark zinc + gold UI, external `kovanica-node` supervisor, Stratum & faucet alarms, snapshot verifier |
| **`desktop`** | Tauri | Unified `kovanica.online` dark zinc + gold E2E encrypted Comms shell |
| **`android*` & `ios`** | Kotlin / Swift + UniFFI | `android-wallet` (`kovanica.online` palette, 2-tab Wallet/Account, KVP-102 tokens, BIP-44 parity), `android-node` (`kovanica.online` dark zinc + gold native UI, foreground `START_STICKY` + WakeLock/WifiLock keep-alive, embedded `127.0.0.1:8545` RPC & thermal-safe `1..4`-thread PoW miner), `BatchTokenDeployHelper` & iOS light client |

## Related Notes
- [[03 - PRO-21 Address & Cryptography]]
- [[04 - Wave A-D Protocol Features]]
- [[06 - Five-Repository Ecosystem]]
- [[09 - Developer SDK & Playground]]
