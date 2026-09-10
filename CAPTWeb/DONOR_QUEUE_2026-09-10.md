# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPTWeb`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P1

### 20. [oso95/scroll-world](https://github.com/oso95/scroll-world)

**Route:** SKILL NOW
**License evidence:** MIT
**Action:** Keep scroll-world as an optional immersive web-experience skill for Inversion Labs/CAPT launches.
**Guardrail:** High visual novelty but low core value; never make it a dependency.

### 25. [airbnb/lottie-web](https://github.com/airbnb/lottie-web)

**Route:** ECOSYSTEM
**License evidence:** MIT
**Action:** Support Lottie animation assets for lightweight web/mobile motion where useful.
**Guardrail:** Animation must respect performance and reduced-motion settings.

### 27. [matraic/m3e](https://github.com/matraic/m3e)

**Route:** ECOSYSTEM
**License evidence:** MIT
**Action:** Evaluate Material 3 Expressive component patterns for CAPT web surfaces.
**Guardrail:** Small project; verify accessibility and maturity before adoption.

### 30. [posthog/posthog](https://github.com/posthog/posthog)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Reference PostHog observability, session-replay and experiment patterns for CAPT product telemetry.
**Guardrail:** Huge product and unclear repo license metadata; do not import platform wholesale.

### 45. [open-webui/open-webui](https://github.com/open-webui/open-webui)

**Route:** REFERENCE
**License evidence:** NOASSERTION
**Action:** Study Open WebUI provider/model UX, local-model management and extension surfaces.
**Guardrail:** Large product with licensing ambiguity; pattern donor only.

### 53. [plausible/analytics](https://github.com/plausible/analytics)

**Route:** ECOSYSTEM
**License evidence:** AGPL-3.0
**Action:** Use Plausible-compatible privacy-first analytics for public CAPT/Inversion Labs web surfaces if needed.
**Guardrail:** AGPL/server deployment boundary; collect only necessary telemetry.

### 107. [https://21st.dev](https://21st.dev)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Use 21st.dev as a curated component/inspiration source for polished web UI.
**Guardrail:** Third-party components need license/accessibility/performance review individually.

### 110. [https://60fps.design](https://60fps.design)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Use 60fps.design as a motion/interaction benchmark for CAPTWeb and macOS polish.
**Guardrail:** Reference examples must be translated into accessible, reduced-motion-safe behavior.

## P2

### 16. [tooljet/tooljet](https://github.com/tooljet/tooljet)

**Route:** REFERENCE
**License evidence:** AGPL-3.0
**Action:** Reference ToolJet AI for visual internal-tool/workflow builder patterns.
**Guardrail:** AGPL and massive surface area; no direct incorporation into CAPT core.

### 55. [penpot/penpot](https://github.com/penpot/penpot)

**Route:** REFERENCE
**License evidence:** MPL-2.0
**Action:** Keep Penpot as design-system/prototyping reference and possible external workflow tool.
**Guardrail:** MPL boundary and full design platform scope make core integration unnecessary.

### 106. [https://v0.app](https://v0.app)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Use v0.app as a design/prototyping benchmark for CAPTWeb, not as architecture authority.
**Guardrail:** External hosted tool; generated code still needs CAPT review and ownership checks.

### 108. [https://glass3d.dev](https://glass3d.dev)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep Glass3d.dev as a visual-effect prototyping reference for selective 3D glass treatments.
**Guardrail:** Aesthetic utility only; avoid generic glassmorphism or performance regressions.

### 109. [https://cta.gallery](https://cta.gallery)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep CTA.gallery as a conversion-layout reference for launch pages.
**Guardrail:** Design inspiration only; do not copy brand-specific creative work.

### 112. [https://metatags.io](https://metatags.io)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Use MetaTags.io as a lightweight metadata/social-preview QA reference for public sites.
**Guardrail:** External preview tool only; canonical metadata should be tested in CI.

## P3

### 32. [https://developer.chrome.com](https://developer.chrome.com)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep Chrome for Developers root as a general web implementation reference only.
**Guardrail:** Too broad to be an actionable donor.
