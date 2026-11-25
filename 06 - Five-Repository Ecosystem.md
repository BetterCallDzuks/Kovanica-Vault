---
title: Five-Repository Ecosystem
tags:
  - ecosystem
  - repos
  - sdk
---

# 06 · Five-Repository Ecosystem

Back to [[00 - Kovanica Protocol MOC]] · See [[Kovanica Architecture & Ecosystem.canvas]]

All five repositories under **`BetterCallDzuks/*`** enforce a strict PR-only workflow against `main` (`pr-policy.yml`) with clean separation of concerns:

```mermaid
flowchart TB
    L1["1. kovanica-l1 (Rust L1 · Audit-Frozen)"]
    SDK["2. kovanica-sdk v0.9.0 (TypeScript SDK)"]
    WEB["3. kovanica-web (kovanica.online · 38 Routes)"]
    APPS["4. kovanica-apps (wallet-web · MV3 Extension · Desktop · Mobile)"]
    PG["5. kovanica-playground (Developer RPC & Studio Workbench)"]

    L1 -->|"JSON-RPC 2.0 / WS / FFI"| SDK
    L1 -->|"RPC / Stratum / Faucet"| WEB
    SDK --> WEB
    SDK --> APPS
    SDK --> PG
```

| Repository | Stack | Role |
| :--- | :--- | :--- |
| **`BetterCallDzuks/kovanica-l1`** | Rust | Layer-1 node, Hybrid PoW + GHOSTDAG, Wasmi, RPC, Stratum, Faucet, Indexer, CLI |
| **`BetterCallDzuks/kovanica-sdk`** | TypeScript (`v0.9.0`) | Browser/Node client, failover transport, Wave A–D facades, offline codecs |
| **`BetterCallDzuks/kovanica-web`** | TanStack Start + Nitro + Tailwind v4 | Public portal (`kovanica.online`), Explorer, AMM, RWA, Mining Pool, Docs, Pricing |
| **`BetterCallDzuks/kovanica-apps`** | React, Tauri, MV3, Kotlin, Swift | `wallet-web`, `browser-extension`, `console-desktop`, `node-desktop`, Android, iOS |
| **`BetterCallDzuks/kovanica-playground`** | React 18 + Vite 5 | Read-only RPC Explorer + 4-group developer studio workbench |

## Related Notes
- [[07 - Web Properties & 5-Tab IA]]
- [[08 - Client Applications & Browser Extension]]
- [[09 - Developer SDK & Playground]]
- [[12 - Security, Audit & Mainnet 1.1.2027]]
