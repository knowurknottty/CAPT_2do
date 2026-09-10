# Nemotron Donor Council Receipt — 2026-09-10

## Requested geometry

Three free NVIDIA Nemotron models were assigned three vessels each. Vessel execution was parallel-only: one independent CAPT runtime per vessel, barrier-released, with no shared runtime ledger.

- `nvidia/nemotron-3.5-lightning:free`: 3 vessels
- `nvidia/nemotron-3-super-120b-a12b:free`: 3 vessels
- `nvidia/nemotron-3-ultra-550b-a55b:free`: 3 vessels

## Primary ballot fan-out

Revision `nemo-triage-r3-finalballot` ran 9 vessels on 9 unique worker threads behind a 9-party barrier. Barrier release spread was **0.108 ms**. Super returned all three compact ballot partitions; Ultra returned partition 1; Lightning returned no canonical answer content on all three partitions.

## Recovery evidence

- `r4`: 5 parallel recovery vessels, 5 unique threads, **0.073 ms** release spread. Ultra partition 2 recovered; Lightning remained empty; Ultra partition 3 remained empty.
- `r5`: 4 parallel recovery vessels, 4 unique threads, **0.057 ms** release spread. Ultra partition 3 returned provider content, but the 8,192-character CAPT observation was analysis rather than a complete compact ballot, so it was not treated as a valid classification vote. Lightning remained empty.
- `r6`: 3 Lightning vessels, 3 unique threads, **0.076 ms** release spread; no canonical answer content.
- `r7`: 3 focused Lightning vessels on ~3 KB high-value packets, 3 unique threads, **0.089 ms** release spread; no canonical answer content.

## Adjudication rule

Model output was advisory, never authoritative. Super supplied one complete independent pass; Ultra supplied valid compact ballots for partitions 1 and 2 plus an incomplete analytical response for partition 3. Lightning supplied no usable ballots despite repeated parallel-only recovery attempts. Final routing therefore used the valid Nemo evidence plus source metadata/README or exact linked skill-file evidence and human architectural adjudication. No Lightning votes were invented or substituted.

See `DONOR_TRIAGE_2026-09-10.md` for the authoritative 112-target ledger.
