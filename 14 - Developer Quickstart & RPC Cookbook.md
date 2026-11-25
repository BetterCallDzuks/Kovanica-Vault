---
title: Developer Quickstart & RPC Cookbook
tags:
  - sdk
  - playground
  - web
sdk_version: 0.9.0
---

# 14 · Developer Quickstart & RPC Cookbook

Back to [[00 - Kovanica Protocol MOC]] · Live Reference: [testnet.kovanica.online/api-reference](https://testnet.kovanica.online/api-reference)

## 1. Query Live Testnet JSON-RPC (`Chain 2`)

```bash
curl -sS -X POST https://rpc-testnet.kovanica.online/rpc \
  -H "content-type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"kovanica_syncStatus","params":[]}'
```

## 2. Check Live Wave B Base Fee & Storage Deposit

```bash
curl -sS https://testnet.kovanica.online/api/base_fee
```

## 3. Derive Deterministic KVP-106 RWA Asset ID

```bash
curl -sS -X POST https://testnet.kovanica.online/api/rwa/derive \
  -H "content-type: application/json" \
  -d '{
    "issuer": "kvnc8a4atp0g5tngcua9h90anhel7233alyd5y88h0yc592cv8adu5uyz46d3dag",
    "asset_class": "BOND",
    "unique_id": "US-TBILL-2027-Q1",
    "version": 1
  }'
```

## 4. Connect with `kovanica-sdk` (`v0.9.0`)

```ts
import { KovanicaClient } from "kovanica-sdk";

const client = new KovanicaClient({
  rpcUrl: "https://rpc-testnet.kovanica.online/rpc",
});

const status = await client.getSyncStatus();
console.log("Chain tip:", status);
```

## 5. Mine on Testnet via Stratum V1 TLS

Generate a validated command interactively at [testnet.kovanica.online/pool](https://testnet.kovanica.online/pool) (see [[10 - Mining Pool & Stratum V1 TLS]]):

```bash
kovanica mine \
  --chain-id 2 \
  --stratum stratum+tls://stratum.example.com:3333 \
  --tls \
  --address kvnc...dag \
  --worker rig-01 \
  --threads 4
```

## Related Notes
- [[06 - Five-Repository Ecosystem]]
- [[09 - Developer SDK & Playground]]
- [[10 - Mining Pool & Stratum V1 TLS]]
- [[05 - DeFi, AMM & KVP-106 RWA]]
