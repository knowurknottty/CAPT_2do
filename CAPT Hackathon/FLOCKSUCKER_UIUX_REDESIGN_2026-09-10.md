# Flock-Sucker UI/UX Redesign — NVIDIA Submission

## Why this is required

The current app is functionally strong but visually reads as a conventional Material 3 Android security app with threat colors layered over generic cards, tabs, and settings surfaces. The NVIDIA submission should not merely add Nemotron to an inherited interface. The competition build should establish an original Inversion Labs product language whose interaction model expresses the evidence discipline already present in the code.

This redesign is therefore **submission-critical work**, not optional polish.

## Product identity

Flock-Sucker should feel like a **portable field instrument + evidence ledger + geospatial investigation console**.

It should not look like:
- a generic antivirus app;
- a hacker-neon dashboard;
- a card wall of raw detections;
- a threat meter that implies certainty the evidence does not support.

It should communicate three things immediately:
1. **What is the environment doing right now?**
2. **What observations appear to belong together over time and space?**
3. **What is observed vs correlated vs inferred vs unknown?**

## Core UX principle: evidence before alarm

Every primary detection/track surface should make epistemic state visible before presenting a threat conclusion.

Use four explicit evidence states:
- **Observed** — directly measured signal/event.
- **Correlated** — multiple observations linked by deterministic/behavioral evidence.
- **Inferred** — model/rule interpretation derived from observations.
- **Unknown** — insufficient evidence for a stronger claim.

Threat severity and evidence confidence are separate dimensions. A weak Flock-like fingerprint must not visually look equivalent to a high-confidence repeated mobile track merely because both map to a concerning class.

## New top-level information architecture

### 1. FIELD
The live operating surface. Replaces the generic Home/Now card feed.

Persistent instrument header:
- scanning state;
- privacy mode / ephemeral mode;
- location state;
- external hardware state;
- local/cloud analyst state;
- last successful observation timestamp.

Below it, a **sensor constellation** shows BLE, Wi-Fi, cellular, GNSS, RF, NTN/satellite, audio/ultrasonic, and external/adversarial sensors as compact live lanes. Each lane exposes health, ingress activity, and last observation without requiring a settings drill-down.

The main stream shows **meaningful changes**, not every callback. New entity, repeated sighting, confidence increase, route continuation, sensor degradation, or analyst conclusion changes should rise to the top.

### 2. TRACKS
Replaces the idea that History is merely a chronological list.

A Track is a persistent candidate entity or correlated observation family. Each track shows:
- first/last seen;
- observation count;
- location diversity;
- identifier rotation/persistence evidence;
- strongest protocol/source evidence;
- current confidence state;
- movement/co-traveler indication;
- whether the conclusion is deterministic, heuristic, or model-assisted.

Repeated sightings collapse into one track instead of flooding the screen with duplicate rows.

### 3. MAP
Map and history become one investigation space rather than separate destinations.

Required behaviors:
- select a track to show its chronological route/observation sequence;
- timeline scrubber or compact event rail;
- cluster unrelated observations at coarse zoom;
- preserve individual sequence at detail zoom;
- show uncertainty in location/evidence rather than implying false GPS precision;
- filter by sensor source, evidence state, confidence, device family, and time window.

### 4. LAB
Technical and analytical surfaces live here rather than occupying primary navigation.

Includes:
- adversarial sensors;
- cellular diagnostics;
- RF/GNSS/ultrasonic detail;
- Flipper/external hardware;
- detector health;
- model analysis/provenance;
- advanced filtering and diagnostic export.

Settings remain accessible globally but should not compete with the four primary jobs.

## Detection/track card redesign

The current left-edge threat-color card should evolve into an **evidence tile**.

Primary row:
- human-readable candidate identity;
- evidence-state badge;
- last-seen age;
- compact source/protocol glyphs.

Secondary row:
- evidence summary in plain language;
- observation count and location count;
- confidence progression if changed.

Expandable evidence drawer:
- raw identifiers/signatures;
- exact detector/rule source;
- correlation factors;
- false-positive analysis;
- model interpretation;
- provenance and timestamps.

Color must not carry meaning alone. Pair color with labels, shapes, line weight, and icons for accessibility.

## Nemotron UX

Nemotron is an **analyst**, never the sensor and never the source of record.

Model-derived content must be visually and semantically separated from raw evidence. Every analysis should show:
- model/provider/runtime provenance;
- evidence IDs/sources consumed;
- conclusion type;
- confidence or uncertainty statement;
- competing hypotheses when applicable;
- timestamp/version;
- explicit distinction between model inference and deterministic classification.

