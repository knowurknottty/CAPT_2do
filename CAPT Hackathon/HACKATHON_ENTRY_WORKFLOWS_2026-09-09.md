# Hackathon Entry Workflows — 2026-09-09

**Priority:** Inversion Labs product value first, humanitarian usefulness second, realizable prize value third.

This plan is based on the current official rules for:

- Amazon Build, Ship, Shape: https://amazonappdev2026.devpost.com/rules
- Nebius x NVIDIA Global AI Hackathon: https://nebiusglobalaihackathon.devpost.com/rules
- Hack Apertus: https://hackapertus.devpost.com/rules
- Hack Apertus terms: https://hackapertus.ch/terms-and-conditions

## Portfolio decision

| Priority | Entry | Competition / Track | Source repo(s) | Submission repo | Status |
|---|---|---|---|---|---|
| 1 | **CAPT Guardian / Relay** | Amazon — Alexa+ | `capt-workspace-mcp`, selected CAPT governance concepts | **new narrow public repo** | GO |
| 2 | **Flock-Sucker Sovereign Field Sentinel** | Nebius x NVIDIA — Physical AI | `Flock-Sucker` | existing public repo, significantly updated | GO after license gate |
| 3 | **CAPT Sovereign** | Nebius x NVIDIA — Personal AI | `CAPT-Inversion-Labs`, `capt-workspace-mcp`, CAPT Node concepts | **new self-contained public repo** | GO |
| 4 | **CAPTsec Apertus Gauntlet** | Hack Apertus — Readiness / Red-Teaming | CAPTsec / Arena concepts only | **new repo created on/after Oct 1** | HOLD |
| 5 | **OpenWatch Apertus** | Hack Apertus — Adoption / Own Project, if Oct-1 challenge fit remains | Flock concepts only; no code dependency by default | **new repo created on/after Oct 1** | HOLD |

The public CAPT derivatives must be **self-contained**. They may reuse code that Inversion Labs intentionally chooses to release, but they must not require a private CAPT package or private repository to run.

---

# 1. Amazon — CAPT Guardian / Relay for Alexa+

## Why this is first

Amazon Alexa+ is unusually aligned with work already completed in `capt-workspace-mcp`: authenticated Streamable HTTP and MCP protocol support at or above the required `2025-11-25` floor already exist internally. The contest explicitly treats a basic MCP wrapper as obvious, so the entry must demonstrate a stateful multi-service workflow with meaningful governance rather than a large tool catalog.

**Prize target:** Alexa+ 1st ($25,000 cash) + Open Source mini ($5,000 cash). The rules permit one track prize plus one mini-challenge prize, so the practical project ceiling is **$30,000 cash** plus listed AWS credits. Enter AWS Builder only if AWS becomes architecturally useful; do not bolt it on just to chase a second mini that the same project cannot also win.

## Product thesis

**CAPT Guardian** is a governed Alexa+ action relay for caretaking and humanitarian coordination. Alexa+ can gather context and orchestrate services, but consequential actions cross a CAPT-style approval boundary. Every completed workflow returns a compact provenance receipt showing what was requested, what authority was granted, which tools actually ran, and what changed.

The judge should understand the value in one sentence:

> Alexa+ can act for you, but CAPT Guardian makes consequential agent action explicit, bounded, reviewable, and replayable.

## Repo boundary

Create a new public repo during the Amazon submission period, tentatively `capt-guardian-alexa` or `capt-alexa-relay`.

Release only the intentionally public subset:

- MCP `2025-11-25+` Streamable HTTP server;
- narrow tool registry;
- approval/capability gate;
- workflow state machine;
- provenance/receipt schema;
- tests and deterministic demo fixtures;
- Alexa+ configuration/integration artifacts actually used at runtime;
- setup instructions and an explicit open-source license chosen after donor/license audit.

Do **not** publish the CAPT/Inversion Labs mothership or make the public repo depend on private code.

## Competition-period build workflow

1. **Freeze donor provenance.** Record the pre-hackathon donor commits and create `COMPETITION_DELTA.md` showing exactly what is new after August 31, 2026.
2. **Extract the minimal MCP transport.** Bring over only the owned, intentionally releasable Streamable HTTP/MCP primitives and tests. Verify protocol negotiation against `2025-11-25` or later.
3. **Build three narrow humanitarian/caretaking tools.** Prefer a coherent workflow over breadth: intake/context, coordination/request creation, and status/follow-up. No generic 30-tool dump.
4. **Add the action authority boundary.** Low-risk reads may run directly; actions with external consequence generate a one-use approval request bound to exact action arguments.
5. **Add the provenance receipt.** Emit a human-readable and machine-readable receipt with workflow ID, approved action digest, tool calls, result state, timestamps, and explicit unknown/failure states.
6. **Wire the actual Alexa+ runtime path.** Demonstrate Alexa+ -> self-hosted MCP over Streamable HTTP -> workflow -> approval -> action -> receipt. The required technology must be called in code at runtime, not merely named in documentation.
7. **Exploit the judging bonus honestly.** Maintain a real friction log from onboarding through deployment; Amazon currently permits up to a 10% judging bonus for useful friction logs.
8. **Ship the judge package.** Public repo, visible license, one-command/local test path, hosted judge endpoint, deterministic fixtures, architecture diagram, `COMPETITION_DELTA.md`, and <3 minute public demo.

