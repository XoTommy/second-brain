---
title: DMO — Runner Improvements
project: DMO
status: planned
updated: 2026-10-13
tags: [DMO, runners, promotion]
---

# DMO — Runner Improvements

## Two different failure modes

### 1. Missed/unsurfaced runner
DMO may never surface a source opportunity.

### 2. Late promotion
DMO sees the token early but waits too long before calling it.

These need separate fixes.

## ZKINU — missed/unsurfaced case

CA:

`DGdmHacFYkfrazHYtFEPtAbRnSru8db5cNyQkgY6QsQV`

Observed:

- Red Bull called around ~$40K;
- later market around ~$185K;
- displayed ATH around ~$255K.

Exact DMO failure branch is still UNPROVEN until logs/DB show whether the issue was:

- source inactive;
- message not received;
- parser;
- admission;
- DMO gate;
- market data;
- research delay;
- pre-send;
- publication.

Do not tune thresholds merely because it later pumped.

## LUCKY — late-promotion case

CA:

`H1hqLeM7YWs2JFHFJWkbQAcLyPh7DWfn7aUCwtGdpump`

DMO did catch it early but later emitted `EARLY WATCH` around ~$186K.

At that stage DMO already had:

- fresh canonical market;
- viable liquidity;
- no hard veto;
- 2-source independent convergence.

Missing:

- official project/contract attribution;
- verified catalyst.

GemBot's observed marker appeared around ~$17K.

**Conclusion:** discovery worked; promotion logic was too bureaucratic/late.

## Planned dual-path promotion

### Path A — Catalyst / Thesis Call

```text
credible attribution
+ verified narrative/catalyst
+ healthy market
+ safety
→ CALL
```

### Path B — Early Market / Flow Call

```text
high-quality source(s)
+ genuine independent convergence
+ early market position
+ constructive structure
+ executable liquidity
+ no Rug VETO
→ CALL / Beta-style lower-confidence call
```

Research can continue afterward.

## EARLY WATCH semantics

Internal workflow state must not define market earliness.

Track opportunity expansion from the frozen first-seen executable reference:

```text
current MC / first-seen MC
```

Distinguish:

- genuinely early;
- expanded but actionable;
- late/crowded;
- exhausted.

Do not impose one arbitrary universal multiple cutoff without data.

## Runner-preservation rule

Any promotion improvement must preserve:

- current source-driven discovery;
- CurrentState;
- canonical market selection;
- fast-lane responsiveness;
- existing successful CALL behavior.

Goal:

> **earlier valid calls, not simply more calls.**
