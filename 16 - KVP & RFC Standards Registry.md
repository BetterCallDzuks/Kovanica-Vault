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

> [!IMPORTANT] Numbering Clarification (`RFC-001`–`RFC-008` vs `KVP-101`–`KVP-106`)
> The `001`–`008` sequence belongs to the companion **`RFC-001`–`RFC-008`** specifications (ordered sequentially below). Protocol proposals use **`KVP-101`–`KVP-106`** (plus **`KVP-20`** for fungible contract token pairs and **`PRO-21`** for canonical addresses).

## Sequential RFC & KVP Registry (`RFC-001` → `RFC-008`)

| RFC | KVP | Name | What It Defines | Live Surface / Crate |
| :--- | :--- | :--- | :--- | :--- |
| **`RFC-001`** | `KVP-101` | **Multisig Wallets** | M-of-N shared custody, spend proposals, partial signatures, and signature combine. | `/multisig`, `kovanica-multisig` |
| **`RFC-002`** | `KVP-102` | **Native Multi-Asset Tokens** | On-chain fungible tokens (`token_create`, min fee `5 KVNC`), balances, transfers, wrapped bridge tokens, and on-chain AMM pools (`kvnc/v1/pool`). | `/multi-asset`, `/pools`, `/swap`, `/wallet` |
| **`RFC-003`** | `KVP-103` | **Stealth Addresses** | Privacy-preserving one-time stealth addresses spent using one-time derived keys. | `/stealth` |
| **`RFC-004`** | `KVP-104` | **HTLC (Hash Time-Locked Contracts)** | Trustless atomic swaps with hashlock + timelock (`redeem` / `refund`). | `/htlc`, `/wallet/atomic-swap` |
| **`RFC-005`** | `KVP-105` | **Time-Lock Vaults** | CLTV / CSV time-locked vaults and treasury vesting schedules. | `/vaults`, `kovanica-vault` |
| **`RFC-006`** | — | **Fee Floor & Wave B Base Fee** | Canonical atoms/byte fee floor + Wave B EIP-1559 dynamic base fee (`kovanica_getBaseFee`). | `/api/fee_estimate`, `/api/base_fee` |
| **`RFC-007`** | `KVP-106` | **Real-World Assets (RWA) & Native NFTs** | Institutional RWA (`kovanica-rwa`, deterministic BLAKE3 `kvp106:rwa:v1`, classes `RE`/`BOND`/`INVOICE`/`COMMODITY`/`FUND`/`OTHER`, allowlist, freeze, coupon scheduler; min fee `10 KVNC` create / `0.5 KVNC` mint) **and** non-fungible assets/collections. | `/rwa`, `/wallet/rwa-issue`, `/wallet/rwa-manage`, `/explorer/rwa/$assetId`, `/nft` |
| **`RFC-008`** | — | **On-Chain Name Registry** | Human-readable name resolution (`NameRegistryClient`; intentionally holds no KVP number). | `kovanica-sdk`, `wallet-web`, `kovanica-playground` |
| — | **`KVP-20`** | **Fungible Contract Token Interface** | ERC-20-style `token_approve` / `token_transfer` / `token_transfer_from` for `KVNC/KVP-20` & `KVP-20/KVP-20` AMM pairs and wrapped bridge assets (`USDC`, `WETH`, `WBTC`). | `/swap`, `/pools`, `kovanica-amm` |
| — | **`PRO-21`** | **Canonical Address Format** | 64-char `kvnc` + 57 base32 + `dag` (32-byte Ed25519 pubkey + 29-bit BLAKE3 checksum). Strictly enforced on Mainnet (Chain `1`) & Testnet (Chain `2`). | All wallets, explorer, faucet & RPC |

## Related Notes
- [[03 - PRO-21 Address & Cryptography]]
- [[04 - Wave A-D Protocol Features]]
- [[05 - DeFi, AMM & KVP-106 RWA]]
- [[07 - Web Properties & 5-Tab IA]]
- [[14 - Developer Quickstart & RPC Cookbook]]
