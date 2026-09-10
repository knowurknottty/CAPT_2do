# Hackathon Entry Workflows — 2026-09-10

## Executive decision

Run two serious entries now: **Amazon CAPT Guardian / Relay** and **Nebius x NVIDIA Flock-Sucker Sovereign Field Sentinel**. Keep **NVIDIA CAPT Sovereign** as a second-wave submission only after the first two are demonstrably on-track. Keep both **Hack Apertus** concepts on a hard **HOLD until 2026-10-01**, when the challenges and final track requirements are released.

Priority order by expected value and readiness:

1. Amazon — CAPT Guardian / Relay for Alexa+
2. NVIDIA — Flock-Sucker Sovereign Field Sentinel
3. NVIDIA — CAPT Sovereign / Personal AI
4. Apertus — OpenWatch (HOLD until Oct 1)
5. Apertus — CAPTsec Gauntlet (HOLD until Oct 1)

## Council execution evidence

The council was dispatched as a true vessel fan-out, not model-parallel/role-serial execution.

- Matrix requested: **9 OpenRouter models × 8 independent vessel roles = 72 vessels**.
- Geometry proof: **72 barrier parties, 72 unique worker threads, 2.809 ms release spread, 139.314 s wall time** for the primary fan-out.
- Each vessel used an isolated CAPT runtime/ledger.
- Failed cells were recovered only in parallel batches; successful cells were not rerun.
- Final merged valid outputs: **55/72 accepted**.
- Complete 8/8 accepted: `glm-5.3-flash`, `deepseek-v4-flash-0731`, `hy3`, `qwen3.8-flash`, `nemotron-3.5-lightning`, `nemotron-3-super-120b-a12b`.
- `nemotron-3-ultra-550b-a55b`: **7/8 accepted**; one repo-architect cell still returned no canonical answer content after recovery.
- `nemotron-3-nano-omni-30b-a3b-reasoning:free`: **0/8**, blocked by the current OpenRouter workspace guardrail; no substitute vote was fabricated.
- `qwen3.7-flash`: **0/8**, blocked by the current OpenRouter workspace guardrail; no substitute vote was fabricated.

A reasoning-budget compatibility issue in the older stable CAPT driver was isolated: several current OpenRouter reasoning models can consume the response budget in `message.reasoning` and return no `message.content`. Recovery used explicit bounded reasoning while preserving CAPT approval and digest binding. No CAPT authority checks were disabled.

## Structured vote signal

Of the accepted responses, **24 produced clean machine-parseable JSON ballots** in the requested schema. Those ballots gave:

- Entry A / Amazon Guardian: **22 GO, 2 HOLD**
- Entry B / NVIDIA Flock-Sucker: **19 GO, 4 HOLD, 1 missing**
- Entry C / NVIDIA CAPT Sovereign: **8 GO, 14 HOLD, 1 KILL, 1 missing**
- Entry D / Apertus OpenWatch: **2 GO, 21 HOLD, 1 missing**
- Entry E / Apertus CAPTsec: **2 GO, 21 HOLD, 1 missing**

The HOLDs on D/E are mostly rule-timing discipline: Apertus challenges are not released until Oct 1.

## Rule facts that control the plan

### Amazon — Build, Ship, Shape

- Submission deadline: **2026-10-23 12:00 PDT**.
- Organizations are eligible.
- Public GitHub repository, visible open-source license and functional setup instructions are required.
- Existing work may be significantly updated during the competition window; the delta must be explained.
- Alexa+ accepts a working Agent Skill or a **self-hosted MCP server implementing MCP >= 2025-11-25 over Streamable HTTP**.
- Required technology must execute at runtime, not merely appear in documentation.
- Alexa+ first prize: **$25,000 cash**.
- Open Source mini challenge: **$5,000 cash + $5,000 AWS credits**.
- AWS Builder mini challenge: **$5,000 cash + $5,000 AWS credits**.
- One project can win one track prize plus one mini challenge, so the practical Alexa+ cash ceiling is **$30,000**.

### Nebius x NVIDIA Global AI Hackathon

- Submission deadline: **2026-10-30 10:00 PDT**.
- Working software must run on **Nebius Token Factory or Nebius AI Cloud** and use at least one NVIDIA open-source model.
- Public open-source repo, license, setup instructions and a public demo under three minutes are required.
- Existing work must be significantly updated during the hackathon window and the delta explained.
- Multiple submissions are allowed only when unique/substantially different.
- Relevant tracks: **Physical AI** and **Personal AI**.
- Stage-one risk: superficial API/model rebrands are rejected.
- Grand prize: **$20,000**; second: **$10,000**; third: **$6,000**.
- Tavily bonus: **$3,000**.
- **Current official stacking rule: each project may win one Overall OR one Track award AND one Bonus award. Therefore Grand Prize + Tavily can stack for a $23,000 cash ceiling.**
- OpenRouter calls used during development/review do not satisfy the Nebius runtime requirement.

