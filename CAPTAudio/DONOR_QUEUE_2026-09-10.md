# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPTAudio`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P0

### 52. [openai/whisper](https://github.com/openai/whisper)

**Route:** CORE CHERRY-PICK
**License evidence:** MIT
**Action:** Use Whisper as a supported local transcription engine behind a replaceable CAPTAudio interface.
**Guardrail:** Model/data privacy and hardware sizing must be explicit.

## P1

### 63. [saurabhav88/EnviousWispr](https://github.com/saurabhav88/EnviousWispr)

**Route:** CORE CHERRY-PICK
**License evidence:** GPL-3.0
**Action:** Mine EnviousWispr for low-latency local dictation, dual-engine fallback and macOS privacy UX.
**Guardrail:** GPL boundary; reimplement architecture or isolate integration.
