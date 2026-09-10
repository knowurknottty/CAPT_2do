# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPT Mobile`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P1

### 19. [software-mansion/argent](https://github.com/software-mansion/argent)

**Route:** ECOSYSTEM
**License evidence:** Apache-2.0
**Action:** Use Argent patterns/tools for controlled mobile app inspection, debugging and profiling.
**Guardrail:** Keep device control explicit, scoped and auditable.

## P2

### 68. [ionic-team/capacitor](https://github.com/ionic-team/capacitor)

**Route:** REFERENCE
**License evidence:** MIT
**Action:** Keep Capacitor as a cross-platform delivery option for thin CAPT clients.
**Guardrail:** Native Android/macOS paths may be superior; do not standardize prematurely.

## P3

### 76. [bluelinelabs/conductor](https://github.com/bluelinelabs/conductor)

**Route:** REFERENCE
**License evidence:** Apache-2.0
**Action:** File BlueLineLabs Conductor as Android-navigation reference only.
**Guardrail:** View-based Android framework is peripheral to current Compose/CAPT architecture.
