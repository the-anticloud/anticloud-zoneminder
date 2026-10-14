# Educators — ZONEMINDER

**Project:** ZONEMINDER  
**Category:** SURVEILLANCE_CAMERA  
**Upstream:** https://github.com/ZoneMinder/zoneminder  
**Pinned commit:** `3d858e2ccb323e168b520f1689ea7b3b43290fcd`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `9bcf1b072eaba36fbbc638117c2ee93cdce541b76a276e0665007161a97da8de`  
**Date:** October 2026

## Teaching with ZONEMINDER

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `9bcf1b072eaba36fbbc638117c2ee93cdce541b76a276e0665007161a97da8de` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
