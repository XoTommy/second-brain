---
title: DMO — Repos, Branches & Handoffs
project: DMO
status: reference
updated: 2026-10-13
tags: [DMO, repo]
---

# DMO — Repos, Branches & Handoffs

## Frozen Beta

- branch: `dmo-beta`
- worktree: `D:\dmo-beta`
- HEAD: `7c15b93fa1344a744f4fe8461293a7f14a293b92`

**DO NOT MODIFY.**

## Rug Defense worktree

`D:\dmo-rug-defense`

Contains current Rug Defense/economic-cluster work and GemBot shadow artifacts.

## Original repo

`D:\dmo-call-aggregator`

## GemBot research

`D:\gembot-recon`

Research-only.

## Important docs

- `docs/DMO_RUG_DEFENSE_CONTINUATION_20261011.md`
- `docs/DMO_RUG_DEFENSE_CONTINUATION_20261011.json`
- `docs/DMO_ECONOMIC_CLUSTER_HARDENING_20261012.md`
- `docs/DMO_GEMBOT_SHADOW.md`

## Publication checkpoint

Reported accepted publication-path checkpoint:

`13c0084922e2c9f27b617284a263bcada850696b`

## Important commits

| Commit | Purpose |
|---|---|
| `d9e0792` | production runtime |
| `91cc9a1` | refresh BACKOFF |
| `05a9310f` | evaluation windows |
| `d2b09ab8` | prospective cohort |
| `1e977097` | anti-lookahead replay |
| `4e20785c` | coverage expansion |
| `247b386` | GMGN backtest |
| `e8e94fa` | live hardening |
| `388b0565` | NEWSOM safety |
| `ad4df95` | fast-path provider identity |
| `4e72f7b` | acceptance alias/canonical fixes |

## Local DB

- PGDATA: `D:\dmo-call-aggregator\data\postgres-test-cluster`
- host: `127.0.0.1`
- port: `55439`

## Secrets rule

Never print or paste Helius/Telegram/private secrets.

## Cross-chat handoff rule

Every real checkpoint from another DMO chat must update the relevant Obsidian note with one of:

`ACCEPTED / IMPLEMENTED / SHADOW / EXPERIMENTAL / PLANNED / UNPROVEN / REJECTED`

This is how parallel chats stay one project instead of diverging.
