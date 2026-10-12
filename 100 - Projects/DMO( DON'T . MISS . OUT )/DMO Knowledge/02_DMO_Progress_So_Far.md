---
title: DMO — Progress So Far
project: DMO
status: active
updated: 2026-10-13
tags: [DMO, progress]
---

# DMO — Progress So Far

## Accepted Beta

**Frozen baseline**

- branch: `dmo-beta`
- worktree: `D:\dmo-beta`
- HEAD: `7c15b93fa1344a744f4fe8461293a7f14a293b92`

Accepted characteristics:

- source-driven CALL/WATCH/REJECT flow;
- fresh `CurrentState`;
- canonical market selection;
- hard vetoes;
- pre-send refresh/cancel;
- PostgreSQL durability;
- prospective outcomes;
- anti-lookahead;
- trading disabled.

Accepted local latency baseline: ~6.60s median / ~13.18s p95.

## Important historical commits

- `d9e0792` — production runtime.
- `91cc9a1` — bounded refresh BACKOFF.
- `05a9310f` — evaluation windows/dataset.
- `d2b09ab8` — prospective cohort/restart recovery.
- `1e977097` — historical replay + anti-lookahead.
- `4e20785c` — coverage expansion.
- `247b386` — GMGN backtest/coverage.
- `e8e94fa` — live hardening.
- `388b0565` — NEWSOM fail-closed CurrentState patch.
- `ad4df95` — fast-path provider identity ordering.
- `4e72f7b` — alias/canonical fixes in acceptance sequence.

## Opportunity engine evidence

Recent prospective examples include:

- SEAN ~5.89x observed.
- oracle ~5.06x.
- Diggs ~2.27x.
- XDOGE ~2.15x.
- Solamians ~2.57x.
- Sniff ~2.35x.
- apelink ~2.08x.

These are observed tracker peaks, not guaranteed executable returns.

**Conclusion:** the opportunity engine is already producing runners.

## Rug Defense hardening

Active worktree: `D:\dmo-rug-defense`

Latest economic-cluster hardening:

- explainable bounded clustering implemented;
- transfer topology / private-funder fan-out / actor reuse support;
- supporting evidence alone cannot VETO;
- 7 runner benchmarks;
- 0 runner base-decision changes;
- 0 runner VETOs;
- OFF vs SHADOW differences: 0;
- median added latency ~2.42ms;
- p95 ~7.86ms;
- max observed ~34.45ms;
- request cap 8/candidate;
- focused tests 234 passed, 1 skipped;
- full suite 1,523 passed, 32 skipped, 291 subtests;
- SHADOW safe: yes;
- enforcement ready: no.

At that checkpoint the changes were reported **uncommitted**.

## Current weak spots

- proven prospective rug-catch rate is still unestablished;
- disposable-wallet actor attribution remains hard;
- source set includes probable trench/noise feeds;
- promotion can be too late when catalyst/attribution is missing;
- GemBot edge is not fully reconstructed;
- persistent $0 hosting remains an operational problem.

## Current status sentence

> **DMO works well enough to find runners; current work is about cleaner sources, earlier promotion, and stronger scam/rug discrimination without harming the working engine.**
