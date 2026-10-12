---
title: DMO — Runtime, Cloud & Publication
project: DMO
status: active
updated: 2026-10-13
tags: [DMO, runtime, cloud, publication]
---

# DMO — Runtime, Cloud & Publication

## Separation rule

DMO decides whether an opportunity qualifies.

The downstream relay/publisher decides how an already-qualified call is rendered/distributed.

Do not confuse opportunity-selection failures with relay/cloud failures.

## Telegram routing

### TEST channel
May contain CALL, Beta, EARLY WATCH, WATCH, REJECT, results, diagnostics, research/status.

### Downstream/public path
Should receive only approved call types.

Do not forward:

- EARLY WATCH;
- WATCH;
- REJECT;
- stats;
- diagnostics;
- raw source chatter.

The public channel must not mirror TEST.

## Phanes / relay

A separate workstream handles downstream CA forwarding/rendering.

Known lesson: sender-ID/filtering bugs can make parsed calls fail to forward even when DMO itself worked.

## Railway

Railway has been the working publisher/cloud component in several phases.

Known publisher issues:

- forwarding too much TEST content;
- closed PostgreSQL connection requiring restart/recovery.

These are operational, not opportunity-selection defects.

## Local PostgreSQL

PGDATA:

`D:\dmo-call-aggregator\data\postgres-test-cluster`

Binaries:

`D:\dmo-call-aggregator\data\postgresql-test-tools\pgsql\bin\`

Host/port:

`127.0.0.1:55439`

## Active Rug runtime

```powershell
Set-Location 'D:\dmo-rug-defense'
& 'D:\dmo-rug-defense\.venv\Scripts\python.exe' 'D:\dmo-rug-defense\main.py'
```

Expected safety state:

- TEST_CHANNEL;
- trading disabled;
- Rug Defense SHADOW.

## Hosting experiments

### Railway
Working reference, but full persistent hosting cost is a concern after trial.

### Northflank
Free sandbox investigated; real persistence/connectivity and card verification had to be proven before migration.

### Botkeep
NO-GO for migration due unreliable worker/Postgres/start/recovery behavior.

## Rule

> **Cloud hosting is an operational requirement, not a reason to rewrite DMO.**

Accepted local latency baseline: ~6.60s median / ~13.18s p95.

A later cloud run reported roughly ~9.31s median / ~13.87s p95.

Long-term target: persistent phone-only operation at $0 recurring infra if possible.
