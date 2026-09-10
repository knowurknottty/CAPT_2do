# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPTSmith`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P0

### 2. [humanlayer/skills](https://github.com/humanlayer/skills/blob/main/plugins/show-me/skills/show-me/SKILL.md)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate an Inversion-Labs visual-explanation skill for diagrams, code-shapes and focused HTML artifacts.
**Guardrail:** Keep output minimal and verifiable; avoid decorative diagram spam.

### 3. [humanlayer/skills](https://github.com/humanlayer/skills/blob/main/plugins/build-iterated-agentic-loop/skills/build-iterated-agentic-loop/SKILL.md)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Adapt into a governed iterated-loop skill that installs repo-local skill/workflow/memory templates with explicit approval gates.
**Guardrail:** Do not create autonomous CI loops without bounded budgets and human authority.

### 6. [mattpocock/skills](https://github.com/mattpocock/skills/blob/main/skills/engineering/ask-matt/SKILL.md)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Fork concept into Ask CAPT: route a user request to the best CAPT skill/flow/variant.
**Guardrail:** Router must use capabilities and task evidence, not brittle keyword dispatch.

### 7. [mattpocock/skills](https://github.com/mattpocock/skills/blob/main/skills/engineering/code-review/SKILL.md)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Expand code-review into six-axis CAPT review: spec, standards, security, tests, architecture, and operational/provenance risk.
**Guardrail:** Avoid review theater; every axis needs evidence and pass/fail criteria.

### 9. [mattpocock/skills](https://github.com/mattpocock/skills/blob/main/skills/engineering/to-spec/SKILL.md)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate conversation-to-spec synthesis with repo/tracker provenance.
**Guardrail:** Never invent requirements absent from conversation or code evidence.

### 10. [mattpocock/skills](https://github.com/mattpocock/skills/blob/main/skills/engineering/to-tickets/SKILL.md)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate tracer-bullet ticket decomposition with explicit dependency edges.
**Guardrail:** Avoid atomizing work into fake parallelism.

### 11. [mattpocock/skills](https://github.com/mattpocock/skills/blob/main/skills/engineering/implement/SKILL.md)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate spec/ticket implementation flow with TDD seams, review, and verification-before-commit.
**Guardrail:** Must respect CAPT approval and current branch/worktree ownership.

### 12. [mattpocock/skills](https://github.com/mattpocock/skills/blob/main/skills/engineering/wayfinder/SKILL.md)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Adapt Wayfinder for multi-session programs using decision tickets and unresolved-blocker maps.
**Guardrail:** Do not confuse planning tickets with implementation completion.

### 17. [cathrynlavery/diagram-design](https://github.com/cathrynlavery/diagram-design)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate editorial diagram-design grammar as a companion/upgrade to show-me.
**Guardrail:** Normalize overlapping diagram skills into one CAPT visual grammar.

### 50. [coderamp-labs/gitingest](https://github.com/coderamp-labs/gitingest)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate a governed git-ingest skill that turns repos into bounded prompt/evidence packs with provenance and size controls.
**Guardrail:** Untrusted repository text must remain data, never instructions.

### 70. [miqdadbadjuber/anti-slop](https://github.com/miqdadbadjuber/anti-slop)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate anti-slop as a CAPT-specific quality filter for generic UI/text/code, adapted into positive measurable criteria.
**Guardrail:** Pure prohibitions can cause brittle style; pair with task-specific quality rubrics.

### 81. [smixs/skill-conductor](https://github.com/smixs/skill-conductor)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate Skill Conductor concepts: architecture-first skill design, BinEval, threshold-blind judging, cross-family calibration and gated self-update.
**Guardrail:** Meta-skill can recursively amplify bad criteria; require frozen eval banks and rollback.

### 88. [alibaba/open-code-review](https://github.com/alibaba/open-code-review)

**Route:** CORE CHERRY-PICK
**License evidence:** Apache-2.0
**Action:** Extract Alibaba Open Code Review's deterministic-plus-LLM hybrid review pipeline into the six-axis CAPT review skill.
**Guardrail:** Security rules and language analyzers need independent tests; do not trust model comments alone.

### 97. [tt-a1i/archify](https://github.com/tt-a1i/archify)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate Archify-style verifiable architecture/workflow/sequence/data-flow HTML diagrams with motion/export.
**Guardrail:** Merge with show-me/diagram-design rather than creating three overlapping visual skills.

## P1

### 8. [mattpocock/skills](https://github.com/mattpocock/skills/blob/main/skills/engineering/grill-with-docs/SKILL.md)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Adapt grill-with-docs into requirement interrogation plus ADR/glossary capture for ambiguous engineering work.
**Guardrail:** Do not interrogate when sufficient requirements already exist.

