# Ethics — ZONEMINDER

**Project:** ZONEMINDER  
**Category:** SURVEILLANCE_CAMERA  
**Upstream:** https://github.com/ZoneMinder/zoneminder  
**Pinned commit:** `3d858e2ccb323e168b520f1689ea7b3b43290fcd`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `9bcf1b072eaba36fbbc638117c2ee93cdce541b76a276e0665007161a97da8de`  
**Date:** October 2026

## Position

ZONEMINDER is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