## Demo storyboard

- **0:00–0:15 — Hook:** a voice request that would normally cause an agent to act across services.
- **0:15–0:50 — Orchestration:** show Alexa+ using the real MCP endpoint and building a multi-step plan.
- **0:50–1:25 — Governance:** a consequential step halts at a one-use approval boundary; change the action and show the prior approval no longer matches.
- **1:25–1:55 — Execution:** approve the exact action; show the downstream service call occur.
- **1:55–2:25 — Receipt:** show the provenance record and replay/audit view.
- **2:25–2:50 — Failure proof:** one denied or unavailable dependency fails closed rather than fabricating success.
- **2:50–3:00 — Close:** why this matters for caretaking, accessibility, and trusted ambient agents.

## Kill gates

Do not submit until all are true:

- real Streamable HTTP/MCP runtime path demonstrated;
- public repo contains everything required to run the submission;
- license is visible at repo root;
- meaningful post-Aug-31 delta is documented and shown in the video;
- approval binding survives an argument-tampering test;
- receipt matches actual executed tools/results;
- demo fits under three minutes;
- no secret, private CAPT source, or private dependency is required by judges.

---

# 2. Nebius x NVIDIA — Flock-Sucker Sovereign Field Sentinel

## Why it is strong

Flock-Sucker is already a real Android sensing product rather than a hackathon shell: BLE, Wi-Fi, cellular, satellite/NTN, GNSS, RF and ultrasonic/audio lanes; evidence-aware classification; repeated sightings; mapping/history; detector-health telemetry; encrypted storage; ephemeral mode; and local-AI paths. That gives the Physical AI entry a visible real-world sensing loop and a strong privacy story.

**Prize target:** compete for the **Overall** cash awards, not merely the Physical AI track hardware award. Current rules allow one Overall **or** Track award **plus one Bonus award**, so an Overall win may also stack with the **$3,000 Tavily bonus** if Tavily is a real runtime component.

## Immediate blocker

`Flock-Sucker` currently has no top-level open-source `LICENSE` file. Before choosing a license, run an SPDX/dependency/license compatibility audit. Do not blindly stamp a license over third-party code.

## Product thesis

**Sovereign Field Sentinel** turns raw local radio/sensor observations into an evidence-ranked field picture without pretending that a radio signature proves identity or intent.

The phone remains the evidence collector and privacy boundary. Nemotron on Nebius performs bounded correlation and competing-hypothesis analysis on a sanitized evidence envelope. Local rules remain available when offline.

## Competition-period build workflow

1. **License/provenance gate.** Inventory owned vs third-party code, choose a compatible top-level OSS license, and record the pre-Aug-26 baseline commit plus competition delta.
2. **Define `EvidenceEnvelope v1`.** Include observation type, bounded identifiers, confidence inputs, temporal/spatial relationship, detector health, evidence source, and explicit redaction fields. Never equate a candidate class with proven intent.
3. **Build the privacy firewall.** Default-deny raw location, personal identifiers, raw audio, faces, contact data, and stable device identifiers from cloud inference. Show the exact payload before external transmission.
4. **Add Nebius runtime inference.** Make a real runtime call to Nebius Token Factory or an AI Cloud deployment using an eligible NVIDIA open-source model. Recommended architecture: fast Nemotron for routine correlation; heavier Nemotron only for ambiguous multi-record synthesis.
5. **Add differential reasoning.** Output `observed`, `supported`, `alternative explanations`, `unknown`, and `recommended next observation`. Model prose never upgrades weak evidence into fact.
6. **Add offline/online handoff.** Local detector pipeline continues without Nebius. Queued sanitized evidence can be reviewed and explicitly released when connectivity returns; cloud result is merged as an annotation, not source truth.
7. **Add optional Tavily evidence lookup.** Only for public, non-personal questions such as vendor/OUI/spec/documentation context. Show the runtime Tavily call and its cited source. Do not send private field data merely to chase the bonus.
8. **Produce field proof.** Automated tests, Android test build, post-Aug-26 delta report, and <3 minute demo with at least one minute showing the phone/sensor modules operating in the real loop.

