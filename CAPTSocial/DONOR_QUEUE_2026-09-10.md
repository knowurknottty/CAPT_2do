# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPTSocial`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P1

### 4. [blader/humanizer](https://github.com/blader/humanizer)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate as optional humanization/editing skill for outward-facing copy while preserving factual meaning.
**Guardrail:** Must not hide provenance or fabricate human authorship claims.

### 34. [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Integrate selected marketing/CRO skills for launches, copy, SEO and analytics without touching core runtime behavior.
**Guardrail:** Marketing guidance must not optimize for manipulation or unsupported claims.

### 47. [languagetool-org/languagetool](https://github.com/languagetool-org/languagetool)

**Route:** ECOSYSTEM
**License evidence:** LGPL-2.1
**Action:** Integrate LanguageTool-compatible grammar/style checks as a deterministic pre/post-processing option.
**Guardrail:** LGPL boundary; keep service/process interface clean.
