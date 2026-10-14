# Students — TIMEFLUX

**Project:** TIMEFLUX  
**Category:** BRAIN_COMPUTER_INTERFACE  
**Upstream:** https://github.com/timeflux/timeflux.git  
**Pinned commit:** `f9b68163cdbd9cdce5a87204f6206d0a73ff3d02`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `b1ace56782b7baf2976bde772a4ad28c590b280f0e88f723eb810a06a48f1d55`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `f9b68163cdbd9cdce5a87204f6206d0a73ff3d02`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `b1ace56782b7baf2976bde772a4ad28c590b280f0e88f723eb810a06a48f1d55`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