## Demo storyboard

- live phone scan and proof-of-life telemetry;
- repeated observations become one correlated sighting instead of scroll spam;
- privacy screen shows what remains local vs what can leave device;
- sanitized evidence is sent to Nemotron on Nebius;
- model returns competing explanations and a recommended verification step;
- optional Tavily lookup enriches only public device/manufacturer context;
- disconnect network and show local detection continues;
- reconnect and show reviewed handoff plus provenance.

## Kill gates

- compatible top-level OSS license present and dependency obligations satisfied;
- real Nebius runtime call, not OpenRouter, in the competition build;
- real NVIDIA open-source model used at runtime;
- post-Aug-26 significant delta clearly isolated;
- cloud payload is inspectable and privacy-safe;
- offline mode remains useful;
- one-minute Physical AI proof is visually obvious;
- no claim of surveillance intent from weak RF evidence;
- Tavily, if present, performs a real useful runtime job.

---

# 3. Nebius x NVIDIA — CAPT Sovereign / Personal AI

## Why submit a second NVIDIA project

The rules allow multiple submissions when they are unique and substantially different. CAPT Sovereign is not a Flock reskin: it targets the **Personal AI** track with persistent memory, reusable skills, user-chosen tools/data, explicit authority, and durable receipts.

Its main competitive risk is looking like another generic agent framework. The entry must be a complete personal workflow product with a visible daily-use loop.

## Repo boundary

Create a new self-contained public repository, tentatively `capt-sovereign`.

Do not publish or depend on private CAPT Core. Re-implement/release only a narrow owned kernel:

- local memory store with provenance and deletion/retention controls;
- reusable skill registry;
- scoped tool capabilities;
- one-use approvals for consequential actions;
- execution receipts;
- Nebius/Nemotron provider adapter;
- a small operator UI or CLI suitable for a judge to run.

## Product thesis

A private-by-default personal agent whose **memory and authority stay under the user’s control**, while Nemotron provides reasoning through an explicitly bounded disclosure layer.

## Competition-period build workflow

1. **Define one daily workflow.** Example: morning brief -> prioritize commitments -> draft actions -> request approval -> execute -> remember outcome. Avoid a generic agent playground.
2. **Implement local memory ownership.** Every memory has source, timestamp, scope, retention class and deletion path. Retrieval is visible enough for a judge to understand why an item was used.
3. **Implement reusable skills.** Skills declare required capabilities and data classes before invocation.
4. **Implement capability leases.** File/network/calendar/etc. scope is explicit and expires. Consequential action requires one-use approval bound to arguments.
5. **Implement selective disclosure.** Local context is reduced to a minimum task packet before calling Nemotron on Nebius; raw private stores are not blindly uploaded.
6. **Use model tiering intentionally.** Fast/cheap Nemotron handles routine classification; larger reasoning model handles ambiguous planning. Record model choice and latency/cost in receipts.
7. **Prove failure behavior.** Revoke a capability, mutate an approved action, or remove a dependency and show the workflow stops cleanly.
8. **Ship judge path.** Public repo/license/README, one-command demo fixture, hosted or reproducible Nebius path, test suite, architecture/security note, and <3 minute demo.

## Demo proof

Show the same task across two sessions so persistent memory matters, then force a consequential action through approval. Finish with a provenance view answering: what did the model know, what tools could it use, what did it actually do, and what was retained afterward?

## Kill gates

- submission is meaningfully distinct from Flock-Sucker;
- project works without private CAPT code;
- persistent memory is real, scoped and inspectable;
- skill reuse is demonstrated, not merely configured;
- real Nebius/Nemotron runtime path is captured;
- authority tamper test fails closed;
- the product story is understandable without explaining all of CAPT.

---

# 4. Hack Apertus — CAPTsec Apertus Gauntlet

## Status: HOLD until October 1, 2026 12:00 CEST

Hack Apertus states that challenges are released and hacking begins October 1. Its current terms also require submitted Hackathon Output to be open sourced and require participants to warrant that they built the submitted work during the event.

**Do not create the competition repo or competition implementation before the start signal.** We may design the strategy now.

The strongest current fit is the published **Apertus Readiness -> Red-Teaming Apertus** direction.

## Critical IP boundary

Hack Apertus terms are unusually important here:

- submitted code/model weights default to Apache-2.0;
- documentation/design/text defaults to CC-BY-4.0;
- submitted datasets default to CDLA-Permissive-2.0;
- pre-existing IP necessary to use/reproduce/further develop the output receives a broad compatible license.

Therefore the competition build should be a **clean, standalone open-source implementation created after Oct 1**, inspired by CAPTsec/Arena methods but not dependent on private CAPT source.

