# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPT Node`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P0

### 67. [CopilotKit/openbot](https://github.com/CopilotKit/openbot)

**Route:** CORE CHERRY-PICK
**License evidence:** MIT
**Action:** Extract OpenBot's one-computer-per-agent isolation, pre-action decision and post-action recording patterns into CAPT Node.
**Guardrail:** Avoid duplicating CAPT governance; use it to strengthen isolation/execution receipts.

### 69. [tencentcloud/CubeSandbox](https://github.com/tencentcloud/CubeSandbox)

**Route:** CORE CHERRY-PICK
**License evidence:** NOASSERTION
**Action:** Evaluate CubeSandbox's instant concurrent sandbox architecture as a donor for CAPT Node isolation/runtime startup.
**Guardrail:** No asserted license in collected metadata; security claims require adversarial verification.

### 93. [herdrdev/herdr](https://github.com/herdrdev/herdr)

**Route:** CORE CHERRY-PICK
**License evidence:** Apache-2.0
**Action:** Mine Herdr's Rust agent-runtime isolation, fleet lifecycle and execution-environment patterns for CAPT Node.
**Guardrail:** Do not replace CAPT runtime wholesale; benchmark isolation/security semantics first.

## P1

### 13. [magnitudedev/magnitude](https://github.com/magnitudedev/magnitude)

**Route:** CORE CHERRY-PICK
**License evidence:** Apache-2.0
**Action:** Extract hardware profiling, model-fit recommendation and runtime tuning into CAPT Node provider/model placement.
**Guardrail:** Recommendations require measured device evidence; no opaque auto-downloads.

### 48. [activepieces/activepieces](https://github.com/activepieces/activepieces)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Study Activepieces integration breadth and MCP/workflow UX for connector coverage strategy.
**Guardrail:** Huge automation platform; avoid dependency and unreviewed connectors.

### 49. [n8n-io/n8n](https://github.com/n8n-io/n8n)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Study n8n workflow/integration patterns for orchestration UX and connector taxonomy.
**Guardrail:** Fair-code/large-platform concerns; no wholesale embedding.

## P2

### 71. [AKKI0511/AgentConnect](https://github.com/AKKI0511/AgentConnect)

**Route:** REFERENCE
**License evidence:** Apache-2.0
**Action:** Study AgentConnect decentralized collaboration protocol for future cross-node agent coordination.
**Guardrail:** Low adoption; do not add protocol complexity without a concrete CAPT use case.
