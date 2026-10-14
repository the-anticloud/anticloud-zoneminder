# Students — ZONEMINDER

**Project:** ZONEMINDER  
**Category:** SURVEILLANCE_CAMERA  
**Upstream:** https://github.com/ZoneMinder/zoneminder  
**Pinned commit:** `3d858e2ccb323e168b520f1689ea7b3b43290fcd`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `9bcf1b072eaba36fbbc638117c2ee93cdce541b76a276e0665007161a97da8de`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `3d858e2ccb323e168b520f1689ea7b3b43290fcd`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `9bcf1b072eaba36fbbc638117c2ee93cdce541b76a276e0665007161a97da8de`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
