# Parallel Hackathon Council Review — 2026-09-09

## Final authority

This document records the **final verified council run** used to design the hackathon portfolio in `HACKATHON_ENTRY_WORKFLOWS_2026-09-09.md`.

> **Hard invariant: vessels run in parallel only.**

The authoritative wave launched **72 independent CAPT vessels concurrently**:

- 9 requested OpenRouter models;
- 8 role vessels per model;
- one isolated CAPT runtime and ledger per vessel;
- 72 worker threads;
- a 72-party launch barrier;
- sanitized bounded rule/repository packet only;
- no model-side file/search tools;
- no private source or secrets in provider prompts.

The eight roles were rule counsel, judge simulator, repo architect, integration engineer, humanitarian lead, adversarial reviewer, prize strategist, and demo producer.

Raw provider responses and CAPT runtime evidence remain private/local. This public repository contains only the sanitized synthesis.

## Parallelism proof

The final 72-vessel wave recorded:

| Metric | Result |
|---|---:|
| Requested vessels | **72** |
| Unique worker threads | **72** |
| Barrier parties | **72** |
| Barrier release spread | **2.809 ms** |
| Main-wave wall time | **139.314 s** |

The runtime-ready and completion events were interleaved across models and roles. This was not “parallel models with serial roles”; each model-role vessel had its own runtime state.

A recovery wave was also parallel-only: 23 failed cells were released through a 23-party barrier with **0.261 ms** spread and 23 unique worker threads. The final Ultra recovery used a 3-party barrier with **0.047 ms** spread.

## Requested models and final usable yield

| Model | Exact OpenRouter ID | Accepted role outputs | Final state |
|---|---|---:|---|
| NVIDIA Nemotron 3.5 Lightning | `nvidia/nemotron-3.5-lightning:free` | **8/8** | full council |
| NVIDIA Nemotron 3 Super 120B A12B | `nvidia/nemotron-3-super-120b-a12b:free` | **8/8** | full council |
| NVIDIA Nemotron 3 Ultra 550B A55B | `nvidia/nemotron-3-ultra-550b-a55b:free` | **7/8** | one repo-architect canonical-content failure |
| NVIDIA Nemotron 3 Nano Omni | `nvidia/nemotron-3-nano-omni-30b-a3b-reasoning:free` | **0/8** | blocked by current OpenRouter workspace guardrail |
| GLM 5.3 Flash | `z-ai/glm-5.3-flash` | **8/8** | full council |
| DeepSeek V4 Flash 0731 | `deepseek/deepseek-v4-flash-0731` | **8/8** | full council |
| HY3 | `tencent/hy3` | **8/8** | full council |
| Qwen 3.8 Flash | `qwen/qwen3.8-flash` | **8/8** | full council |
| Qwen 3.7 Flash | `qwen/qwen3.7-flash` | **0/8** | blocked by current OpenRouter workspace guardrail |

**Final accepted CAPT model-role outputs: 55/72.**

The two 0/8 models were not missing from OpenRouter’s catalog. Live catalog validation found both exact IDs. Direct transport diagnostics showed their only available endpoints were excluded by the account’s current guardrail policy. The guardrail was **not changed or weakened**, and no substitute model was silently used.

The single remaining Ultra failure was not counted as an opinion.

## Provider/runtime lessons from the run

Three failures in the earlier attempts were harness/provider mechanics rather than model quality:

1. A legacy harness preserved one trailing newline at execution while the approval path normalized it, and CAPT correctly rejected the byte-level approval digest mismatch.
2. A Unix socket can exist before its server is ready to accept connections; the final recovery path used bounded connect retries rather than treating file existence as readiness.
3. Several reasoning models consumed the output envelope in `message.reasoning` and returned no canonical answer content. Recovery used model-supported bounded/disabled reasoning policies while preserving the exact approved task and OpenRouter model ID.

No CAPT approval check was bypassed to make the council run.

## Strict consensus extraction

Of the 55 accepted provider outputs, **24 produced a machine-parseable compact final JSON object** suitable for direct vote counting. Other accepted outputs were retained as qualitative review evidence but were not turned into synthetic votes.

Strict parsed verdict counts:

