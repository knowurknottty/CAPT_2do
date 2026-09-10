# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPT Core`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P0

### 1. [ruvnet/ruflo](https://github.com/ruvnet/ruflo)

**Route:** CORE CHERRY-PICK
**License evidence:** MIT
**Action:** Extract swarm coordination, adaptive-memory and self-learning primitives; reimplement behind CAPT governors.
**Guardrail:** Large overlapping harness; do not import wholesale.

### 5. [affaan-m/ECC](https://github.com/affaan-m/ECC)

**Route:** CORE CHERRY-PICK
**License evidence:** MIT
**Action:** Mine ECC for harness performance, memory, security and research-first gaps; port only independently valuable primitives.
**Guardrail:** High overlap with CAPT; require red-first regressions per donor.

### 43. [lsdefine/genericagent](https://github.com/lsdefine/genericagent)

**Route:** CORE CHERRY-PICK
**License evidence:** MIT
**Action:** Extract GenericAgent's self-evolving skill-tree and token-efficiency ideas into governed skill evolution with rollback/evals.
**Guardrail:** Self-modification must be gated, versioned and reversible.

### 73. [conductor-oss/conductor](https://github.com/conductor-oss/conductor)

**Route:** CORE CHERRY-PICK
**License evidence:** Apache-2.0
**Action:** Extract Conductor OSS durable graph semantics: fan-out, retries, approvals, cancellation, waits and restart-safe state.
**Guardrail:** Do not import Java platform wholesale; reproduce only CAPT-missing invariants.

### 99. [nousresearch/hermes-agent](https://github.com/nousresearch/hermes-agent)

**Route:** CORE CHERRY-PICK
**License evidence:** MIT
**Action:** Continue mining Hermes Agent for persistent memory, skill growth, tool/runtime and self-improvement primitives compatible with CAPT's existing Hermes bridge.
**Guardrail:** Avoid duplicate runtime authority; CAPT remains governor and evidence ledger.

## P1

### 39. [walkinglabs/awesome-harness-engineering](https://github.com/walkinglabs/awesome-harness-engineering)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Maintain walkinglabs harness-engineering list as a donor-discovery feed for architecture/evals/security.
**Guardrail:** Reference collection only; verify primary sources.

### 40. [leezythu/Awesome-Harness-Self-Improvement](https://github.com/leezythu/Awesome-Harness-Self-Improvement)

**Route:** REFERENCE
**License evidence:** MIT
**Action:** Maintain harness-self-improvement reading list for recursive-improvement research.
**Guardrail:** Do not convert unverified self-improvement claims into runtime policy.

### 41. [ai-boost/awesome-harness-engineering](https://github.com/ai-boost/awesome-harness-engineering)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Maintain ai-boost harness list as a second discovery source and compare deltas with other lists.
**Guardrail:** Deduplicate aggressively; no-license metadata means reference only.

### 82. [ryanmac/code-conductor](https://github.com/ryanmac/code-conductor)

**Route:** CORE CHERRY-PICK
**License evidence:** MIT
**Action:** Extract Code Conductor's isolated-worktree parallel coding and task-claim patterns into CAPT development cohorts.
**Guardrail:** Avoid auto-merge defaults; preserve CAPT approval/verification gates.

## P2

### 78. [https://conductor-oss.org/](https://conductor-oss.org/)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep Conductor OSS site/docs beside target 73 as operational reference.
**Guardrail:** Duplicate informational surface, not separate code donor.

### 91. [code-yeongyu/oh-my-openagent](https://github.com/code-yeongyu/oh-my-openagent/issues)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Study oh-my-openagent graph-engineering and mass-parallel interaction patterns as a design reference.
**Guardrail:** No asserted license and opaque terminology; require code-level validation before promotion.

## P3

### 75. [netflix/conductor](https://github.com/netflix/conductor)

**Route:** REFERENCE
**License evidence:** Apache-2.0
**Action:** Keep Netflix Conductor as historical architecture/reference only; use maintained Conductor OSS for current work.
**Guardrail:** Netflix repo has been unmaintained since 2023.
