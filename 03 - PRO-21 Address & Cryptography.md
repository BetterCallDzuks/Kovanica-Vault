---
title: PRO-21 Address & Cryptography
tags:
  - core
  - security
  - crypto
---

# 03 · PRO-21 Address & Cryptography

Back to [[00 - Kovanica Protocol MOC]]

## Canonical PRO-21 Address Format

Every address on Mainnet (Chain `1`) and Testnet (Chain `2`) is strictly **64 characters**:

```text
kvnc + 57 base32 characters + dag
```

- Encodes the **32-byte Ed25519 public key** (`256` bits) + the **first 29 bits of its BLAKE3 hash** MSB-first (`285` bits = `57` unpadded BIP-173 lowercase base32 chars).
- **Fail-closed enforcement:** Legacy 64-hex addresses are permitted *only* on local Devnet (Chain `3`) and strictly rejected on Mainnet (`1`) and Testnet (`2`).

## Cryptographic Primitives Across the Stack

1. **Ed25519** — Canonical account keys & SLIP-0010 HD derivation (`kovanica-sdk` & `kovanica-apps`).
2. **P-256 (WebAuthn Passkeys)** — Hardware-backed browser/mobile passkey verification (Wave C).
3. **ML-DSA-65** — Real post-quantum signature verification built into `kovanica-l1`.
4. **BLAKE3** — Address checksums, KVP-106 deterministic RWA asset IDs (`kvp106:rwa:v1`), and air-gap envelopes (`kvnc-tx:v1:`).

## Related Notes
- [[01 - Consensus & L1 Architecture]]
- [[04 - Wave A-D Protocol Features]]
- [[08 - Client Applications & Browser Extension]]
- [[12 - Security, Audit & Mainnet 1.1.2027]]
