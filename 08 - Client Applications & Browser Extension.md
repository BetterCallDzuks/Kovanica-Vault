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
| **`wallet-web`** | React / TanStack Start + `kovanica-sdk v0.9.0` | Multi-endpoint RPC failover, finality watcher, 3-sub-tab Contracts workspace (7 typed facades + batch + logs/multisig), air-gap `kvnc-tx:v1:` envelopes, chain-aware explorer links |
| **`browser-extension`** | Chrome / Brave / Firefox **MV3** | Non-custodial popup wallet + **`window.kovanica`** dApp provider, Wave A `signBatchTransaction` approval modal, dual Chrome (`manifest.json`) & Firefox (`manifest.firefox.json`, `wallet@kovanica.online`) MV3 builds, deterministic `.zip` packagers (`package:chrome`, `package:firefox`, `package:firefox-source`) & complete Chrome Web Store / Firefox AMO submission kit (`store-assets/` listings, privacy policy, verified brand PNGs) |

> [!TIP] Store Submission Readiness (Merged in `kovanica-apps#27`, Privacy Live in `kovanica-web#42`)
> `browser-extension/store-assets/` ships review-ready **Chrome Web Store** & **Firefox AMO** copy, zero-telemetry `PRIVACY_POLICY.md` (live at `https://kovanica.online/privacy`, `HTTP/2 200`), step-by-step `SUBMISSION_CHECKLIST.md`, verified PNG icons (`16/32/48/128`), `440x280` promo tile, and `1280x800` screenshots — plus reproducible `.zip` + `.sha256` bundles (`18/18` Vitest passing).
| **`console-desktop`** | Tauri + React | Operator node inspector, single-POST batch RPC health probe, cluster readiness aggregator |
| **`node-desktop`** | Tauri (Linux `.deb`) | External `kovanica-node` supervisor, Stratum & faucet alarms, snapshot verifier |
| **`desktop`** | Tauri | E2E encrypted Comms shell |
| **`android*` & `ios`** | Kotlin / Swift + UniFFI | `android-wallet` (streamlined 2-tab Wallet/Account, `Testnet`/`Mainnet` only, dark 24-word seed confirmation, BIP-44 parity), `android-node` (foreground `START_STICKY` + WakeLock/WifiLock keep-alive, embedded `127.0.0.1:8545` RPC & thermal-safe `1..4`-thread PoW miner), `BatchTokenDeployHelper` & iOS light client |

## Related Notes
- [[03 - PRO-21 Address & Cryptography]]
- [[04 - Wave A-D Protocol Features]]
- [[06 - Five-Repository Ecosystem]]
- [[09 - Developer SDK & Playground]]
