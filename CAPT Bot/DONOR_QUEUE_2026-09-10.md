# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPT Bot`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P1

### 18. [caronc/apprise](https://github.com/caronc/apprise)

**Route:** ECOSYSTEM
**License evidence:** BSD-2-Clause
**Action:** Add Apprise-style pluggable outbound notification transport behind CAPT Bot/Node authority gates.
**Guardrail:** Notification fan-out can leak data; destination allowlists required.
