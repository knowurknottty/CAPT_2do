# Parallel Hackathon Council Review — 2026-09-09

## Authority

This document records the final valid hackathon review council used to produce `HACKATHON_ENTRY_WORKFLOWS_2026-09-09.md`.

**Hard invariant:** vessels run in parallel only.

The authoritative council wave launched **72 isolated CAPT vessels concurrently**:

- 9 OpenRouter model IDs
- 8 independent role vessels per model
- one CAPT runtime/ledger per vessel
- bounded sanitized rule/repository packet
- no file/search tools available to the model vessels
- no private source or secrets placed in the provider prompt

The eight roles were:

1. rule counsel
2. judge simulator
3. repo architect
4. integration engineer
5. humanitarian lead
6. adversarial reviewer
7. prize strategist
8. demo producer

Raw provider responses and CAPT runtime evidence remain in the private/local research workspace; this public repo contains the sanitized synthesis only.

---

## Requested model matrix and usable review yield

| Model | Requested ID / canonical retry | Accepted role reviews | Result |
|---|---|---:|---|
| NVIDIA Nemotron 3.5 Lightning | `nvidia/nemotron-3.5-lightning:free` | **8/8** | full council |
| NVIDIA Nemotron 3 Super 120B A12B | `nvidia/nemotron-3-super-120b-a12b:free` | **8/8** | full council |
| NVIDIA Nemotron 3 Ultra 550B A55B | `nvidia/nemotron-3-ultra-550b-a55b:free` | **7/8** | strong council; one canonical-content failure |
| DeepSeek V4 Flash 0731 | `deepseek/deepseek-v4-flash-0731` | **6/8** | strong partial council |
| Qwen 3.8 Flash | `qwen/qwen3.8-flash` | **3/8** | partial council; remaining responses lacked canonical answer content |
| GLM 5.3 Flash | retry used `z-ai/glm-5.3-flash` | **0/8** | canonical alias fixed; provider returned no canonical answer content |
| HY3 | retry used `tencent/hy3` | **0/8** | canonical alias fixed; provider returned no canonical answer content |
| NVIDIA Nemotron 3 Nano Omni | `nvidia/nemotron-3-nano-omni-30b-a3b-reasoning:free` | **0/8** | CAPT/OpenRouter path returned HTTP 404 for this wave |
| Qwen 3.7 Flash | `qwen/qwen3.7-flash` | **0/8** | CAPT/OpenRouter path returned HTTP 404 for this wave |

**Usable independent model-role reviews: 32.**

A failed provider call was not counted as a vessel opinion. The synthesis does not manufacture consensus from missing outputs.

OpenRouter currently lists the Nano Omni and Qwen 3.7 model IDs, so the HTTP 404s are recorded as **runtime-route failures of this campaign**, not evidence that the models do not exist. No provider privacy/data-policy setting was weakened to force the calls through.

---

## Council consensus that survived adversarial review

### Amazon

Strong agreement:

- The Alexa+ route is the highest expected-value target because CAPT's existing MCP work already covers much of the protocol/transport floor.
- A basic API wrapper will score poorly; the project needs visible state, orchestration, authority and auditability.
- The public submission must be a self-contained derivative, not a shell around private CAPT Core.
- The strongest differentiator is **exact-action approval + provenance receipt**, not the number of tools.
- The demo should deliberately show one denied/tampered action so the governance claim is falsifiable.

### Nebius x NVIDIA — Flock-Sucker

Strong agreement:

- Flock-Sucker is the most visually differentiated Physical AI candidate because sensing and evidence collection already exist on a real Android device.
- The cloud model must be an evidence correlator, not an authority oracle.
- Offline operation must remain useful; Nebius should enrich the field picture rather than become a hard dependency.
- Cloud disclosure needs an explicit privacy boundary and inspectable payload.
- Tavily is strategically natural only for public vendor/spec/documentation enrichment of unknown observations.
- The missing top-level license is a hard submission blocker.

### Nebius x NVIDIA — CAPT Sovereign

Strong agreement:

- Personal AI is an exact conceptual fit for CAPT memory, skills, tools and authority.
- The danger is judge fatigue: a generic "agent platform" will look obvious.
- The submission needs one memorable daily workflow spanning two sessions so persistent memory and skill reuse are visible.
- Private memory ownership and selective disclosure to Nemotron should be demonstrated, not merely asserted.
- The public repo must run without private CAPT dependencies.

### Hack Apertus

Strong agreement:

- CAPTsec Gauntlet is the strongest strategic fit with the published Red-Teaming direction.
- OpenWatch is the stronger direct humanitarian idea but depends more heavily on the exact October 1 challenge packet.
- Both should remain design-only before the official start.
- A clean standalone implementation is safer than importing private CAPT/Flock internals because Hack Apertus has broad open-source licensing requirements for submitted output and necessary pre-existing IP.

---

## Post-council rule corrections

The model vessels were intentionally bounded to a frozen rule packet. After the parallel run, the synthesis re-checked current official rules and corrected two material assumptions before writing the final workflows.

### Correction 1 — NVIDIA prize stacking

The current official Nebius x NVIDIA rules state:

> Each Project is eligible for one Overall Award **OR** one Track Award **and one Bonus Award**.

Therefore a project that wins an Overall cash award **can also win a Bonus award**, including Best Use of Tavily. Flock-Sucker's realistic maximum target is thus the $20,000 Overall Grand Prize **plus** the $3,000 Tavily bonus, if both are legitimately earned.

Official source: https://nebiusglobalaihackathon.devpost.com/rules

### Correction 2 — Amazon friction logs

Amazon's current rules say friction-log entries may provide **up to a 10% judging bonus** during Stage 2. This is not merely a Bee-specific tactic; CAPT Guardian should maintain a real friction log from first-party onboarding and deployment work.

Official source: https://amazonappdev2026.devpost.com/rules

---

## Repository findings used by the council

### `capt-workspace-mcp`

Internal donor only. Current repo evidence shows:

- authenticated Streamable HTTP;
- MCP transport tests;
- design support for protocol version `2025-11-25`;
- fail-closed runtime boundaries;
- approval/model-run surfaces;
- provenance/read-back-oriented workspace behavior.

This is the strongest Amazon donor, but the hackathon repo should expose only an intentionally released self-contained subset.

### `Flock-Sucker`

Best NVIDIA Physical AI donor/current submission repo. Current repo evidence shows:

- seven primary sensing domains;
- evidence-aware classification and confidence boundaries;
- encrypted persistent storage plus ephemeral mode;
- repeated-sighting/history/map capabilities;
- detector proof-of-life and ingress telemetry;
- local AI routes;
- external-radio/OEM/system integration work.

Current blocker: **no top-level open-source LICENSE**.

### `CAPT-Inversion-Labs`

Private mothership; donor of concepts and selected intentionally released code only. Do not make it public for a competition.

### `CAPT-Arena-v2`

Useful source of evaluation/evidence methodology for Apertus Gauntlet, but it remains a private conceptual donor. The Apertus submission should be freshly implemented after the event start.

---

## Decision

The council does **not** recommend one giant cross-hackathon repository.

The winning portfolio is deliberately asymmetric:

1. a narrow Alexa+ governance product;
2. a real Android Physical AI field product;
3. a user-owned Personal AI product;
4. a clean-room Apertus red-team harness after October 1;
5. optionally, a clean-room multilingual evidence explainer after October 1.

Shared Inversion Labs concepts should create family resemblance; they should not make the submissions look like superficial rebrands of one codebase.
