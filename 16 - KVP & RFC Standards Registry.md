---
title: KVP & RFC Standards Registry
aliases:
  - KVP Standards
  - KVP Registry
  - RFC Registry
tags:
  - hub
  - core
  - defi
  - rwa
---

# 16 · KVP & RFC Standards Registry

Back to [[00 - Kovanica Protocol MOC]] · See [[Kovanica Architecture & Ecosystem.canvas]]

> [!IMPORTANT] Numbering Clarification (`KVP-10x` vs `RFC-00x`)
> Kovanica Improvement / Protocol Proposals use **`KVP-101` through `KVP-106`** (plus **`KVP-20`** for fungible contract token pairs). There are no `KVP-001`..`KVP-009` IDs — the `001`..`008` numbers belong to the companion **`RFC-001`..`RFC-008`** specification documents mapped below.

## Canonical KVP Standards

| Standard | Companion RFC | Name | What It Defines | Live Surface / Crate |
| :--- | :--- | :--- | :--- | :--- |
| **`KVP-20`** | ERC-20-style | **Fungible Contract Token Interface** | Standard fungible contract calls (`token_approve`, `token_transfer`, `token_transfer_from`) used for `KVNC/KVP-20` & `KVP-20/KVP-20` AMM pairs and wrapped bridge assets (`USDC`, `WETH`, `WBTC`). | `/swap`, `/pools`, `kovanica-amm` |
| **`KVP-101`** | `RFC-001` | **Multisig Wallets** | M-of-N shared custody, spend proposals, partial signatures, and signature combine. | `/multisig`, `kovanica-multisig` |
| **`KVP-102`** | `RFC-002` | **Native Multi-Asset Tokens** | On-chain fungible tokens (`token_create`, min fee `5 KVNC`), balances, transfers, wrapped bridge tokens, and on-chain AMM pools (`kvnc/v1/pool`). | `/multi-asset`, `/pools`, `/swap`, `/wallet` |
| **`KVP-103`** | `RFC-003` | **Stealth Addresses** | Privacy-preserving one-time stealth addresses spent using one-time derived keys. | `/stealth` |
| **`KVP-104`** | `RFC-004` | **HTLC (Hash Time-Locked Contracts)** | Trustless atomic swaps with hashlock + timelock (`redeem` / `refund`). | `/htlc`, `/wallet/atomic-swap` |
| **`KVP-105`** | `RFC-005` | **Time-Lock Vaults** | CLTV / CSV time-locked vaults and treasury vesting schedules. | `/vaults`, `kovanica-vault` |
| **`KVP-106`** | `RFC-007` | **Real-World Assets (RWA) & Native NFTs** | Institutional RWA (`kovanica-rwa`, deterministic BLAKE3 `kvp106:rwa:v1`, classes `RE`/`BOND`/`INVOICE`/`COMMODITY`/`FUND`/`OTHER`, allowlist, freeze, coupon scheduler; min fee `10 KVNC` create / `0.5 KVNC` mint) **and** non-fungible assets/collections. | `/rwa`, `/wallet/rwa-issue`, `/wallet/rwa-manage`, `/explorer/rwa/$assetId`, `/nft` |

## Companion Protocol Standards (Non-KVP)

| Standard | Name | What It Defines | Live Surface |
| :--- | :--- | :--- | :--- |
| **`PRO-21`** | **Canonical Address Format** | 64-char `kvnc` + 57 base32 + `dag` (32-byte Ed25519 pubkey + 29-bit BLAKE3 checksum). Strictly enforced on Mainnet (Chain `1`) & Testnet (Chain `2`). | All wallets, explorer, faucet & RPC |
| **`RFC-006`** | **Fee Floor & Dynamic Base Fee** | Canonical atoms/byte fee floor + Wave B EIP-1559 dynamic base fee (`kovanica_getBaseFee`). | `/api/fee_estimate`, `/api/base_fee` |
| **`RFC-008`** | **On-Chain Name Registry** | Human-readable name resolution (`NameRegistryClient`; intentionally holds no KVP number). | `kovanica-sdk`, `wallet-web`, `kovanica-playground` |

## Related Notes
- [[03 - PRO-21 Address & Cryptography]]
- [[04 - Wave A-D Protocol Features]]
- [[05 - DeFi, AMM & KVP-106 RWA]]
- [[07 - Web Properties & 5-Tab IA]]
- [[14 - Developer Quickstart & RPC Cookbook]]