### Hack Apertus

- Hack window: **2026-10-01 through 2026-10-16**.
- Challenges release **2026-10-01 12:00 CEST**.
- Competition project must be new and started during the hackathon period.
- Track-specific submission requirements are not final yet.
- Design/specification may happen now, but **do not create the competition repo/project before Oct 1**.

---

# Entry A — Amazon: CAPT Guardian / Relay for Alexa+

## Verdict

**GO — highest expected-value entry.** It combines the highest realizable cash ceiling with the least speculative infrastructure work.

## Existing advantage

`CAPT Workspace MCP` already has authenticated Streamable HTTP, real transport E2E tests, and documented MCP 2025-11-25 support. That covers Amazon's protocol floor. The contest work should therefore not be a generic MCP wrapper; it should demonstrate a stateful governed Alexa+ workflow that judges can understand immediately.

## Public repository boundary

Create a **new narrow public repository** containing only intentionally released owned code:

- MCP 2025-11-25 Streamable HTTP transport
- Alexa+/agent-facing tool definitions
- approval boundary
- workflow state machine
- provenance/receipt schema
- reproducible tests and demo fixtures

Do **not** publish `CAPT-Inversion-Labs` or the full private `CAPT Workspace MCP` repository.

Suggested product/repo name: **CAPT Guardian Relay**.

## Winning workflow

1. **Human intent:** user asks Alexa+ for a meaningful caretaking/humanitarian workflow, such as preparing a household for severe weather, coordinating a caregiver task, or organizing an accessibility-sensitive errand.
2. **Alexa+ → MCP:** Alexa+ invokes the self-hosted CAPT MCP endpoint over Streamable HTTP.
3. **Intent decomposition:** CAPT turns the request into bounded subtasks and separates informative from consequential operations.
4. **Multi-service orchestration:** read-only tools gather facts/resources; CAPT reconciles conflicts and tracks provenance.
5. **Human authority gate:** consequential external actions pause for explicit user approval.
6. **Execution:** only approved actions execute; denied/stale actions fail closed.
7. **Receipt:** CAPT emits human- and machine-readable provenance showing request, evidence, approval and actual outcome.
8. **Alexa summary:** Alexa+ explains the result in ordinary language and exposes the receipt on demand.

## Demo sequence

Ten-second hook: **“Alexa can call agents. CAPT makes those agents accountable to you.”**

Show one uninterrupted flow: Alexa+ request → live MCP call → evidence gathering → reconciliation → consequential action pauses → user approval → action completes → receipt appears.

The differentiator is not tool count. It is visible **authority + orchestration + provenance**.

## Mini-challenge target

Default target: **Open Source mini challenge**. Build a genuinely reusable public CAPT MCP/approval component during the competition window. Choose AWS Builder instead only if AWS becomes architecturally necessary rather than prize ornamentation.

## Kill gates

Do not submit until:

- visible OSS license
- MCP >= 2025-11-25 negotiation proven
- Streamable HTTP E2E green
- Alexa+/simulation invokes real runtime code
- approval cannot be bypassed
- receipt derives from actual execution state
- competition-period delta documented
- cold-start setup works from README
- three-minute demo is understandable without CAPT background knowledge

---

# Entry B — NVIDIA: Flock-Sucker Sovereign Field Sentinel

## Verdict

**GO — strongest differentiated NVIDIA entry and strongest humanitarian/physical-world fit.**

## Immediate blocker

The public Flock-Sucker repo currently has **no top-level OSS LICENSE**. Fix this deliberately before submission; vendored third-party licenses do not satisfy the repository requirement.

## Existing advantage

Flock-Sucker already has real sensor ingestion, multi-domain observations, confidence boundaries, repeated-sighting correlation, history/map surfaces, detector health, encrypted storage, ephemeral operation, local inference and external-radio/physical-device integration.

The competition work should turn Nemotron into the **evidence-reconciliation engine**, not a chatbot bolted onto the app.

## Competition workflow

1. **Physical observation:** Android/Flipper/ESP32 or another supported sensor emits observations into Flock-Sucker's canonical pipeline.
2. **Local normalization:** deterministic rules deduplicate, classify and preserve evidence/confidence boundaries.
3. **Privacy gate:** only a minimized evidence bundle leaves the device; ephemeral/local-only operation remains available.
4. **Nebius handoff:** authorized cloud reasoning sends the bounded evidence bundle to an NVIDIA open-source model actually running on Nebius.
5. **Nemotron reconciliation:** compare observations and produce competing hypotheses: same moving platform, unrelated devices, or insufficient evidence.
6. **Evidence-aware result:** output explicitly separates **observed / known / inferred / unknown** and ties inference to source observations.
7. **Governance:** high-impact claims cannot be promoted beyond the evidence/confidence boundary.
8. **Field return:** interpretation appears on-device/map with an auditable explanation.

## Humanitarian scenario

