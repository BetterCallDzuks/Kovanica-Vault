---
title: Security, Audit & Mainnet 1.1.2027
tags:
  - security
  - roadmap
mainnet_launch: 2027-01-01
---

# 12 · Security, Audit & Mainnet 1.1.2027

Back to [[00 - Kovanica Protocol MOC]]

## Canonical Chain Isolation

| Network | Chain ID | Canonical Tag | Status |
| :--- | :---: | :--- | :--- |
| **Mainnet** | `1` | `1-f35df34c92001436` | Audit-frozen RC (`v1.0.0-mainnet`) · Launches **1.1.2027** |
| **Testnet** | `2` | `2-24cdb5fadd98b207` | **Live** (`rpc-testnet.kovanica.online`, `seed1.kovanica.online:8000`) |
| **Devnet** | `3` | `3-<ephemeral>` | Local development only |

## Engineering & Governance Guardrails

- **Audit-Frozen L1 Consensus:** `kovanica-l1` consensus & cryptographic parameters remain frozen pending formal external security audit before Mainnet T0 (`1.1.2027`).
- **PR-Only Workflow Across All 5 Repos:** Zero direct commits to `main`, mandatory Conventional Commit PRs, `pr-policy.yml` gate, full CI (`typecheck`, `lint`, `test`, `build`).
- **Zero Mainnet/Testnet Leakage:** Mainnet pre-launch endpoints return explicit `503` (reads) / `403` (mutations) — never silently falling back to testnet data.
- **Zero Secret Leakage & CSP Hardening:** Per-request CSP nonces, HSTS, `X-Frame-Options: DENY`, strict `https://` URL sanitization on all sponsor/partner configs, and zero committed `.env` or keystore files.

## Related Notes
- [[01 - Consensus & L1 Architecture]]
- [[03 - PRO-21 Address & Cryptography]]
- [[06 - Five-Repository Ecosystem]]
- [[00 - Kovanica Protocol MOC]]
