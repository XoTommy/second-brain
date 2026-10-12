---
title: DMO — Source Network
project: DMO
status: audit-needed
updated: 2026-10-13
tags: [DMO, sources]
---

# DMO — Source Network

## Problem

DMO expanded to ~33 Telegram sources.

Some are useful callers. Some appear to behave like raw trench/terminal feeds that call nearly everything.

Noise feeds can:

- flood candidate queues;
- waste provider/RPC budget;
- create fake convergence;
- make absolute winner counts look impressive without selectivity.

## Source objective

Do **not** rank by win rate alone.

Main priority:

> **ACTIVE + GOOD**

Judge sources by:

1. activity;
2. precision;
3. earliness;
4. unique contribution;
5. independence;
6. resource efficiency.

Conceptually:

```text
Source Value ≈ Activity × Precision × Earliness × Unique Contribution
```

Not a literal fixed formula.

## Desired buckets

- **KEEP_CORE** — active, selective, early, useful.
- **QUALITY_LOW_VOLUME** — less active but highly accurate/unique.
- **WATCHLIST** — mixed or insufficient sample.
- **REMOVE_NOISE** — trench-feed behavior.
- **REMOVE_REDUNDANT** — mostly duplicates/copies another source.
- **REMOVE_LOW_QUALITY** — enough evidence of poor quality and poor unique value.

## Critical metric

> **If this source were removed, which useful runners would DMO have missed entirely?**

This counterfactual matters more than absolute winner count.

## Audit metrics

Per source:

- calls/day;
- unique tokens/day;
- duplicate rate;
- median token age / MC at first call;
- earliest-source percentage;
- lead time vs next independent source;
- 1.5x/2x/2.5x/5x hit rate;
- calls required per 2x winner;
- calls required per 5x winner;
- unique early winners;
- percentage of candidate/provider load;
- dependency/copying evidence.

## Known lessons

- Red Bull Callz: historically useful runner source, but high raw volume.
- Wizzy's Casinò: fast source; sometimes CA is embedded in a link rather than raw text.
- A fast 2x is not automatically a good DMO call if the coin collapses immediately.
- Two noisy sources calling everything do not create meaningful independent convergence.

## Goal

Find the **smallest high-quality source set that preserves nearly all useful early opportunities while removing as much junk volume as possible**.

Do not target an arbitrary source count.
