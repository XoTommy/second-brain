---
title: "DMO — Ultimate Product & Architecture Synopsis"
project: DMO (Don't Miss Out)
version: "2.2 — Cross-Chat Master Operations / Live-Beta"
status: "Product source of truth; implementation claims require repository verification"
date: 2026-10-13
tags:
  - DMO
  - product-spec
  - V1
  - V2
  - V3
  - crypto-intelligence
---

# DMO — Ultimate V1 / V2 / V3 Product & Architecture Synopsis

> **DMO = Don't Miss Out.** Discover potentially meaningful crypto opportunities **before their significance becomes obvious**, investigate *why* they might matter, verify identity and claims, assess risks and uncertainty, surface a small number of useful findings, track real outcomes, and improve. DMO is an intelligence and research system—not a guarantee of profitable trades or a service that blindly copies calls.

**Document authority:** This is a revised product specification based on the previous 66-section synopsis and the PAID discussion. It describes **what DMO must do**, not a claim that every capability is already operational. Features, providers, and factual token claims require separate verification. The previous synopsis remains historical background; use this version to judge future work.

---

## 0. The correction that governs everything

Our original direction was early discovery and meaningful investigation. During implementation, a narrow rule—two observations with rising price and liquidity—became the main demonstrated path to `WATCH` / `REVIEW_CANDIDATE`. That tests a useful market-evidence component but **does not test DMO's core product**. The correction is not to discard working infrastructure; it is to put early discovery, identity, narrative/catalyst research, risk checks, and time-valid assessment at the center of V1.

**Non-negotiable requirements:**

1. **Discovery does not require confirmation by the crowd.** No whale purchase, Smart Money entry, KOL mention, volume spike, or rising price/liquidity is a mandatory precondition for opening an investigation or entering a provisional early-research shortlist.
2. **Early does not mean good.** A recognizable name, website, X account, low market cap, or convincing story does not establish authenticity, safety, demand, liquidity, or profit potential.
3. **Research is part of the actual V1 workflow.** It cannot exist only as a schema, unused module, optional prose field, or V2 aspiration. Where automated research is unavailable, V1 must explicitly route the case to a bounded human-assisted research step rather than pretending it completed one.
4. **Separate discovery, research priority, assessment, publication, and trading.** Being worth investigating is not being approved to publish; being published as research is not a buy recommendation.
5. **Preserve the information boundary.** A backtest may use only data demonstrably available at its historical decision time. Future outcomes cannot be fed backward into decisions.
6. **Evaluate failures as carefully as winners.** Count missed discoveries, late alerts, rejected winners, promoted failures, scams, liquidity failures, costs and feasible exits—not merely maximum chart multiples.
7. **Reuse before building.** Inspect the code, connect existing capabilities, and patch the smallest demonstrated gaps. Do not rebuild the project, invent an arbitrary 0–100 score, or add infrastructure to avoid evaluating product behavior.

### What “pre-Smart-Money” actually means

DMO seeks evidence that can exist **before major wallet/KOL/crowd attention**: a new launch, timely product, authentic official relationship, understandable mechanism, emerging narrative, entity connection, distinctive token structure, or relevant public catalyst. Wallet/flow/volume data are useful as risk evidence, evolving context, or later confirmation. Some early activity is already wallet activity; the goal is not a metaphysical guarantee of being first, but to avoid making large-wallet arrival the *required discovery trigger*.

---

# PART I — PRODUCT CONTRACT

## 1. North star and product boundary

DMO's loop is:

```text
SENSE → DISCOVER → IDENTIFY → PRIORITIZE RESEARCH → INVESTIGATE
→ VERIFY → CONTEXTUALIZE → CHECK COUNTER-EVIDENCE → ASSESS
→ NOTIFY (only when justified) → REVISIT → TRACK OUTCOME → LEARN
```

The system must be able to answer, at the relevant historical time:

- **How did we first notice it?** Source, discovery timestamp, token identity and market-cap context if available.
- **Why might it matter?** Project/product, meme or narrative, catalyst, original source and mechanism. “Price went up” is not a sufficient standalone answer.
- **What is verified, merely claimed, contradicted, or unknown?** Especially contract-to-project identity and security.
- **Why investigate now rather than wait?** Novelty, catalyst freshness, material information, and potential opportunity to research before broad attention—not an assumed profitable entry.
- **Why promote, continue watching, filter, or decline to publish?** Evidence references, risks, unknowns, and explicit conditions for reassessment.
- **What happened after the decision?** Feasible outcomes, not hindsight-selected peaks.

DMO is **not** a Telegram firehose, generic chatbot, raw price scanner, whale/KOL copier, automatic trade execution system, or guaranteed 1.5x/2x service. Trading remains an external user decision.

## 2. Version ladder: one system, three maturity stages

| Stage | Purpose | Discovery | Investigation | Product output |
|---|---|---|---|---|
| **V1 — Revenue Engine** | Useful, low-cost early research and a defensible shortlist | Automatically ingest configured Telegram feeds; use supported GMGN discovery feeds where feasible; manually supplied tokens also accepted | Bounded, rule-guided identity, project/narrative/catalyst and risk research, including clearly labeled human-assisted steps if needed | Selective early research/watch notifications; transparent tracking and outcomes |
| **V2 — Intelligence Engine** | Adaptive, more discriminating investigations | Expand candidate generation and proactive targeted scanning | Agent selects tools, tests hypotheses and counter-evidence, optimizes depth and rechecks | Better timing, source reliability, wallet/narrative reasoning and learning |
| **V3 — Ultimate Intelligence System** | Continuously discover what humans did not point out | Continuous multi-source on-chain, social, ecosystem and public-information sensing | Autonomous investigations and evolving memory/model capabilities, subject to evidence and safety controls | Proactive, continuously updated intelligence platform |

**Clarification of the old slogan:** “V1 investigates what we tell it to investigate” means *configured sources and explicit inputs define V1's discovery universe*, **not** that a human must manually paste every address or wait until a token pumps. V1 should automatically ingest its configured feeds and open bounded investigations. V2 chooses its additional research; V3 expands autonomous discovery beyond preselected universes.

V1 must not become a multi-year project. It also must not be called product-ready merely because its components pass unit tests.

## 3. Discovery is separate from market confirmation

Candidate input types:

1. **Telegram discovery:** configured channel alert; retain exact original message, event/message time, receipt time, contract/chain, links, source and edits when available.
2. **GMGN-based discovery:** supported token/market/trending/new-pair views if independently validated, rate/cost bounded and explicitly enabled. A market endpoint by itself is not a continuous on-chain scanner.
3. **Human-supplied research:** contract, website, announcement or thesis. Mark discovery as manually supplied; do not claim autonomous detection.
4. **V2/V3 expansion:** target-specific wallet/flow monitors, public announcements, broader social/ecosystem scanners, and eventually independent on-chain event monitoring.

Candidate-generation criteria may include a new deploy, publicly announced launch, authentic official relationship, new usable product, verifiable fee/buyback mechanism, narrative-to-token link, unusual early distribution, a trusted source's early alert, or wallet activity. **No single candidate criterion is a trading endorsement.**

A token with zero prior GMGN snapshots, no whale, or quiet socials can still be `RESEARCH_NOW`. A token with a soaring chart can be rejected for unverifiable identity, security risk or uneconomic exit.

## 4. Priority and valuation policy

Preferred early-discovery context: **below $50K; $50K–$100K; $100K–$250K; $250K–$500K; $500K–$1M; $1M+**. The under-$100K objective expresses *timing interest*, not proof of quality, a mandatory cutoff or an unconditional entry rule. Higher-market-cap continuation ideas remain eligible when the relevant opportunity is still early in its own lifecycle.

Record market cap as **reported** or **verified**, with provider, observation time and unit. If unavailable, say `unknown`; never substitute liquidity, FDV or a social post as verified market cap. Record liquidity separately. At very small sizes, assess whether a real order and exit are plausible under fees, price impact, token restrictions and liquidity conditions.

## 5. What counts as “official” or a real narrative

Identity verification is an **evidence chain**, not visual polish:

```text
Canonical token contract ↔ linked project/issuer/account
↔ time-stamped website or social claim ↔ independent corroboration where available
```

Check reciprocal links, account history, domain provenance where accessible, project-announcement timing, on-chain deployer/ownership connections where supported, impersonation and recycled branding. A website and X profile can exist at launch while their **authenticity, ownership and statements remain unverified**.

Narrative types include: project/product utility, official entity connection, public announcement, ecosystem theme, cultural meme, creator/community association, infrastructure launch and time-bound event. Do not require traditional utility for every meme, and do not treat a professional website as a quality guarantee.

For each narrative/catalyst preserve: *what is claimed; who said it; the exact token link; publication and observation times; mechanism by which it might matter; what was verified; counter-evidence; what is still unknown; freshness and possible failure conditions*.

## 6. Market data, wallets and KOLs: correct roles

Market metrics contextualize price, liquidity, holder growth, transaction behavior, price impact and feasible exit. Historical deltas are valuable when samples exist but **a missing baseline is not a research rejection**.

Wallet intelligence examines deployer history, top holders, bundling, clusters, insiders, concentration, early exits, repeat wallets, Smart Money and KOL participation. “Smart Money absent” is not automatically negative for an *early* candidate. Smart Money present is not automatically positive; wallets may be late, linked, spoofed, illiquid or exiting.

KOL reach, social interest and volume acceleration can indicate diffusion or crowding. Do not require them for discovery; do not confuse their presence with independent proof of the project narrative.

## 7. Evidence and provenance

Classify records as `FACT / OBSERVATION / SOURCE CLAIM / HYPOTHESIS / INTERPRETATION / ASSESSMENT`. Keep raw messages, responses and citations where permissible. For material evidence store:

- canonical `chain + contract_address` and related entity/account/URL identity;
- evidence source, exact retrieval path, event/publication time **if known**, acquisition time, persistence time, availability and freshness;
- raw content or reproducible reference, normalized metric/unit and interpretation;
- identity link strength, independent corroboration, counter-evidence, uncertainty and investigation/decision ID.

Distinguish publication time from collection time. Do not impute unavailable provider timestamps. Repeated GMGN samples from one provider are longitudinal data, **not independent-source corroboration**. Two 24-hour rolling aggregate totals do **not** reveal activity exclusively between their sample times.

Market windows must state `minimum_horizon`, selected baseline/latest, actual elapsed and timestamp basis; reusing a pair across multiple horizons is **not multiple independent confirmations**.

## 8. Two different state dimensions (do not conflate them)

**Investigation lifecycle** tracks work: `DETECTED → IDENTIFIED → RESEARCHING → PARTIALLY_VERIFIED → REASSESSING → RESOLVED`, with explicit unknown/error paths. Longer-term token lifecycle may include discovery, formation, expansion, acceleration, distribution, exhaustion and decline **only when evidence supports those states**.

**Opportunity/communication decision** governs what to do now:

| Decision | Meaning | May it notify? |
|---|---|---|
| `INVALID_CANDIDATE` | Identity conflicts or fundamental invalidity; retain why | No positive alert |
| `INSUFFICIENT_EVIDENCE` | Material information absent; distinguish missing data from disproven thesis | Optional internal research queue, no positive claim |
| `RESEARCH_NOW` *(product requirement; implementation may use an equivalent existing state)* | Time-sensitive identity/narrative/catalyst or structural observation justifies immediate inquiry **without momentum requirement** | Internal/operator research alert only |
| `CONTINUE_WATCHING` | Plausible but unresolved; revisit on defined evidence or time | Watch update, not endorsement |
| `REVIEW_CANDIDATE` | Identity-linked evidence and risk review justify operator review; reasons and unresolved items explicit | Provisional research shortlist; not automatic trade call |
| `FILTERED` | Documented risk/disqualification or low evidential relevance, with reasons | No positive alert; revisit if conditions change |
| `APPROVED_FOR_PUBLICATION` *(future explicit gate, not current claimed functionality)* | Meets documented disclosure/risk/evidence rules and operator/policy controls | Publish factual alert appropriate to verified content |

**Compatibility note:** The existing implementation reportedly exposes `INVALID_CANDIDATE`, `INSUFFICIENT_EVIDENCE`, `CONTINUE_WATCHING`, `REVIEW_CANDIDATE` and market-based shadow `WATCH`; it does not yet implement all states above. Map new product semantics to existing interfaces only after code inspection. Do not rename schemas or claim `APPROVED` is already reachable. A provisional market-only `REVIEW_CANDIDATE` is not a fully researched candidate.

The reason a case was discovered and the reason it qualifies for publication must be different, separately auditable fields.

## 9. Decision hierarchy: no arbitrary score

1. **Identity and integrity:** known chain/address, token-contract linkage, provenance, obvious impersonation or contradictory facts.
2. **Hard-risk gates:** documented and evidence-supported inability to sell, malicious controls, dangerous mint/freeze permissions, critical holder/deployer concentration or liquidity risks, etc. An unknown security field is *unknown*, not a clean bill of health. Risk conclusions must respect chain-specific relevance.
3. **Early thesis:** what novel, timely, identity-linked narrative/project/catalyst or early structural feature merits investigation, and why now?
4. **Counter-evidence:** bundlers, insider sales, manufactured volume, false official claims, dilution, lack of actual product, stale catalyst or misleading social attention.
5. **Market/execution context:** market cap, liquidity, spread/price impact, taxes/fees, temporal trends, holder dynamics and source limitations.
6. **Decision with explicit uncertainty:** research now, watch, review, filter or publish as permitted; preserve exact reasons and recheck triggers.

Do **not** build an arbitrary 0–100 opportunity score or tune cutoffs using a single successful token. Calibrate over a prospective cohort with real failures. Hard gates must be documented and tested; a mere “80 bundlers” claim warrants verification, not a fabricated universal percentage rule.

## 10. Publication is a distinct product decision

Premium output should be **few, early, explainable, timestamped, honest**. Candidate fields: identity; discovery source and time; market cap and liquidity *with measurement time/source*; why it matters; original project/catalyst evidence; what has been verified; risk flags; what is unknown; current state; the next evidence needed; chart/research links; and outcome tracking.

Mark `EARLY RESEARCH`, `PROVISIONAL WATCH`, `FOLLOW-UP`, or `RESULT` visibly. Do not style an unreviewed signal as an approved buy. Historical win banners must tie to actual alert time/entry reference, executable prices where possible, stated methodology and costs; maximum chart multiple is not realized user return.

A Telegram source can trigger discovery; its message must not be treated as automatically verified or automatically republished as proprietary original research. Check source terms, attribution rights, permission and applicable financial-promotion obligations before commercial redistribution.

---

# PART II — V1: REVENUE ENGINE

## 11. Mission and V1 promise

> **Find research-worthy tokens early within our bounded sources, investigate the real story and risks promptly, surface a selective and defensible shortlist, and track every subsequent outcome.**

V1 stays low-cost/₹0 infrastructure where practicable. No mandatory paid AI/API, no Grok requirement, no custom model training or blockchain-wide indexer. A human-assisted research checkpoint is preferable to fake automation, but clearly label operator work and its timing. The V1 product must remain valuable for independent research even if subscriptions do not sell.

### V1 minimum viable end-to-end behavior

```text
CONFIGURED TELEGRAM / VERIFIED GMGN DISCOVERY / MANUAL INPUT
→ CANONICAL IDENTITY + FIRST-SEEN RECORD
→ IMMEDIATE EARLY-RESEARCH PRIORITY (NO MOMENTUM GATE)
→ PROJECT / WEBSITE / X / NARRATIVE / CATALYST INVESTIGATION
→ GMGN MARKET + SECURITY + HOLDER / WALLET CONTEXT AS AVAILABLE
→ CONTRADICTIONS, BUNDLERS, LIQUIDITY AND EXECUTION RISKS
→ SELECTIVE TRIAGE + OPERATOR RESEARCH REPORT
→ EXPLICIT PUBLICATION DECISION
→ BOUNDED REVISITS + RESULTS + AUDITABLE LEARNING
```

“Investigation” is a real operation producing sourced findings or explicit unanswered questions. Creating an empty evidence object is not completing it.

## 12. V1 discovery universe and ingestion

Existing source set:

- Green onions 🎲 Gambles
- KOL SignalX
- AI CALL | Ponsfamily Alert
- Alpha X100 Callers
- Robinhood Signal X

Normalize chain/address, preserve original post and timestamp, deduplicate exact token identity while preserving distinct events/edits/sources, and record the earliest **observed** discovery time. A duplicate token may contribute genuinely new information even if it does not create a new candidate. Source convergence requires evidence independence; copied calls are not independent.

GMGN skills/CLI are a foundational tool layer throughout V1, **not a synonym for autonomous discovery**. Validate each live capability separately: supported chains, actual CLI commands and fields, permissions, units, rate limits, latency and history availability. Only enable discovery acquisition after a bounded request budget and operating contract are verified. DexScreener can supply suitable market/pair context as already integrated where applicable; neither provider automatically proves identity or price-at-time.

Target chains in product scope: Solana, Robinhood Chain, Base, BNB Chain, Ethereum and Monad, subject to actual provider/adapter support. Do not advertise day-one coverage for a chain without an end-to-end verified path.

## 13. V1 research sequence and latency tiers

**Tier A — immediate, cheap, bounded:** parse identity, detect contract conflict, extract linked URLs and exact source claims, check first-seen/cap context, quick obvious-risk flags; create `RESEARCH_NOW` when the thesis is time-sensitive. This happens **before** requesting a second market observation.

**Tier B — targeted verification:** official-project/contract link, website/X history and announcement timing; product/fee mechanism; current supported token security, deployer/top-holder/bundler checks; market and feasible exit. Where website/X access or APIs are unavailable, create a concrete operator research item and mark `not_attempted` or `unavailable`—never auto-fill a narrative from a ticker.

**Tier C — bounded recheck:** revisit unknowns, first credible market baseline, catalyst progression, liquidity/holder changes, risks and outcomes. Stop investigation when further queries cannot change the immediate decision enough to justify cost/latency.

The order is **risk- and information-sensitive**, not a requirement to execute every GMGN skill for every token. Research may run concurrently or asynchronously only when proven safe and bounded; do not block Telegram indefinitely or exceed budgets.

## 14. V1 catalyst, narrative and product research

For each discovered token, attempt to establish:

- **Identity:** token contract ↔ project website ↔ official or claimed X account; exact supporting links and time.
- **Nature:** product-backed, project-associated, community meme, themed derivative, impersonation or still unknown; no forced utility requirement.
- **Catalyst:** announcement, launch, feature, distribution, listing, event, fee-routing, partnership or other checkable event; exact original claim and age.
- **Mechanism:** why the event could affect attention or demand, while separating inference from facts.
- **Verification:** original announcement or archive, product behavior, relevant on-chain transactions and independent confirmation where accessible.
- **Failure/countercase:** project disavowal, unrelated contract, recycled site, broken product, fake volume, manipulated distribution, token controls, stale narrative, unattainable exits.

Catalyst evidence records and investigation-history infrastructure should be **connected to actual acquisition**, not merely exist as models/stores. Missing external access can legitimately leave a candidate provisional or stop publication. V1 can work with a human-assisted verification step; it cannot claim an automated site/X investigation that never ran.

## 15. V1 GMGN and wallet intelligence

GMGN capability categories (verify each availability and response contract): token/market metrics; security; holders and concentration; deployer/creator; transactions/trades; wallet histories and clusters; Smart Money; flow; historical data. Provider-agnostic internal adapters should preserve provider-specific field meaning and evidence source. Normalizers without runtime acquisition are not a delivered feature.

Apply wallet research to distinguish skilled repeatability from one-off luck, early entrants vs late exits, insider/bundler clusters, size and copyability, and conflicts with project narrative. Do not make a Smart Money signal mandatory for early research. Later wallet arrivals can confirm, contradict or reveal crowding.

Security review: document authority fields, token-sale restrictions when verifiable, honeypot applicability, liquidity controls, creator distribution and unknown fields. Avoid treating missing rug/honeypot values, a null open-source flag, or chain-inapplicable tests as evidence of safety. No “verified safe” promise.

## 16. V1 market observations and temporal evidence

Preserve immutable actual observations, deterministic identity, provider/source/acquisition/persistence times and available metric units. Compare price/liquidity/holders only when the observations and definitions are semantically compatible. Treat 24-hour rolling buys/sells/volume as overlapping-window snapshots, not interval flow.

Current market shadow `WATCH` can remain a **supporting route** to additional review. It must not be the *only* route to investigating a token with a verifiable early catalyst. Lack of a price/liquidity baseline should set the **market momentum dimension** to unknown, not automatically suppress narrative-driven research.

Distinguish: source-reported Telegram cap; verified provider market cap; market cap at first DMO detection; market cap at research completion; cap at any public alert; later peak or exit. Do not collapse these into one “entry MC”.

## 17. V1 convergence, contradictions and uncertainty

Basic Catalyst Radar asks: “What identifiable, time-valid event or project relationship might matter?” Flow Radar asks: “What is actually happening with wallets and capital?” Convergence Radar asks: “Do different *independent* evidence types strengthen or weaken a thesis?”

**No convergence requirement for initial research:** a new catalyst may precede all visible flow. A second copy of the same Telegram claim is not independent verification. Missing independent corroboration should be visible; it is not always a reason to ignore an emerging candidate. Contradictions and uncertainty must remain prominent at assessment and publication.

## 18. V1 result and operating data

Persist the investigation, not just the answer: trigger, source message, time boundary, used tools, original evidence and facts, narrative/catalyst hypothesis, counter-evidence, decision and version, publication/withheld status, recheck triggers and subsequent outcome. Stores must be useful in operation; persistence schemas alone are insufficient.

Outcome checkpoints may include 5m, 1h, 6h, 24h, 3d and 7d, subject to real data availability. Track *all* candidates including filtered and never-published; otherwise we cannot estimate missed opportunities and false positives. Record invalid/unknown outcomes honestly.

The existing in-house tracker and banners may report token movement but cannot label a return realized without a plausible execution model. Track before/after fees and slippage where inputs exist; tax treatment is jurisdiction- and circumstance-dependent, so show assumptions rather than invent a net-tax return.

## 19. V1 monetization and ethical product claims

Private Telegram offers curated, transparent intelligence, not certain returns. Free/public output can show responsibly qualified historical outcomes with unambiguous initial timestamp and methodology. Subscription pricing and payment rails are separate commercial decisions; availability, consumer protection, intellectual-property, financial-promotion and applicable tax issues require verification for the actual customer jurisdictions.

Operational goals: low cost, fast to launch, low noise, honest provenance, repeatable process, actual demand and revenue validation. Do not claim “proven profitable”, “safe”, “guaranteed 2x”, or that chart highs equal sellable gains.

## 20. V1 must-not-build list

Defer full autonomous agent swarms, full-chain indexers, huge knowledge graphs, sophisticated custom training, elaborate GUIs, self-improving production models, speculative wallet predictions and unnecessary infrastructure. Reuse existing sampler, assessment/evidence, tracker, publisher and stores where appropriate **after checking what is wired and enabled**. Avoid new ledgers/workers without a demonstrated operational need.

## 21. V1 product acceptance criteria — mandatory

V1 is not accepted because it has N passing tests. It needs observable end-to-end demonstrations:

| Test | Acceptance evidence |
|---|---|
| **Early discovery** | Running configured feed produces correct token identity and earliest recorded discovery time; no market pump prerequisite. |
| **First-snapshot research** | A new token with zero market history can enter a meaningful research queue based on time-valid identity/narrative/catalyst evidence; uncertainty explicit. |
| **Genuine investigation** | Available site/X/project claims, verification attempts, security/holder/market context and countercase are recorded, or each unavailable step explicitly noted. |
| **Selective decisions** | Cohort includes `RESEARCH_NOW`, watching, filtered and insufficient cases with grounded reasons; not all forwarded calls become premium alerts. |
| **Risk** | An attractive narrative with serious verified danger does not bypass documented safety/publication controls. |
| **Time integrity** | Historical and live decisions cannot consume later social posts, market values or outcomes. |
| **Latency** | Measured detection → research-start → report → publication delays; sample at actual receipt time, not an invented historical time. |
| **Outcomes** | Count every eligible token, failures and unavailable exits, fees/slippage assumptions, and both missed and promoted opportunities. |
| **Operational safety** | Request budgets, disabled-by-default optional tasks, no accidental sends/trades, durable bounded state, recovery behavior and protected credentials. |
| **Product value** | Real operator can explain why each surfaced candidate was timely, what is verified, what is risky, and what is not known. |

Initial pilot should be a **small, precommitted prospective cohort** rather than choosing PAID-like winners after the fact. Calibrate only after observing successes and failures. No guarantee that a usable edge will appear.

## 22. Current reported implementation — status, not a spec claim

From the latest Codex reports in this conversation, **not independently re-audited here**:

- Telegram parser/normalization/dedupe/publisher and tracking foundations exist.
- GMGN token-info investigation, immutable observations, temporal evidence, catalyst/evidence/report-related components and shadow/triage paths are present in some form.
- A controlled two-snapshot PAID experiment showed successful acquisition/persistence and a market-based provisional `WATCH` → `REVIEW_CANDIDATE` state. It was **not early discovery, narrative investigation, a launch-time backtest or a profitable call**.
- Operator labels were corrected to say `minimum_horizon`, actual elapsed and rolling-24h aggregates; Codex reported 661 tests passing after that patch.
- Revisit sampling is reportedly implemented but disabled by default, and a commercial-quality automatically connected site/X/project/catalyst research path has **not been demonstrated**.
- There is no demonstrated blockchain-wide scanner or fully researched multi-candidate shortlist; no claim that `APPROVED` or a safe profitable signal is operational.

**First implementation action:** audit exactly where an incoming candidate goes from parser to actual identity-linked project research, risk review, triage and publication. Connect or repair the smallest missing path. Do not begin by constructing another store or tweaking the rising-price rule. Maintain production isolation and get explicit authorization for bounded live requests and Telegram actions.

---

# PART III — PAID AS AN ADVERSARIAL PRODUCT TEST

## 23. The historical case, without hindsight

Token: Solana `98kfF7rmsg1QDUEoCqNE7g7M1FdrTt92TEp2CLzypump` (PAID). User supplied a Green onions 🎲 Gambles alert reported at **September 16, 12:54 a.m. (timezone not yet confirmed)**. Its latest displayed source snapshot said approximately **$35.5K MC**, 307 holders and 5-minute buys/sells 285/138; an earlier source snapshot in the same post displayed **$47.3K MC / $18K liquidity**. The post also says “since our signal”: a prior alert may exist, so this is an *observed post*, not proven first-ever discovery or executable entry.

The user directly observed a linked project website `https://usepaid.app/` and X account `https://x.com/UsePaid` at launch. This is **valuable firsthand historical context, not independently archived proof of their exact contents, contract linkage or authenticity at 12:54 a.m.** The source reported substantial bundler participation (80 of top 100), concentration and selling, thin social attention, limited Smart Money and other risks. These remain *source claims* until checked against time-valid evidence.

### What an honestly capable V1 would have done then

1. Ingest and timestamp the Telegram alert, preserve exact content, identify Solana contract and linked website/X. Check whether an earlier alert exists.
2. Start early research immediately **at the contemporaneous reported market-cap context**, without waiting for a whale, another KOL, volume spike or a second GMGN observation.
3. Verify or mark unknown: token ↔ project website/X association, product claim and launch timestamp, catalyst, developer/insider/bundler structure, security, liquidity and feasible exit.
4. Create a justified `RESEARCH_NOW`/provisional watch if the identity-linked early thesis warrants work; withhold stronger publication until required risk and factual checks are met.
5. Obtain time-valid market observations and reassess as evidence arrives; preserve initial analysis separately from later success or collapse.

### What the historical case does **not** prove

- That DMO was running and actually ingested the alert; that it independently found the token; or that a user could buy at exactly $35.5K MC.
- That the website was genuine or the described mechanism operational at the source timestamp.
- That a historical GMGN snapshot and risk data are retrievable; that a preconfigured policy would have promoted or published PAID at that moment.
- That subsequent chart gains were feasible after liquidity, fees, price impact or taxes.

**Backtest label: `EARLY SOURCE DISCOVERY DOCUMENTED; DMO HISTORICAL DECISION INDETERMINATE`.** PAID is a useful falsification test for “only promote rising price and liquidity,” not proof of a winning system. Build a matched collection of unsuccessful contemporaneous alerts rather than optimizing around this success story.

---

# PART IV — V2: INTELLIGENCE ENGINE

## 24. Mission and difference from V1

> V2 chooses *what to investigate next* and how deeply, using missing-information detection, explicit costs and uncertainty reduction—not merely executing an endless fixed checklist.

V1's guided research, evidence and results become the foundation. V2 should select GMGN or other verified tools as needed, test alternative hypotheses, challenge official-identity claims, detect contradictions, decide when evidence is adequate and revisit candidates on meaningful changes. It must preserve all V1 early-discovery, risk and no-hindsight protections.

## 25. Agentic investigation policy

A bounded investigation agent should:

```text
Trigger → initial hypothesis and alternatives → inspect known evidence
→ identify the decision-critical unknown → choose permitted tool
→ verify provenance and contract linkage → seek counter-evidence
→ update interpretation → decide next inquiry or stop → explain result
```

Cost, latency, rate limits, data freshness, privacy and failure modes are part of tool selection. No automatic production trades or unbounded web/API use. Model-generated statements are hypotheses until grounded. A model should never silently convert missing retrieval into a positive catalyst.

## 26. Advanced catalyst and narrative intelligence

Track catalyst **first announcement, subsequent verification, changing relevance, failure and resolution**. Model relations among issuer/entity, contract, product, announcement, meme theme, wallets, attention and token behavior. Assess identity authenticity and time availability separately from narrative popularity. Detect an emerging legitimate product before it trends without assuming that legitimacy ensures positive price performance.

## 27. Advanced flow and wallet intelligence

Extend V1 wallet foundations to recurring trader quality, selection/timing, execution size, source-of-funds linkage where lawful, clusters, insiders, distribution, accumulation and market impact. Compare time-bound histories and outlier dependence rather than cherry-picked wins. Distinguish observed wallet actions from speculative intent.

### Wallet Watchout / Next-Play Radar

Watch wallets potentially relevant over the next **24–48 hours**, using 1D/3D/7D/14D behavior: recent plays, timing patterns, entry sizes, selection, exits, repeatability, activity bursts, narrative association and relevant historical failures. Output is **“watch this wallet because of these measured patterns,” not “this wallet will buy token X.”** Validate forward in time; estimate and label uncertainty rather than asserting certainty.

### Large-wallet early-arrival radar

Detect meaningful wallet participation with no obvious public catalyst, investigate why, and check whether it is early or already crowded. This is **one candidate route**, not the V1/V2 prerequisite for finding worthwhile narratives before whales.

## 28. Advanced convergence and source reliability

Weight evidence quality, timestamp alignment, contract identity, genuine source independence, contradictions and freshness. Multiple copies of one call remain one underlying claim. Track source false alarms and timing without training only on celebrated winners. Challenge model interpretations against raw records.

## 29. V2 memory and learning

Link successive investigations into an auditable timeline: initial thesis, later verification, Smart Money entrance, distribution, catalyst success/failure, downgrades and results. Preserve pre-decision features, tool traces and outcomes. Distinguish operator edits, source changes and model-generated hypotheses.

Evaluate on evidence quality, early timing, selective recall/precision tradeoff, risk detection, latency, feasible results, confidence calibration, abstentions, cost and no-hindsight compliance. Do not maximize “did chart eventually go up?” alone.

## 30. Soup and model-development laboratory

Soup is a potential environment for data/evaluation/model experiments, **not a reason to train immediately**. Sequence:

```text
Real investigations → time-valid evidence/tool traces → complete outcome cohort
→ data cleaning/leakage checks → train/evaluate candidate (SFT, LoRA/QLoRA,
DPO/GRPO/distillation only if useful) → held-out forward testing
→ compare against simpler baselines → promote only on measured improvement
```

One strong frontier model plus tools may outperform a specialized swarm. Specialized catalyst/wallet/narrative/risk/orchestrator models are optional experiments, never assumed necessary. Maintain provider/model replaceability and documented limits.

## 31. V2 exit criteria

V2 is justified when it demonstrably selects better targeted inquiries, reduces unnecessary calls, finds missing critical evidence and improves timely decision quality versus V1 on **the same prospective or leakage-safe historical cohort**, without sacrificing provenance or safety. Model training and autonomy are not themselves success metrics.

---

# PART V — V3: ULTIMATE INTELLIGENCE SYSTEM

## 32. Mission

> Continuously sense on-chain, Telegram, social, news and ecosystem information; originate investigations into relevant changes no one specifically requested; verify, contextualize, update and alert with measured uncertainty.

V3 is a continuing platform, not a final frozen release. Its central change is **autonomous candidate generation across broader environments**, not simply a larger model that asks GMGN more often.

## 33. Continuous discovery surfaces

- **On-chain:** new deployments, token creation, liquidity/pool events, meaningful wallets, holder shifts, transfers, security changes, flow and market dynamics across actually supported chains.
- **Market/GMGN:** emerging pairs, token/wallet intelligence, verified feeds and provider changes; distinguish polling coverage from full-chain monitoring.
- **Telegram:** calls, original-source timing, recurring sources, distinct events and narrative clusters.
- **X/social:** official announcements, new entities, narratives, attention shifts, creator and KOL activity; protect against impersonation and copied content.
- **News/public information:** launches, products, integrations, public events, partnerships and ecosystem developments.

Monitor bounded, documented coverage; expose blind spots, provider outages, geographic/time restrictions and detection latency. A broad scanner cannot truthfully promise every opportunity.

## 34. Autonomous discovery and hypothesis formation

```text
New or unusual verified observation → identity/entity linking
→ possible narrative/catalyst/market/wallet hypotheses
→ novelty and timeliness check → counter-evidence search
→ targeted tools → risk/feasible-exit check → ranked investigation queue
→ justified notification → revisit → outcome → learning
```

“Ranked investigation queue” here means internal prioritization by operational relevance/uncertainty, **not fabricated profit probability**. Use source provenance, causal restraint and safeguards against gaming by shills, spoofed wallets and synthetic engagement.

## 35. Knowledge graph and investigation memory

Maintain traceable links among entity, announcement, product, narrative, contract, liquidity pool, wallet, transaction and social claim. Each edge has source, type, earliest known time, validity and confidence; an LLM guess is not automatically a factual edge. Knowledge graphs are introduced only after simpler identity/event stores cannot meet measured needs.

## 36. Continuous risk intelligence

Detect weakening or falsified catalysts, wallet dumping, concentration, security/control changes, liquidity deterioration, fake engagement, source unreliability, stale claims, dangerous execution conditions and evidence that invalidates earlier alerts. Support explicit retractions/corrections, not just upside banners.

## 37. DMO models, training factory and deployment discipline

Possible roles: research, catalyst, wallet, narrative, risk, convergence and orchestration. Decide single versus specialist models experimentally. Preserve model registry, data/tool versions, held-out evaluations, failure cases, rollback, audit trail and human override. Soup may support SFT, preference methods, adapter tuning, distillation and evaluation **after** quality data exists.

Do not deploy a model just because it sounds more sophisticated. Use forward evaluations, leakage tests, calibrated uncertainty and regression checks. Custom models and continuous learning are optional means to better intelligence, not the end goal.

## 38. V3 business evolution

Potential products: fuller research platform, wallet watch, early alerts, professional terminal, historical evaluation, API and vetted intelligence data. Validate demand, licensing and operational economics before expansion. Preserve user trust through transparent corrections, risk disclosures and no inflated results.

---

# PART VI — SHARED TECHNICAL ARCHITECTURE

## 39. Layered system

```text
CONFIGURED FEEDS / MANUAL INPUT / AUTONOMOUS SENSORS (BY VERSION)
                           ↓
             DISCOVERY + FIRST-SEEN RECORD
                           ↓
               CANONICAL IDENTITY LINK
                           ↓
              EARLY RESEARCH PRIORITY
                           ↓
   ┌───────────────────────┼──────────────────────────┐
   │                       │                          │
PROJECT / NARRATIVE   GMGN / ON-CHAIN           MARKET / EXECUTION
CATALYST / SOCIAL     SECURITY / HOLDERS       PRICE / LIQUIDITY
   │                       │                          │
   └───────────────────────┼──────────────────────────┘
                           ↓
       EVIDENCE + PROVENANCE + COUNTER-EVIDENCE
                           ↓
         OPPORTUNITY TRIAGE / RISK / UNCERTAINTY
                           ↓
           HUMAN OR POLICY PUBLICATION GATE
                           ↓
           ALERT / FOLLOW-UP / CORRECTION
                           ↓
       PROSPECTIVE OUTCOME AND MISSED-CASE LOG
                           ↓
            EVALUATION / CALIBRATION / LEARNING
```

**Architectural invariants:** identity consistency; immutability of original evidence; provider abstraction; clear event vs acquisition times; side-effect isolation; repeatable decisions; evidence independence; versioned policy; guarded notification; retention of negative examples and explicit unknowns.

## 40. Tool/provider abstraction

Capabilities might include `get_token_data`, `get_market_data`, `get_token_security`, `get_holder_data`, `get_wallet_history`, `get_transactions`, `get_smart_money`, `get_flow_data`, `get_historical_data`, `get_official_claims`, `get_project_links`. These are **conceptual interfaces, not promises that GMGN provides or that code implements every method**.

Each adapter must document true availability, supported chain, auth needs, cost, rate, latency, schema, timestamps/units, source and failure modes. GMGN remains foundational but swappable behind stable internal contracts. X/social collection is not assumed free, reliable or authorized without validation. No hidden paid dependency in V1.

## 41. Data objects

- **DiscoveryEvent:** token identity, first observed time, source, original message/event, claimed links/cap, trigger type and provenance.
- **IdentityEvidence:** reciprocal project/token links, issuer/account relationship, timestamps, ambiguity and impersonation flags.
- **MarketSnapshot:** actual source/acquisition/persistence times, values, units, provider, immutable fingerprint and raw reference.
- **CatalystEvidence:** original claim/event, publisher, original/event/observation time, mechanism, verification and identity link.
- **RiskEvidence:** specific controls, holder/creator/bundler/liquidity facts, applicability, uncertainty and source.
- **InvestigationRecord:** why opened, what was checked, tool attempts/cost, hypothesis/countercase, missing evidence and temporal cutoff.
- **DecisionRecord:** state, distinct discovery/assessment/publication reasons, source evidence IDs, rule version, cutoff and operator action.
- **AlertRecord / OutcomeRecord:** what was actually sent, when and to whom/channel; later path, realized/feasible benchmarks, losses and uncertainty.

Use existing schemas where possible; additions require an actual missing use case. A record's existence does not prove the acquisition or decision pipeline is connected.

## 42. Operational safeguards

Explicit permission for live provider requests and publication, bounded concurrency/rate budgets, no retries after ambiguous network outcomes without authorization, isolated experiments, durable writes where needed, protected secrets and Telegram sessions, deterministic tests, production path hygiene, fail-closed publication for serious uncertainty, and observability that distinguishes discovery failure, research failure, unknown data and delivery failure.

Revisits should be triggered by relevant new evidence or bounded schedules; no uncontrolled polling. Respect provider terms and privacy. When tool usage is constrained, prefer a precise offline audit or an operator-assisted research task rather than building speculative code.

---

# PART VII — MEASUREMENT, BACKTESTS AND BUSINESS REALITY

## 43. The only honest historical replay

At candidate time `T`, reconstruct the **discovery universe** (what channels/feed could have been monitored), original message arrival, exact contract and links, available archived pages/posts and chain/provider data. Run only policy/code whose inputs can be shown available by `T`; simulate plausible acquisition and investigation latency. Separate later evidence and final price outcome into a sealed evaluation phase.

Classify replay quality:

- `VERIFIED_REPLAY`: reproducible point-in-time evidence and applicable policy;
- `PARTIAL_RECONSTRUCTION`: authentic early signal but essential historical inputs missing;
- `INDETERMINATE`: cannot support a decision claim;
- `LIVE_PROSPECTIVE`: actual timestamped running system, strongest future validation.

Never use today's site copy, current GMGN response, subsequent hype, retrospective “100x call” banners or a survivor-selected winner as launch-time proof. For PAID, source discovery is documented by the user-provided message; the DMO launch decision remains indeterminate until historical inputs and policy are established.

## 44. Metrics that actually measure the mission

Measure **per discovery cohort**, with denominators and missing data:

1. Discovery coverage and **first-seen latency**, including tokens later found important but missed by configured feeds.
2. Market cap/price/liquidity at first *observed* detection vs investigation completion vs first actual alert, only when supported by valid timestamps.
3. Time spent collecting identity, narrative/catalyst and security evidence; proportion with meaningful research rather than just a market snapshot.
4. Shortlist precision, recall and volume, plus filtered winners and published losers; differentiate “worth researching” from return performance.
5. Maximum favorable/adverse excursion **after feasible alert/entry**, 1.5x/2x reach and realized-exit assumptions, failure/sellability, liquidity, fees, slippage and taxes where supportable.
6. Independent verification, contradiction accuracy, source reliability, no-hindsight violations, incident rates, API cost and operating latency.

A sub-$100K alert is an achievement of timing, **not** evidence of profitability. A displayed 2x is not a guaranteed achievable 2x. Do not assert a win rate or financial edge before sufficient forward data exists.

## 45. Practical implementation sequence — no reset

**0. Freeze the corrected contract.** Save this synopsis. Do not spend the next coding session revalidating PAID's rising-liquidity rule or adding infrastructure.

**1. Small read-only repository-to-spec mapping.** Inspect configured discovery → first-seen → project/social research → catalyst/identity evidence → security/holder data → triage → operator output → publication. Report for each: actually wired; present but unwired; missing; or unverified. Use latest code, not old audit claims. No network or source edits.

**2. Repair one decisive vertical slice.** One newly received configured-source token, no market baseline: record early discovery and identity; extract/verify available project/narrative links or explicitly request human research; attempt permitted risk checks; produce truthful operator research priority and reasons. Preserve existing market pipeline and publication behavior until separately authorized.

**3. Offline adversarial tests.** Cases: authentic new project with flat/unknown market; rising-chart impersonator; strong narrative with verified dangerous token controls; absent website but genuine meme; copied Telegram claims; wrong contract; no GMGN timestamp; token with only one observation; duplicated horizon baseline. Assert no blind approval and no missed research solely due to lack of whales or momentum.

**4. Bounded prospective live pilot.** Specify source set, duration, maximum requests and storage paths, with explicit user approval before any requests/sends. Track all candidates, operator effort, false positives, misses and outcomes. Keep premium publication off until documented criteria are validated.

**5. Calibrate, then monetize carefully.** Establish whether the resulting shortlist is selectively useful and whether users find the research valuable. If the results disappoint, adjust hypotheses based on complete data; don't rewrite history or promote only wins.

Only after V1 is demonstrably useful should V2 agentic complexity or Soup training become the priority.

## 46. V1 definition of done

> **Given a newly posted token in a configured source, DMO can notice it promptly, explain what original time-valid information makes it worth researching (even with no whale or momentum), verify the project/contract relationship and material risks as available, produce a small honest research shortlist with explicit uncertainty, control publication, and track *every* case and its feasible subsequent outcome.**

This is a testable product claim. It is not equivalent to “the software has 661 passing tests” or “PAID moved after two snapshots.”

## 47. V2 definition of done

> On the same bounded research universe and leakage-safe evaluation, DMO independently chooses and verifies the next useful inquiries, improves timeliness and decision quality relative to V1, measures cost and uncertainty, and tracks wallet/catalyst evolution without inventing facts.

## 48. V3 definition of done

> DMO originates useful investigations from continuously monitored multi-source events beyond handpicked input lists, catches and corrects stale/false hypotheses, maintains a longitudinal evidence graph and improves prospectively with controlled model and process updates.

---

# FINAL PRINCIPLES — THE NON-NEGOTIABLE SOURCE OF TRUTH

1. **Earlier meaningful evidence, not later market applause.** Research first; market response is context and feedback.
2. **Discovery ≠ verified project ≠ review ≠ publication ≠ profitable trade.** Maintain all boundaries.
3. **Identity and narrative must be connected to the exact contract and the right moment in time.**
4. **The early thesis earns investigation, never immunity from security or exit risk.**
5. **No whale, KOL, rising liquidity, or volume surge is required to research a token.**
6. **No market cap—including below $100K—guarantees 1.5x or 2x.**
7. **GMGN is a foundational evidence/tool provider; Telegram is a discovery source; external AI is a replaceable capability; Soup is a future training lab. DMO is the system connecting them.**
8. **Preserve provenance, original decisions, all failures, real costs, and unknowns.**
9. **Never confuse a functioning component with a validated product.**
10. **Ship the smallest honest V1; use measured forward evidence to justify V2 and V3.**

> **DMO's promise is not “we see a coin pumping.” It is “we discover a reason to investigate before it becomes obvious, verify what we can, explain the risks, and tell you what the evidence actually supports.”**

---

# OPERATIONAL ADDENDUM — 2026-10-13

> **Authority of this addendum:** This section records the current live-Beta state, decisions, failures, and next priorities discovered after the September product synopsis. It does **not** retroactively claim that planned features are implemented. Where this addendum conflicts with older operational assumptions, this addendum governs current work. The accepted DMO opportunity engine is to be preserved unless a demonstrated defect requires a surgical change.

## A. Current north star: keep the runners, remove the rugs

DMO's immediate goal is no longer to redesign the whole intelligence system. The current source-driven opportunity engine is demonstrably finding fast runners. The dominant remaining problems are:

1. **rug/scam capability detection**, especially coordinated economic ownership hidden behind many wallets;
2. **source quality**, because some of the 33 configured channels behave like terminal/trench feeds rather than selective callers;
3. **promotion latency**, where DMO sometimes discovers a runner early but waits too long for traditional catalyst/attribution evidence before promoting it.

The governing rule for current work is:

> **Do not reduce DMO's ability to discover early runners. Rug Defense may warn on or remove demonstrably dangerous opportunities, but it must remain logically separate from opportunity discovery/scoring.**

No change should be accepted merely because it reduces call volume. The objective is a higher-quality opportunity stream with fewer rugs, not maximum conservatism.

## B. Frozen/active code boundaries

- Accepted frozen Beta baseline: branch `dmo-beta`, worktree `D:\dmo-beta`, HEAD `7c15b93fa1344a744f4fe8461293a7f14a293b92`.
- Active Rug Defense worktree: `D:\dmo-rug-defense`.
- Do **not** modify `D:\dmo-beta` during Rug Defense/source-quality experiments.
- Publication remains `TEST_CHANNEL`.
- Trading remains `DISABLED`.
- Rug Defense remains `SHADOW`.
- Enforcement remains **OFF** until prospective evidence justifies it.
- Base DMO discovery/source/convergence/thesis/CurrentState logic is not to be casually rewritten.

## C. Evidence that the opportunity engine is finding runners

A Telegram export from the 2026-10-12 live window contained 14 visible new calls (10 full DMO + 4 Beta) plus one older result whose original call was outside the slice. By the end of that uneven observation window, seven of the 14 visible calls had already recorded a 2x+ milestone. This is **not** a 50% final win-rate claim because observation windows differ and some calls were only minutes old.

Notable prospective observed milestones included:

- `SEAN` — CA `8PGyHCKvSUjezHkV7KLwMacnmSJLe1YbRM1zvDVApump`: called around $345.5K; observed maximum ~5.89x.
- `oracle` — CA `8HbBuMvWeMqfc5AeKcmomQLVc4ZXNHFJ7XCubdBgpump`: executable reference ~$35.1K; observed ~5.06x.
- `Diggs` — CA `5EihbnwJYmBaWfgnFdrjZ3pPwm5MZi4Wk9k8KLvdpump`: observed ~2.27x.
- `XDOGE` — CA `9emscrCbv7SV2f9oXFUwmKmSVZxiwGe5ynScMKCpump`: observed ~2.15x.
- `Solamians` — CA `8ZP5CzbPL1fmP8dn1GEmLd8xw1JdudUF5Dk7EpLxpump`: observed ~2.57x.
- `Sniff` — CA `8h4Cy6wgufWmonnxLmxabLYZdHPcDyRWMywYxgWYpump`: observed ~2.35x.
- `apelink` — CA `2ikMciSZ1nK1X9E8X7U5trw3Tc9jW1Ud7FjrhAxPpump`: observed ~2.08x.

Observed peak is not automatically an executable return, and a token reaching 2x/5x does **not** prove it was safe. A runner can still be rug-capable. These cases are therefore runner-preservation benchmarks, not automatic safe-token labels.

## D. Rug Defense: final current semantics

The intended Rug Defense states are now:

- **PASS** — required scoped evidence was acquired sufficiently and the implemented high-value checks found no meaningful supported current catastrophic capability. PASS is not a guarantee of safety.
- **CAREFUL** — real positive evidence shows suspicious economic coordination/control/capability, but proof is below the VETO standard. CAREFUL is a warning, not a rejection.
- **UNKNOWN** — a safety-critical mechanism could not be reliably assessed because acquisition/integrity/support failed. UNKNOWN is not synonymous with suspicious and is intended to remain non-blocking.
- **VETO** — strong verified evidence establishes a destructive mechanism or credible common economic control with meaningful current executable destructive capability. Only VETO is intended eventually to block an otherwise valid call.

Opportunity score must never override a verified Rug Defense VETO, but Rug Defense must never rewrite the base DMO opportunity decision in SHADOW.

## E. Economic-cluster hardening — 2026-10-12 result

The latest hardening pass implemented bounded, explainable economic clustering in `D:\dmo-rug-defense`. Changes remained **uncommitted** at the time of the report; pre-existing work was preserved.

Implemented strong relationship classes include:

- verified transfer topology;
- reviewed private-funder fan-out;
- actor reuse/history where independently supported.

Supporting-only evidence is not allowed to VETO. Examples of supporting evidence include freshness, same-block timing, identical balances, synchronized activity, or common exchange funding. False-positive safeguards remain important for treasuries, vesting, multisigs, PDAs, market makers, team allocations, protocol accounts, liquidity management and exchange/service infrastructure.

Acceptance results:

- runner benchmark count: 7;
- runner base decisions changed: 0;
- runner VETOs: 0;
- OFF vs SHADOW base-decision differences: 0;
- median added controlled-publication latency: ~2.42 ms;
- p95 added latency: ~7.86 ms;
- max observed added latency: ~34.45 ms;
- Helius/RPC request cap: 8 per candidate; 5 observed live in the measured profile;
- provider starvation observed in controlled tests: no;
- focused tests: 234 passed, 1 skipped;
- full suite: 1,523 passed, 32 skipped, 291 subtests passed;
- opportunity engine modified: no;
- Beta baseline modified: no;
- SHADOW isolated: yes;
- ready for bounded live SHADOW: yes;
- ready for enforcement: no.

### 9LIVES lesson

9LIVES (`AqUPRnyFCRuMqKYgY5Tf64CFshFecuaGSGXx4cqqpump`) remained an honest non-win for the forensic detector:

- original Rug verdict: PASS;
- retrospective prospective detectability: `NOT_PROVABLE`;
- extended historical check: UNKNOWN;
- root gap: a common destructive controller could not be proven from pre-call relationship history.

Do **not** hindsight-tune a special 9LIVES threshold. Later collapse may identify whom to investigate, but future relationships cannot be injected into the original decision.

### AA → CYBERPIN chronology

AA has verified later exit history, but its prospective historical assessment remains UNKNOWN where the required pre-exit evidence is incomplete. CYBERPIN also remains historically UNKNOWN under strict chronology. The anti-lookahead boundary is preserved.

## F. Disposable-wallet scammer model

A major current assumption is that sophisticated memecoin scammers may create fresh wallets for a single launch, rug the coin, abandon those wallets and create new ones for the next launch. Therefore **wallet reputation/history must be secondary, not the backbone of Rug Defense**.

Primary question:

> **On this token, right now, do apparently separate fresh wallets form one economically coordinated actor with enough combined holdings/capability to destroy the actual pool?**

Primary same-token evidence should prioritize:

- common upstream funding with verified fan-out;
- common token-distribution paths;
- direct pre-decision transfers;
- fan-in/fan-out topology;
- bundle/launch relationships when objectively provable;
- combined holdings of defensibly linked wallets;
- current executable impact against the canonical pool.

Actor/funder/collector history remains useful bonus evidence when infrastructure is reused, but DMO must not depend on scammers reusing leaf wallets.

Hard limit: if multiple wallets are independently funded, never interact, share no observable infrastructure and coordinate only off-chain, common ownership may be impossible to prove prospectively. Rug Defense must not fabricate certainty in that case.

## G. Rug Defense is broader than wallet clustering

Fresh-wallet clustering is only one defense layer. Current coverage must eventually be audited across at least these attack families:

1. contract/control abuse — mint, freeze, delegate, malicious transfer restrictions/honeypot/tax behavior;
2. liquidity/pool abuse — LP control/removal, fake or non-executable liquidity, canonical-pool ambiguity, migration tricks;
3. economic-ownership rugs — Sybil/bundled distribution, hidden team control, common-funder/distributor clusters;
4. executable dump capability — whether a supported actor can actually crater the live pool now;
5. launch manipulation — sniper/bundle concentration, manufactured volume/holders, wash behavior/fake decentralization;
6. serial scam infrastructure — reused deployers, funders, distributors, collectors and proven prior exits;
7. social/project deception — impersonation, fake links/sites/accounts and fabricated claims (usually CAREFUL unless paired with destructive on-chain capability);
8. post-launch deterioration — consolidation, coordinated distribution, team unloading, liquidity/control changes and other state changes requiring reassessment.

A **Rug Defense Coverage Matrix** remains a useful audit task before blindly adding more detectors: attack type → existing detection → evidence source → classification behavior → false-positive risk → test case → blind spot → priority.

## H. Third-party graph tools: current decision

RugMaps was qualified as a possible Bubblemaps-like machine-readable graph layer. Result:

- API health/pricing reachable;
- actual Solana graph contract/access not verified;
- historical snapshot support unproven;
- raw wallet/edge/transaction evidence unverified;
- 9LIVES prospective signal not provable;
- qualification-readiness score: 3/50;
- verdict: **NOT QUALIFIED / NOT USABLE for DMO today**.

Do not burn more critical time trying to rescue RugMaps. Bubblemaps or another graph provider may later be added as an optional discovery sensor, but Rug Defense must not depend on a paid/opaque third party.

Current preferred core:

> **Helius/on-chain evidence → bounded economic clustering → existing canonical-pool executable-capacity math → PASS / CAREFUL / UNKNOWN / VETO.**

## I. Source-network cleanup is now high priority

DMO currently tracks 33 sources. Some appear to behave like raw terminal/trench feeds: very high call volume with little meaningful selectivity. These sources can flood candidate queues, consume provider/RPC budget, create fake-looking convergence and make weak signals appear stronger simply because a firehose called them.

The goal is **not** to keep only the highest historical win-rate channels. Low-volume/high-precision channels should remain useful, but the main priority is **active sources that make many genuinely good, early calls**.

Source value should therefore consider four dimensions together:

> **Activity × Precision × Earliness × Unique Contribution**

Desired categories:

- **CORE** — active, good precision, early, useful and independently valuable;
- **QUALITY LOW-VOLUME** — less active but highly accurate/selective, worth retaining;
- **WATCH** — insufficient or mixed evidence;
- **REMOVE** — trench-feed noise, low-quality spray callers, redundant/copied feeds with little timing advantage, or sources consuming disproportionate resources without useful unique contribution.

Important audit question for every removal:

> **If this source had been absent, which successful runners would DMO have failed to discover early or at all?**

Do not rank sources by win rate alone. A source with 2 calls/day at 80% can be valuable, but a source with 40 good early calls/day at 45% may contribute more daily opportunity flow. Conversely, a 300-calls/day feed with 8% 2x and little unique edge is noise even if it occasionally catches a moonshot.

Source independence also matters: dependent/copying feeds must not count as genuinely independent convergence.

**Next source task:** perform a read-only quality audit first. Do not remove registry entries until the evidence and counterfactual winner-loss list are reviewed.

## J. Missed/late runner case: ZKINU

Token: `ZKINU — ZERO KNOWLEDGE INU`

CA: `DGdmHacFYkfrazHYtFEPtAbRnSru8db5cNyQkgY6QsQV`

A tracked source (`Red Bull Callz`) posted it around ~$40.07K market cap. A later screenshot showed roughly ~$185.7K current market cap and ~$255.1K displayed ATH. This is a meaningful runner case and a useful audit target.

Current lesson: do **not** immediately change DMO because the coin ran. Determine whether the source was active, whether the message entered DMO, whether the parser/admission path succeeded, what original live decision was made and whether any gate or resource issue blocked publication. Source cleanup may also change how much weight this source should have.

ZKINU should remain a regression/audit case for **missed-source or missed-promotion behavior**, not a reason to loosen every gate.

## K. Late-promotion case: LUCKY

Token: `LUCKY`

CA: `H1hqLeM7YWs2JFHFJWkbQAcLyPh7DWfn7aUCwtGdpump`

DMO evidence shown in the TEST-channel EARLY WATCH:

- first seen: `2026-10-12T18:58:32.539891+00:00`;
- EARLY WATCH publication: `2026-10-12T19:12:19.543788+00:00`;
- current market cap at watch: `186403`;
- liquidity at watch: `38684.73`;
- independent discovery convergence: 2 sources;
- fresh canonical market: verified;
- economically viable liquidity: verified;
- no active hard veto: verified;
- missing/unconfirmed: official project/contract attribution and verified catalyst.

GemBot's Premium marker was shown around ~$17K and the displayed peak reached ~13.5x from that marker. The chart indicates the major crowd arrived after the early portion of the move.

The important failure is conceptual:

> **DMO discovered the opportunity substantially earlier than it promoted it, but traditional catalyst/project-attribution requirements kept it from becoming a useful call until much of the move was already gone.**

The exact DMO first-seen market cap should be recovered from persisted evidence before claiming a specific ~$60K figure.

### Planned promotion correction — not yet implemented

DMO should support two valid positive paths:

**Path A — Catalyst / Thesis Call**

- credible project/contract attribution;
- verified catalyst/thesis;
- healthy current market;
- no Rug VETO.

**Path B — Early Market / Flow Call**

- high-quality source signal(s);
- genuinely independent convergence where present;
- still-early market position;
- constructive market/flow structure;
- executable liquidity;
- no Rug VETO;
- research may continue after the early call.

For memecoins, lack of a traditional external catalyst must not automatically prevent a high-quality early market opportunity from being called. Sometimes the actionable catalyst is **attention/flow arriving before the crowd**.

### “EARLY WATCH” semantics must reflect market reality

`EARLY WATCH` cannot simply mean “an internal workflow state that has not yet become CALL.” It should reflect whether the opportunity is actually still early.

DMO should retain the frozen first-seen executable reference and compare later state against it, e.g. current market cap / first-seen market cap, time elapsed and structure. If the opportunity has already expanded dramatically, terminology/state should reflect `LATE WATCH`, `OPPORTUNITY EXPANDED`, or an equivalent non-early state rather than announcing an “EARLY WATCH” after the crowd has arrived.

Do not install one arbitrary universal market-cap multiple as a hard rule without calibration.

## L. Sequence of work from here

Do **not** attack every improvement simultaneously.

1. **Preserve/review the current uncommitted Rug Defense hardening patch.** It passed the reported tests and preserved the runner engine; do not lose it.
2. **Audit the 33-source network read-only.** Identify CORE, QUALITY LOW-VOLUME, WATCH and REMOVE candidates using activity + precision + earliness + unique contribution, including counterfactual runners lost by removal.
3. **Prune junk sources only after reviewing the audit.** The objective is a smaller, cleaner source network with meaningful convergence and lower provider load.
4. **Then harden promotion timing using LUCKY and ZKINU as primary regression cases.** Do not weaken the whole system merely because those coins ran.
5. **Implement/validate the dual promotion concept only if point-in-time evidence supports it:** catalyst/thesis path + early market/flow path.
6. **Continue Rug Defense in SHADOW.** Prioritize same-token fresh-wallet coordination + current executable capability; actor history remains secondary.
7. **Audit broader Rug Defense coverage** before adding more ad-hoc heuristics.
8. **Collect prospective outcomes for every call/reject/watch/rug label.** Never tune from winners only.

## M. Current hard invariants

- **Keep runners; remove provable rugs.**
- Rug Defense must not change base DMO opportunity decisions in SHADOW.
- Opportunity score cannot override verified catastrophic capability.
- A pump does not prove safety; a dump does not prove a prospectively detectable rug.
- Supporting heuristics alone do not VETO.
- UNKNOWN means evidence failure, not “probably scam.”
- CAREFUL means real positive suspicion below VETO proof.
- Only VETO is intended eventually to block.
- Same-token current economic control matters more than old leaf-wallet reputation.
- Do not rely on Bubblemaps/RugMaps as a required dependency.
- Remove noisy source feeds based on daily opportunity value, not win rate alone.
- Independent convergence only counts when the sources are genuinely independent/selective.
- Traditional catalyst verification is valuable, but should not force DMO to miss obvious early market/flow opportunities.
- `EARLY` must describe the market opportunity, not merely an internal state-machine label.
- Preserve strict anti-lookahead and frozen prospective evidence.
- `D:\dmo-beta` remains untouched.
- TEST_CHANNEL, trading disabled, SHADOW, enforcement off until explicitly accepted.

> **Current DMO mission:** Find the tiny fraction of memecoins with real early runner potential, get there before the crowd, and use an independent evidence-based Rug Defense to avoid as many destructive scams as can be prospectively proven — without turning DMO into a slow, overengineered system that misses the move.



# CROSS-CHAT CONSOLIDATION ADDENDUM — 2026-10-13

> **Purpose:** This addendum closes an important documentation gap. DMO development is currently happening across multiple parallel chats/workstreams. The sections below record concrete work from those other threads so this note can function as a single operational memory, rather than only a summary of the Rug Defense/improvement chat. Where a workstream is experimental or incomplete, it is explicitly labeled as such.

## N. GemBot reverse-engineering workstream — active, experimental

A separate DMO workstream is reverse-engineering **GemBot's calling edge**, specifically the logic behind its early Premium/Ultra-Risky style calls. The objective is **not** to copy GemBot's UI, buttons, charts, or branding. The only target is proven calling intelligence that could improve DMO's ability to identify runners earlier.

Current concrete status from the reverse-engineering thread:

- workspace/research area: `D:\gembot-recon`;
- approximately 100 historical Premium call artifacts have been reconstructed/collected for analysis;
- a real Premium artifact exposing fields such as `callAtMs` and `callMcUsd` was found;
- rough cap floors around ~$7K and ~$20K appeared in the observed Premium artifact population, but these are **not yet validated as a complete calling classifier**;
- one pre-call burst was deeply decoded;
- a preliminary live selector exists;
- primary frozen experimental policy reported as `capfloor-only-7k-v1`:
  - below ~$7K => PASS/not-call in the experiment;
  - at/above ~$7K => experimental CALL;
  - missing/unsupported => WATCH;
- latest retained prospective snapshot reported hundreds of launches registered, an active-set sampler, dozens of experimental calls, and only a very small number of confirmed real GemBot matches;
- a separate activity/freshness experimental arm also produced unique calls;
- **no validated GemBot classifier has been proven yet**;
- control/negative quality is still insufficient to claim GemBot has been cloned;
- selector is currently paused in the last reported checkpoint.

Additive DMO-side shadow artifacts created by this workstream include:

- `D:\dmo-rug-defense\dmo\gembot_shadow.py`
- `D:\dmo-rug-defense\scripts\gembot_shadow.py`
- `D:\dmo-rug-defense\docs\DMO_GEMBOT_SHADOW.md`

The shadow adapter is deliberately non-authoritative:

- no active runtime hook;
- no production publication authority;
- `publication_eligible = false`;
- experimental CALL/PASS/WATCH must never silently become real DMO approval.

### GemBot transplant rule

Only transplant a GemBot-derived feature into DMO after it survives:

1. point-in-time reconstruction;
2. positive and negative/control comparison;
3. prospective validation;
4. runner-preservation testing;
5. proof that the feature adds signal beyond existing DMO/source information.

Do **not** transplant a feature merely because it correlates with known historical winners.

### Why this matters to current DMO improvement

The LUCKY case demonstrated that GemBot could mark an opportunity materially earlier than DMO's eventual EARLY WATCH. Reverse engineering may therefore help the **promotion/early-call path**, but it must not be used to weaken Rug Defense or overwrite DMO's existing opportunity engine without evidence.

## O. Telegram publication / Phanes / downstream routing workstream

A separate operational thread is handling how accepted DMO output moves from the internal TEST channel to the downstream public/private call presentation path. This is distinct from candidate selection and Rug Defense.

Current intended routing rule:

- `DMO Calls TEST` keeps the full internal report/output;
- only **actual DMO CALL** and approved **DMO BETA CALL** events are allowed to stage/send a raw canonical CA downstream;
- `EARLY WATCH`, `WATCH`, `REJECT`, statistics, diagnostics, source chatter and other non-call messages must **not** be forwarded as calls;
- downstream rendering/presentation is handled separately (Phanes/relay/publisher path);
- the public-facing pipeline must not simply mirror the TEST channel.

Reported publication milestones/status from that thread:

- an accepted production artifact/branch checkpoint `13c0084922e2c9f27b617284a263bcada850696b` was reported for the publication path;
- full calls were configured for the called channel while Beta/Early remained TEST-only in that checkpoint;
- a local standalone relay was later run with an allowlist intended to pass FULL+BETA only;
- that relay initially missed channel posts because of a sender-ID check issue, then successfully published a CA after correction;
- the Railway publisher later encountered a closed PostgreSQL connection and required publisher-only restart/recovery;
- do not confuse publication/relay failures with DMO opportunity-selection failures.

Hard publication principle:

> **DMO decides whether an opportunity qualifies. The downstream relay/publisher decides how that already-qualified call is rendered/distributed. Non-call TEST messages must never become public calls merely because they exist in the source channel.**

## P. Cloud/runtime/hosting status from parallel operations work

Cloud deployment has been an independent operational workstream because the user must eventually be able to run DMO without depending on the laptop.

Concrete recent operational history:

- accepted local Beta decision-latency baseline was roughly 6.60s median / 13.18s p95;
- a later cloud latency run reported hundreds of natural decisions at roughly 9.31s median / 13.87s p95 with pooling-only changes and Beta logic unchanged;
- Railway remained the working TEST/publication owner during that phase;
- Botkeep migration was a **NO-GO** despite authentication/parity success because starts/recovery failed;
- earlier Northflank/Botkeep/other free-host experiments are infrastructure experiments only and must not be allowed to mutate accepted DMO behavior;
- when hosting experiments fail, preserve the working Railway/local runtime rather than forcing migration for its own sake.

Current principle:

> **Cloud hosting is an operational requirement, not a reason to rewrite DMO. Preserve the accepted decision engine and measure latency/persistence independently of product-quality changes.**

## Q. Cross-chat source/caller analysis and why it matters

Other DMO-adjacent chats have been analyzing callers, wallet behavior, copytrading feasibility and scam structure. Only findings that materially affect DMO should be promoted into DMO rules. Current durable lessons include:

- absolute winner count is not source quality; trench-feed channels can appear successful by calling nearly everything;
- source ranking must balance **activity + precision + earliness + unique contribution**;
- independent convergence is valuable only when the sources are genuinely independent/selective;
- a source can remain valuable even at lower volume if its precision is high;
- the main source-network priority is **active and good**, not merely high win-rate but inactive;
- runner discovery and rug capability are separate axes: a coin can be a legitimate fast runner and still be rug-capable;
- source/caller research should improve candidate quality without becoming a blind copytrading system.

## R. One master timeline / workstream map

DMO is currently being improved through several parallel workstreams. Treat these as one system with separate responsibilities:

1. **Opportunity engine / Beta** — source-driven discovery, fast market validation, CALL/WATCH/REJECT, outcome tracking.
2. **Rug Defense** — independent safety classification: PASS / CAREFUL / UNKNOWN / VETO; current focus on same-token economic clustering and executable destructive capability.
3. **Source-network quality** — remove trench-feed noise while preserving active/high-quality/early sources and unique runners.
4. **Promotion timing** — prevent cases like LUCKY where DMO sees the opportunity early but waits until the edge is mostly gone; investigate ZKINU as a separate missed-source/promotion case.
5. **GemBot reverse engineering** — experimental research into earlier runner-selection/promotion signals; shadow-only until proven.
6. **Publication/Phanes/relay** — downstream distribution of already-qualified calls only; no TEST-channel mirroring.
7. **Cloud/runtime** — persistent hosting and latency/persistence engineering without changing accepted DMO logic.
8. **Evaluation/data flywheel** — prospective outcomes, missed runners, rejected winners, rugs, false VETOs, timing and executable returns.

No single chat is the whole DMO project. The master note must be updated whenever one of these workstreams reaches a meaningful checkpoint.

## S. Immediate synchronized priority order

Current synchronized order across workstreams:

1. preserve the working opportunity engine and current Rug Defense hardening;
2. complete source-quality audit and remove true trench-feed noise only after counterfactual runner-loss review;
3. continue GemBot reverse engineering in shadow/research mode and transplant only proven early-call intelligence;
4. use LUCKY and ZKINU as promotion/missed-runner regressions;
5. keep Rug Defense SHADOW while collecting fresh same-token coordination/capability evidence;
6. keep publication routing strict: only qualified call types downstream;
7. keep hosting work operationally separate from product logic;
8. maintain point-in-time evidence and never rewrite historical decisions using future outcomes.

> **Cross-chat operating rule:** when a separate DMO chat produces a real checkpoint, test result, new failure mode, or architectural decision, merge that fact into this master note with its status (`implemented`, `experimental`, `planned`, `rejected`, or `unproven`). This prevents parallel chats from becoming separate versions of DMO.