The ideal judge-visible moment is not “AI says this is a threat.” It is:

> 12 observations from 3 sensor lanes appear related. Two hypotheses remain plausible. Here is the evidence for each, what changed since the previous sighting, and what remains unknown.

## Visual language

Direction: **dark field instrument**, not cyberpunk decoration.

- near-black/graphite base with restrained contrast hierarchy;
- active sensor/acquisition accent distinct from evidence confidence;
- amber for uncertainty/attention rather than generic warning spam;
- red reserved for consequential high-confidence conditions;
- model-derived analysis gets a separate visual treatment so it cannot be mistaken for measured data;
- monospace only for identifiers, timestamps, RF/network values, hashes, and provenance—not body copy;
- compact uppercase micro-labels for instrument state where useful;
- subtle grids, traces, dots, and temporal rails are allowed when they encode real state;
- avoid gratuitous glow, fake radar animation, and ornamental spectrum displays.

Material components can remain under the hood, but default Material visual identity should no longer dominate the product.

## Interaction rules

- One tap should answer “why am I seeing this?”
- One tap from a repeated sighting should expose the full track.
- One tap from a track should expose the map/history sequence.
- Raw evidence must never be hidden behind AI analysis.
- Model analysis must never overwrite deterministic evidence.
- Empty states should report scanner health and acquisition status rather than simply saying “nothing found.”
- Advanced mode should reveal depth, not create an entirely different navigation model.
- Pull-to-refresh should represent a deliberate rescan/status refresh, not fake a network-feed metaphor.

## NVIDIA judging/demo flow

The UI redesign should make the Physical AI proof legible in under three minutes:

1. **FIELD** — show live physical sensor acquisition and detector health.
2. Introduce a repeated observation and show it collapse into a **TRACK** instead of duplicating cards.
3. Open **MAP** and show the chronological sighting route/evidence sequence.
4. Trigger Nebius/Nemotron analysis on the evidence envelope.
5. Show competing hypotheses and observed/correlated/inferred/unknown boundaries.
6. Open provenance to prove which observations and runtime produced the conclusion.
7. Demonstrate privacy/offline-online handoff and user control.

This simultaneously demonstrates UI quality, physical-world sensing, model integration, responsible AI, and the product's differentiation.

## Implementation sequencing

### Phase 0 — protect active work
The current `work/adversarial-sensor-suite-r1` tree is dirty and contains active MainScreen/adversarial-sensor changes. Do not overwrite or stash it opportunistically. Capture/commit that work first, then branch the redesign from the resulting state.

### Phase 1 — design system
- replace generic theme semantics with explicit field/evidence/status tokens;
- add instrument surface, evidence-state badge, sensor-lane indicator, provenance label, and track-status primitives;
- establish typography/spacing/shape rules;
- add accessibility semantics and non-color state encoding.

### Phase 2 — FIELD + TRACKS
- refactor MainScreen into Field surface;
- collapse duplicate sightings into track-centric presentation;
- expose sensor health inline;
- move specialized sensor pages out of primary navigation and into Lab.

### Phase 3 — MAP investigation workspace
- unify map + sighting history;
- add selected-track timeline/route overlay;
- preserve current bounded clustering and truthful GPS/evidence semantics.

### Phase 4 — LAB + Nemotron analyst
- integrate adversarial sensors and diagnostics;
- create analyst panel with explicit provenance and evidence boundaries;
- keep raw evidence accessible independently of cloud/model availability.

### Phase 5 — verification
- Compose/unit tests for state rendering and evidence semantics;
- build/install target variant;
- ADB UI-tree navigation checks;
- screenshots at primary states;
- accessibility/content-description pass;
- demo rehearsal on physical hardware;
- verify no regression to scanning, storage, map history, or detector-health behavior.

## Hard gates

Do not call the redesign finished unless:
- a fresh user can distinguish observed data from model inference without explanation;
- repeated sightings are represented as a coherent track instead of duplicate-feed spam;
- scanner health is visible from the primary operating surface;
- the map can explain the temporal history of a selected track;
- the UI remains useful with cloud AI disabled;
- critical state is not encoded by color alone;
- no existing detector/storage/privacy semantics are weakened;
- the NVIDIA demo can prove the physical → evidence → Nemotron → provenance chain live.

## Immediate next action

First capture the active adversarial-sensor branch safely. Then create an isolated `hackathon/flocksucker-field-ui-r1` branch/worktree from that exact state and implement the redesign in the order above. Do not redesign directly on top of uncommitted sensor work.