# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPTVid`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P0

### 21. [Vincentwei1021/video-shotcraft](https://github.com/Vincentwei1021/video-shotcraft)

**Route:** SKILL NOW
**License evidence:** Apache-2.0
**Action:** Integrate Shotcraft shot recipes and motion-planning workflow into CAPTVid.
**Guardrail:** Prefer reusable shot grammar over copying generated templates blindly.

### 22. [remotion-dev/remotion](https://github.com/remotion-dev/remotion)

**Route:** ECOSYSTEM
**License evidence:** NOASSERTION
**Action:** Use Remotion as a first-class programmatic render backend for CAPTVid where licensing/runtime fit is confirmed.
**Guardrail:** Keep renderer replaceable; upstream repo metadata did not assert a simple SPDX license.

## P1

### 42. [ShandaAI/AlayaRenderer](https://github.com/ShandaAI/AlayaRenderer)

**Route:** ECOSYSTEM
**License evidence:** Apache-2.0
**Action:** Prototype AlayaRenderer as an optional world/render backend for generative scenes and simulation visuals.
**Guardrail:** Keep isolated from core; GPU/runtime cost and maturity require benchmarks.

### 95. [calesthio/OpenMontage](https://github.com/calesthio/OpenMontage)

**Route:** REFERENCE
**License evidence:** AGPL-3.0
**Action:** Mine OpenMontage's production-pipeline taxonomy, tools and skill organization for CAPTVid.
**Guardrail:** AGPL-3.0 and enormous scope; use as reference unless isolation/compliance is explicit.

## P3

### 77. [codecflow/conductor](https://github.com/codecflow/conductor)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep codecflow Conductor as a browser-control-to-RTMP reference for agent visualization/streaming experiments.
**Guardrail:** Tiny project with no asserted license; not a runtime donor.

### 100. [https://github.com/descriptinc](https://github.com/descriptinc)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep Descript's public GitHub organization as a future audio/video tooling discovery source.
**Guardrail:** Organization-level link is too broad for integration.