### 83. [conductor-oss/conductor-skills](https://github.com/conductor-oss/conductor-skills)

**Route:** SKILL NOW
**License evidence:** Apache-2.0
**Action:** Mine Conductor Skills for workflow review/scaffolding patterns, especially reliability/security checklists and human WAIT semantics.
**Guardrail:** Keep CAPT-native terminology and runtime boundaries; do not couple skill to Conductor.

## P2

### 14. [pingdotgg/t3code](https://github.com/pingdotgg/t3code)

**Route:** REFERENCE
**License evidence:** MIT
**Action:** Study t3code interaction and coding-workspace UX for CAPT developer surfaces.
**Guardrail:** Do not clone another editor/product wholesale.

### 23. [chuspeeism/dashi-ppt-skill](https://github.com/chuspeeism/dashi-ppt-skill)

**Route:** REFERENCE
**License evidence:** AGPL-3.0
**Action:** Mine Dashi presentation workflow/themes for editable slide-generation patterns.
**Guardrail:** AGPL; reference patterns unless compatibility is explicitly cleared.

### 35. [composio-community/awesome-claude-plugins](https://github.com/composio-community/awesome-claude-plugins)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep awesome-claude-plugins as a discovery index for future skill/plugin scouting.
**Guardrail:** Curated list is not vetted code; every downstream item needs its own review.

### 36. [hashgraph-online/awesome-ai-plugins](https://github.com/hashgraph-online/awesome-ai-plugins)

**Route:** REFERENCE
**License evidence:** Apache-2.0
**Action:** Keep awesome-ai-plugins as cross-agent plugin discovery/reference.
**Guardrail:** Treat popularity as discovery signal, not trust.

### 44. [voideditor/void](https://github.com/voideditor/void)

**Route:** REFERENCE
**License evidence:** Apache-2.0
**Action:** Reference Void for open-source AI-editor UX and developer workflow patterns.
**Guardrail:** Do not create another editor unless a CAPT-specific gap justifies it.

### 64. [visionik/deft](https://github.com/visionik/deft)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Keep deft/directive as a software-agent best-practices comparison source.
**Guardrail:** No asserted license; guidelines can conflict with CAPT's stricter governance.

### 72. [langflow-ai/langflow](https://github.com/langflow-ai/langflow)

**Route:** REFERENCE
**License evidence:** MIT
**Action:** Reference Langflow's visual workflow builder and component model.
**Guardrail:** Large overlapping platform; no reason to embed whole system.

### 84. [anomalyco/opencode](https://github.com/anomalyco/opencode)

**Route:** REFERENCE
**License evidence:** MIT
**Action:** Use OpenCode as a reference implementation for open coding-agent UX, tools and provider interoperability.
**Guardrail:** Full coding agent overlaps existing stack.

### 86. [Microck/opencode-studio](https://github.com/Microck/opencode-studio)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Study OpenCode Studio's secure local configuration-management UX.
**Guardrail:** No asserted license metadata; external editor-specific surface.

### 90. [opensoft/oh-my-opencode](https://github.com/opensoft/oh-my-opencode)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Mine oh-my-opencode for async-agent, LSP/AST and curated-tool ergonomics after a license review.
**Guardrail:** No asserted license; high overlap and hype-heavy positioning.

### 101. [https://github.com/awesome-skills](https://github.com/awesome-skills)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep awesome-skills organization as a skill-discovery source.
**Guardrail:** Organization-level index is unvetted; each candidate needs individual review.

### 111. [https://repolyze.mxcorp.in](https://repolyze.mxcorp.in)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep Repolyze as a benchmark for repo-analysis UX and report categories.
**Guardrail:** External AI analysis is not trusted evidence; CAPT should reproduce useful checks deterministically where possible.

## P3

### 85. [jjmartres/opencode](https://github.com/jjmartres/opencode)

**Route:** REFERENCE
**License evidence:** MIT
**Action:** Keep jjmartres/opencode config as a secondary configuration/skill-layout reference.
**Guardrail:** Opinionated fork with low unique leverage.

### 87. [https://github.com/topics/opencode-plugin](https://github.com/topics/opencode-plugin)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep opencode-plugin topic page as discovery-only index.
**Guardrail:** Unvetted topic results.

### 89. [https://github.com/topics/opencode-agent](https://github.com/topics/opencode-agent)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep opencode-agent topic page as discovery-only index.
**Guardrail:** Unvetted topic results.
