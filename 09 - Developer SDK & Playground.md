---
title: Developer SDK & Playground
tags:
  - sdk
  - playground
repos:
  - BetterCallDzuks/kovanica-sdk
  - BetterCallDzuks/kovanica-playground
sdk_version: 0.10.0
---

# 09 · Developer SDK & Playground

Back to [[00 - Kovanica Protocol MOC]]

## `kovanica-sdk` (`v0.10.0`)
- Browser & Node.js (18/20/22) TypeScript client with `FailoverHttpTransport` and `KovanicaWsClient` (`newHeads`, `newCommittedLeader`, backpressure-capped block+receipt streaming).
- **KVP-103 Dual-Key Ed25519 Stealth Addresses** (`src/stealth.ts`): meta-address codec, deterministic mnemonic derivation, sender one-time derivation, watch-only view-tag scanner, one-time spend key recovery & RFC 8032 scalar signing.
- Typed contract facades across all canonical families (`NameRegistryClient`, `TokenClient`, `EscrowClient`, `HtlcClient`, `NftClient`, `VaultClient`, `MultisigClient`, `AmmClient`, `RwaClient`).
- Offline PRO-21 address validation, universal raw wire tx codec, storage-slot derivers, air-gap `kvnc-tx:v1:` envelopes, runnable `examples/` kit (`01`–`05`), and automated npm OIDC `--provenance` publish workflow (`.github/workflows/publish.yml`).

## `kovanica-playground`
A read-only developer console and interactive studio (zero private key custody) organized into **4 clean sub-tabs**:
1. **HD Wallet & Signer** — Ephemeral SLIP-0010 wallet, tx auto-decoder, air-gap studio, fee-tier estimator.
2. **Contracts & Codegen** — Wasmi call builder, multi-call batch estimator, cURL/SDK codegen, 7 typed facades.
3. **Storage & Logs** — Storage slot deriver, live `kovanica_getStorageAt` bincode decoder, paginated log explorer.
4. **Verification & Diagnostics** — Failover RPC probe, receipt poller, JSON-RPC 2.0 batch runner, golden vectors.
- Plus **Wave A–D & RWA Studio** (`WaveARwaStudio`), **KVP-103 Stealth Studio** (`StealthStudio`), 1-click public RPC presets (`rpc-testnet.kovanica.online/rpc`), and cross-subdomain Ecosystem Switcher.

## Related Notes
- [[04 - Wave A-D Protocol Features]]
- [[06 - Five-Repository Ecosystem]]
- [[07 - Web Properties & 5-Tab IA]]
- [[08 - Client Applications & Browser Extension]]