Prefer a scenario useful without encouraging evasion or confrontation: journalist, humanitarian field worker, disaster-response volunteer, domestic-violence survivor, civil-rights observer, or ordinary traveler understanding nearby sensing infrastructure while minimizing data disclosure.

The claim is **situational awareness and evidence interpretation**, not attribution of intent.

## Physical AI demo

The first minute should visibly prove physical-world input: phone and/or Flipper/ESP32 → local observations → bounded cloud handoff → Nemotron reconciliation on Nebius → evidence-aware map/result.

## Tavily

Tavily is worthwhile only for real evidence enrichment: manufacturer documentation, public device identifiers, published infrastructure details, etc. Its output must enter the same provenance envelope. Because NVIDIA permits one Bonus alongside an Overall/Track award, **Grand + Tavily has a $23k cash ceiling** if both are won.

## Kill gates

- top-level OSS license
- explicit competition-period delta
- live Nebius runtime proof
- NVIDIA open-source model called there
- physical input shown clearly
- no unsupported surveillance/intent claims
- offline/local mode retained
- cloud payload data-minimized
- reproducible known fixture plus live physical run

---

# Entry C — NVIDIA: CAPT Sovereign / Personal AI

## Verdict

**HOLD behind A and B.** Technical fit is excellent, but it creates another public-derivative/release burden and risks splitting effort before the stronger entries are golden.

## Activation condition

Activate only after Amazon A and NVIDIA B pass first end-to-end competition gates with enough calendar margin remaining.

## Workflow

1. User explicitly chooses data/tool sources.
2. Persistent memory stores only consented durable context.
3. Nemotron on Nebius performs planning/reasoning.
4. Reusable skills execute through bounded capabilities.
5. Sensitive actions pause for human approval.
6. Consequential tool calls receive provenance and receipts.
7. Local/cloud routing is visible and policy-controlled.
8. User can inspect/revoke memory, permissions and current authority.

Flock-Sucker must remain clearly Physical AI/environmental sensing; CAPT Sovereign must remain Personal AI/governed persistent agency.

---

# Entry D — Apertus: OpenWatch

## Verdict

**HOLD until 2026-10-01. Do not create the competition project early.**

## Pre-hack design only

A new Apertus-native interpretation layer that may consume Flock-Sucker exports as an external dependency if final rules permit.

Semantic contract:

- what was **observed**
- what is **known** from reliable references
- what is **inferred**
- what remains **unknown**
- competing explanations
- multilingual explanation using Apertus
- privacy-preserving export/share

On Oct 1, read the released challenge and final track rules before initializing the repo. Kill or reshape immediately if the released challenge does not reward this use case or restricts pre-existing dependencies.

---

# Entry E — Apertus: CAPTsec Gauntlet

## Verdict

**HOLD until 2026-10-01. Do not create the competition project early.**

## Pre-hack design only

A clean new red-team/evaluation harness inspired by owned CAPTsec/Arena methods, not copied wholesale from private repositories.

Candidate workflow after challenge release:

1. ingest official Apertus challenge categories
2. generate bounded adversarial test families
3. run deterministic/reproducible prompts and perturbations
4. score privacy, bias/cultural representation, factuality and other official categories
5. preserve model/config/version provenance
6. deduplicate failure families
7. produce minimally sufficient reproducible issue packets
8. verify fixes/regressions when applicable

The value is not “we can jailbreak an LLM.” It is **reproducible failure discovery with evidence strong enough to repair**.

---

# Shared execution plan

## Zero-regret work first

1. Decide and add an appropriate top-level OSS license to Flock-Sucker.
2. Define the intentionally public CAPT derivative boundary for Amazon before copying code.
3. Build one reusable `EvidenceEnvelope` / receipt contract that can serve Amazon Guardian, Flock-Sucker/Nemotron and later Apertus without exposing private CAPT internals.
4. Maintain `competition-delta.md` from day one in every eligible repo, separating pre-existing from competition-period work.
5. Build judge-visible runtime evidence: health endpoint, protocol/model identity where safe, provenance receipt and deterministic fixture.

## Recommended work order

**Lane A — Amazon:** public derivative → MCP transport/spec gate → Alexa+ end-to-end → approval/receipt → open-source contribution gate → demo hardening.

**Lane B — NVIDIA/Flock:** license → Nebius/Nemotron canary → minimized EvidenceEnvelope → reconciliation engine → physical live demo → privacy/adversarial testing.

**Lane C — NVIDIA/CAPT:** dormant until A/B green.

**Lane D/E — Apertus:** specifications only until Oct 1; instantiate competition repos after challenge/rule release.

## Submission philosophy

Do not optimize for “technically eligible.” Optimize for **judge-verifiable inevitability**:

- required platform visibly performs indispensable work
- demo has one clear human problem
- behavior is reproducible
- claims are bounded by evidence
- private Inversion Labs IP remains private
- every contest feature leaves behind a useful production capability

That is the common thread the council converged on.