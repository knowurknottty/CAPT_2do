# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPTMem`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P1

### 62. [garrytan/gbrain](https://github.com/garrytan/gbrain)

**Route:** CORE CHERRY-PICK
**License evidence:** MIT
**Action:** Extract gbrain knowledge-graph traversal, synthesis and gap-analysis ideas into CAPTMem with provenance controls.
**Guardrail:** Opinionated agent-brain assumptions may not match CAPT; port primitives only.

### 66. [electric-sql/pglite](https://github.com/electric-sql/pglite)

**Route:** CORE CHERRY-PICK
**License evidence:** Apache-2.0
**Action:** Prototype PGlite-backed embedded relational/event state for local-first CAPT modules where SQLite is insufficient.
**Guardrail:** Do not replace stable stores without migration, durability and concurrency evidence.

## P2

### 54. [appflowy-io/appflowy](https://github.com/appflowy-io/appflowy)

**Route:** REFERENCE
**License evidence:** AGPL-3.0
**Action:** Study AppFlowy local-first workspace/data ownership patterns for CAPTMem UX.
**Guardrail:** AGPL and huge scope; no platform import.

### 61. [toeverything/affine](https://github.com/toeverything/affine)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Study AFFiNE privacy-first/local workspace architecture for CAPTMem and collaborative knowledge surfaces.
**Guardrail:** No asserted license metadata in collected evidence; huge overlap with workspace products.