| Entry | GO | HOLD | KILL | Council reading |
|---|---:|---:|---:|---|
| **A — Amazon CAPT Guardian / Relay** | **22** | 2 | 0 | strongest consensus GO |
| **B — NVIDIA Flock-Sucker Field Sentinel** | **19** | 4 | 0 | strong GO after licensing/runtime gates |
| **C — NVIDIA CAPT Sovereign** | 8 | **14** | 1 | valid, but defer behind A/B unless scope stays narrow |
| **D — Apertus OpenWatch** | 2 | **21 incl. HOLD variants** | 0 | hard HOLD until Oct 1 challenge/start gate |
| **E — Apertus CAPTsec Gauntlet** | 2 | **21 incl. HOLD variants** | 0 | hard HOLD until Oct 1 challenge/start gate |

When asked for the single highest expected-value target, the parseable council favored **Amazon 15 to NVIDIA Flock-Sucker 8**.

## Final portfolio decision

### 1. Amazon — CAPT Guardian / Relay: GO

Strongest existing donor: `capt-workspace-mcp`.

Verified local repo evidence already includes authenticated Streamable HTTP, MCP transport tests, and support for protocol version `2025-11-25`. That clears much of Alexa+’s protocol floor. The contest build still needs a self-contained public derivative, a significant post-August-31 competition delta, an actual Alexa+/MCP runtime path, narrow stateful orchestration, one-use action approval, and receipts that correspond to real execution.

Do **not** publish private CAPT Core. The submission should be a deliberately released product, not a wrapper around a private dependency.

### 2. Nebius x NVIDIA — Flock-Sucker Sovereign Field Sentinel: GO after license gate

Flock-Sucker is the strongest visually differentiated Physical AI entry because the Android sensing/evidence pipeline already exists on real hardware.

Hard gates:

- perform ownership/dependency/SPDX audit;
- add a compatible top-level OSS license;
- make a real runtime call through Nebius Token Factory or Nebius AI Cloud using an NVIDIA open-source model;
- document a significant post-August-26 delta;
- make cloud disclosure inspectable and privacy-minimized;
- show at least one minute of physical hardware or key application modules in the demo.

Nemotron should correlate evidence and competing hypotheses; it must not turn weak radio evidence into an accusation of identity or intent.

### 3. Nebius x NVIDIA — CAPT Sovereign: CONDITIONAL GO

Personal AI matches CAPT’s memory, skills, selected tools, approval and provenance concepts extremely well. The risk is scope and judge fatigue: a generic “agent platform” is weak.

Only execute after Amazon and Flock are on track, and only as a **new self-contained public product** with one memorable multi-session workflow. It must be substantially different from Flock-Sucker and must run without private CAPT dependencies.

### 4. Hack Apertus — CAPTsec Gauntlet: HOLD until Oct 1

Strategically strong fit for Apertus Readiness / Red-Teaming, but do not create the competition implementation early. Re-read the released challenge on October 1, then create a clean standalone open implementation if the fit survives.

### 5. Hack Apertus — OpenWatch: HOLD until Oct 1

Humanitarian fit is strong, but the Own Project path currently requires a new project started during the hackathon period. Treat Flock-Sucker as an external dependency/data-source concept only if the final rules and licenses allow it. Do not contaminate Hack Apertus output with private CAPT or unwilling-to-open pre-existing IP.

## Post-council official-rule corrections

The council vessels were deliberately bounded to a frozen rule packet. Current official rules were rechecked after the run before finalizing strategy.

### NVIDIA prize stacking

The current rules state that each project may receive **one Overall Award OR one Track Award, and one Bonus Award**. The Tavily bonus is $3,000 and requires a functional runtime Tavily API call. Therefore an Overall winner can also receive the Tavily bonus if legitimately earned. For Flock-Sucker, the maximum cash target is **$20,000 Grand Prize + $3,000 Tavily = $23,000**.

Official source: https://nebiusglobalaihackathon.devpost.com/rules

### Amazon friction log

Amazon’s current rules allow optional friction-log entries and state that participants who submit them can score **up to a 10% judging bonus**. CAPT Guardian should maintain a real friction log from onboarding through deployment.

Official source: https://amazonappdev2026.devpost.com/rules

## Repository boundaries

- `capt-workspace-mcp`: private/internal donor. Release only an intentionally scoped, self-contained subset for Amazon.
- `Flock-Sucker`: existing public product and NVIDIA Physical AI base. Licensing audit is mandatory before submission.
- `CAPT-Inversion-Labs`: private mothership. Never make it public to satisfy contest rules.
- `CAPT-Arena-v2` / CAPTsec methodology: conceptual donor for Apertus; reimplement competition output cleanly after the official start.

## Standing architecture rule

Do not build one giant “hackathon repo” and reskin it five times. Shared schemas and Inversion Labs concepts may create family resemblance, but each submission must have a distinct user problem, runtime proof, public boundary, competition delta, demo, and kill gate.