## Proposed workflow after challenge release

1. Read the released challenge and freeze an eligibility/scorecard before coding.
2. Create a fresh repo and provenance clock after the official start.
3. Build a deterministic red-team case schema covering factuality, false certainty, privacy leakage, prompt injection, authority escalation, provenance, multilingual/dialect robustness, and cultural assumptions as allowed by the final challenge.
4. Build paired attack/repair evaluation: adversarial prompt -> Apertus result -> independent rubric -> minimal countermeasure -> replay.
5. Add contamination controls so test generation, execution and judging evidence remain separable.
6. Produce reproducible scorecards plus raw case artifacts with hashes and licenses.
7. Add a small public dashboard/CLI that lets judges replay a failure and see exactly why it failed.
8. Submit only if the released challenge explicitly fits the method.

## Kill gates

- challenge does not reward/permit this red-team direction;
- any required private CAPT implementation would have to be exposed;
- dataset provenance/license cannot be proved;
- results cannot be reproduced from the public repo;
- test generator and evaluator are so coupled that the score is meaningless.

---

# 5. Hack Apertus — OpenWatch

## Status: HOLD until October 1

This is the higher-humanitarian but less certain Apertus entry. Current site structure includes **Apertus Adoption -> Own Project**, but the actual challenge packet is released October 1.

## Product thesis

A multilingual evidence explainer for field observations that distinguishes:

- **observed** — what the sensor/person actually recorded;
- **known** — externally verifiable facts;
- **inferred** — hypotheses supported by evidence;
- **unknown** — unresolved uncertainty;
- **next check** — the cheapest observation that could discriminate among explanations.

Apertus's openness and multilingual orientation make this useful for community groups, aid workers, journalists, researchers, and ordinary people who need understandable uncertainty rather than an opaque risk score.

## Boundary

Do not clone Flock-Sucker into the competition. Build a fresh standalone project after Oct 1 that accepts a neutral observation JSON format plus synthetic/public fixtures. Once Flock-Sucker has a compatible explicit license, an optional adapter can be considered **after** final Apertus rules are known.

## Proposed workflow after challenge release

1. Freeze released challenge requirements and create fresh repo after start.
2. Define a minimal observation/evidence schema and public/synthetic fixture set.
3. Use Apertus to generate multilingual explanations with strict evidence labels.
4. Run counterfactual generation: ask what benign and concerning explanations both fit the same observation.
5. Add source/provenance attachments and uncertainty calibration.
6. Add privacy mode that strips identifying fields before inference or sharing.
7. Test across multiple languages/dialects represented by the final challenge.
8. Demo one observation moving from ambiguous raw data to a useful, non-accusatory next-step recommendation.

## Kill gates

- final challenge does not fit Own Project/adoption;
- project needs pre-existing Flock code before compatible licensing is settled;
- multilingual output is merely translation rather than better evidence reasoning;
- the model presents inference as fact;
- fixtures/datasets lack clean provenance.

---

# Cross-entry leverage

## A. Reuse concepts, not submission identity

Amazon Guardian and NVIDIA CAPT Sovereign can share an intentionally public governance vocabulary—capability, approval, receipt, evidence envelope—but their products, code paths and demos must remain substantially different.

Apertus code must be treated separately because the event starts October 1 and its open-source terms are broader. Do not prebuild its competition repositories now.

## B. Competition Delta Manifest

For every existing/donor project, maintain:

- baseline commit and timestamp;
- files/features created during the eligible period;
- test evidence;
- runtime-required technology calls;
- demo timestamps proving each required technology is actually used.

This prevents a late submission scramble over what counts as a significant update.

## C. Judge-proof evidence pattern

Every project should answer the same five questions in under 30 seconds:

1. What did the system observe or know?
2. What did the model infer?
3. What authority was available?
4. What actually executed?
5. What evidence proves the result?

That is the Inversion Labs signature across otherwise distinct products.

---

# Execution order

1. **Amazon CAPT Guardian:** create the narrow public derivative, lock MCP conformance, then build one exceptional caretaking/humanitarian workflow and capture friction logs from the first setup attempt.
2. **Flock-Sucker:** finish license/provenance audit first; then Nebius/Nemotron evidence envelope, offline-online handoff, privacy firewall, Tavily public-evidence enrichment, and physical demo.
3. **CAPT Sovereign:** build only after Guardian's public governance kernel is stable enough to inform—not duplicate—the Personal AI product.
4. **September 30:** freeze Apertus design-only packets. No competition code.
5. **October 1:** read released Apertus challenges, select Gauntlet/OpenWatch/both, then create fresh competition repos and start implementation.

## No-travel assumption

The core strategy uses the online paths only. NVIDIA city-event awards are not part of the expected-value calculation.
