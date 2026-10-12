---
title: DMO — GemBot Reverse Engineering
project: DMO
status: experimental
updated: 2026-10-13
tags: [DMO, GemBot, reverse-engineering]
---

# DMO — GemBot Reverse Engineering

## Goal

Reverse engineer only GemBot's **calling edge**, especially early Premium / Ultra-Risky style calls.

Do not copy its UI, branding, charts, or presentation.

## Workspace

`D:\gembot-recon`

## Progress

Reported work includes:

- ~100 historical Premium artifacts reconstructed/collected;
- real fields such as `callAtMs` and `callMcUsd`;
- rough observed cap-floor patterns around ~$7K / ~$20K;
- one deeply decoded pre-call burst;
- preliminary live selector;
- separate activity/freshness experiment;
- prospective sampling;
- only a very small number of confirmed real GemBot matches;
- insufficient negative/control evidence for a validated clone;
- selector paused at latest retained checkpoint.

## Experimental policy

Primary frozen experimental policy reported:

`capfloor-only-7k-v1`

Conceptually:

- below ~$7K → PASS/not-call;
- at/above ~$7K → experimental CALL;
- unsupported/missing → WATCH.

This is not production logic.

## DMO shadow adapter

Reported additive files:

- `D:\dmo-rug-defense\dmo\gembot_shadow.py`
- `D:\dmo-rug-defense\scripts\gembot_shadow.py`
- `D:\dmo-rug-defense\docs\DMO_GEMBOT_SHADOW.md`

Safety:

- no production authority;
- no active publication hook;
- `publication_eligible = false`.

## Transplant rule

A GemBot-derived feature may enter DMO only after:

1. point-in-time reconstruction;
2. positive vs negative/control comparison;
3. prospective validation;
4. runner-preservation testing;
5. proof it adds signal beyond current DMO/source information.

## Why it matters

LUCKY shows the potential value:

- DMO saw it but promoted late;
- GemBot marked it much earlier.

GemBot research may help **promotion timing**, but it must not weaken Rug Defense or silently replace DMO logic.

## Status

> **Promising, active research. No validated GemBot clone yet.**
