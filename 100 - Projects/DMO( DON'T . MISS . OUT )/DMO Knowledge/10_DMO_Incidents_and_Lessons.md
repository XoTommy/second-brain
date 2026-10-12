---
title: DMO — Incidents & Lessons
project: DMO
status: living-log
updated: 2026-10-13
tags: [DMO, incidents]
---

# DMO — Incidents & Lessons

## NEWSOM

Problem: EARLY WATCH could publish through severe deterioration / missing valuation / low liquidity / ambiguity.

Fix: `388b0565` CurrentState fail-closed safety and pre-send validation.

Lesson: stale/incomplete market state cannot authorize positive publication.

## Chain alias issue

`sol` vs `solana` mismatch affected fast/pre-send paths.

Final acceptance sequence ended at `4e72f7b`.

Lesson: provider identity normalization is correctness-critical.

## AA

`3TFxV7N9oARQb8Ne6f936W3LKzerMSqvaG4a6qj7pump`

Known later coordinated destructive exit.

Lesson: later evidence can inform future tokens, not rewrite earlier history.

## CYBERPIN

`7GM6QjXd1VbzWbHqSZK1mP6cYmVorh7wm9kJfwttpump`

Known later coordinated consolidation/sale.

Lesson: chronology matters; prior AA history is only usable after it existed.

## 9LIVES

`AqUPRnyFCRuMqKYgY5Tf64CFshFecuaGSGXx4cqqpump`

Original PASS, later collapse.

Forensic result: `NOT_PROVABLE` prospectively; extended check UNKNOWN.

Lesson: many holders do not prove many owners, but do not fabricate a common controller.

## ZKINU

`DGdmHacFYkfrazHYtFEPtAbRnSru8db5cNyQkgY6QsQV`

Source called around ~$40K; later observed much higher.

Lesson: prove whether miss was capture/parser/admission/gate/data/queue/publication before changing logic.

## LUCKY

`H1hqLeM7YWs2JFHFJWkbQAcLyPh7DWfn7aUCwtGdpump`

DMO saw it early but only later emitted EARLY WATCH around ~$186K while catalyst/official attribution remained missing.

GemBot marker appeared around ~$17K.

Lesson: discovery worked; promotion was late. Market earliness must matter more than internal workflow labels.

## Source-network lesson

More channels ≠ more intelligence.

Keep active/selective/early/unique sources; remove trench feeds only after counterfactual runner-loss analysis.

## General debugging rule

For every live miss/failure:

1. freeze original evidence;
2. reconstruct point-in-time decision;
3. identify exact root cause;
4. implement smallest fix;
5. test runners + rugs + false positives;
6. keep future outcome out of historical logic.
