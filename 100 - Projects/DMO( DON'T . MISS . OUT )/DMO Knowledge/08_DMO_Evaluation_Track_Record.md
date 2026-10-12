---
title: DMO — Evaluation & Track Record
project: DMO
status: active
updated: 2026-10-13
tags: [DMO, evaluation]
---

# DMO — Evaluation & Track Record

## What to measure

Track:

- winners;
- losers;
- missed runners;
- late alerts;
- rejected winners;
- rugs;
- false VETOs;
- liquidity failures;
- executable exit feasibility;
- timing;
- fees/slippage where relevant.

Do not report only maximum chart multiples.

## Anti-lookahead

Future outcomes are evaluation labels only.

Never:

- use a later rug wallet to justify an earlier decision;
- tune rules from a known winner/loser;
- treat 5x later as proof of safety.

## Live runner slice — 2026-10-12

A Telegram export contained 14 visible new calls (10 full DMO + 4 Beta).

By export end, 7 had recorded 2x+ observed milestones, but observation windows were uneven, so this is **not** a final 50% win-rate claim.

Notable observed maxima:

- SEAN ~5.89x
- oracle ~5.06x
- Diggs ~2.27x
- XDOGE ~2.15x
- Solamians ~2.57x
- Sniff ~2.35x
- apelink ~2.08x

Observed peak ≠ guaranteed executable return.

## Two evaluation axes

### Opportunity quality
Did DMO find a useful move early enough?

### Safety quality
Did Rug Defense correctly identify destructive capability?

A coin may score well on one axis and badly on the other.

## Rug Defense benchmark status

Latest hardening proved:

- isolation from base DMO;
- no runner decision changes;
- no runner VETOs;
- low latency overhead;
- green test suite.

It **did not yet prove a high rug-catch rate**.

## Per-call record

Store:

```text
token / CA / chain
sources
first_seen
call_time
call_MC
liquidity
base_decision
rug_label
rug_reason
1.5x / 2x / 2.5x / 5x
time_to_2x
max_observed_multiple
last_multiple
executable estimate
rug/scam outcome
notes
```
