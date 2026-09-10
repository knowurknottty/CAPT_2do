# Donor Queue — 2026-09-10

Sorted donor candidates whose **primary destination** is `CAPTsec Red`. See the root `DONOR_TRIAGE_2026-09-10.md` for complete corpus and cross-cutting rationale.

## P1

### 56. [DependableSystemsLab/ravage](https://github.com/DependableSystemsLab/ravage)

**Route:** REFERENCE
**License evidence:** CC0-1.0
**Action:** Study RAVAGE robotic attack-injection methodology only for authorized simulation/red-team fixtures involving GPS/IMU faults.
**Guardrail:** Dual-use physical attack capability; no real-world offensive integration.

### 80. [conductor-oss/conductor-agents](https://github.com/conductor-oss/conductor-agents)

**Route:** CORE CHERRY-PICK
**License evidence:** Apache-2.0
**Action:** Mine Conductor Agents security/coding harness structure for long-running parallel harnesses with safety gates and restart durability.
**Guardrail:** Security harness must remain authorized/sandboxed; Conductor dependency should not leak into CAPT core.

### 104. DISCOVER:Nextfil

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Create a discovery ticket for Nextfil and compare its Linux CLI behavior to the desired CAPTsec Red capability before designing a CAPT-native equivalent.
**Guardrail:** Source was unresolved in the paste; no implementation until identity/function are verified.

## P2

### 103. [https://github.com/XPSec-Security](https://github.com/XPSec-Security)

**Route:** REFERENCE
**License evidence:** not asserted / n/a
**Action:** Keep XPSec Security organization as a security-tool discovery source; select concrete repos before any integration decision.
**Guardrail:** Organization-level reference plus offensive-security risk requires repo-by-repo review.
