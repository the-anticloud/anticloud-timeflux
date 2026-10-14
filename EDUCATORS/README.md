# Educators — TIMEFLUX

**Project:** TIMEFLUX  
**Category:** BRAIN_COMPUTER_INTERFACE  
**Upstream:** https://github.com/timeflux/timeflux.git  
**Pinned commit:** `f9b68163cdbd9cdce5a87204f6206d0a73ff3d02`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `b1ace56782b7baf2976bde772a4ad28c590b280f0e88f723eb810a06a48f1d55`  
**Date:** October 2026

## Teaching with TIMEFLUX

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `b1ace56782b7baf2976bde772a4ad28c590b280f0e88f723eb810a06a48f1d55` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
