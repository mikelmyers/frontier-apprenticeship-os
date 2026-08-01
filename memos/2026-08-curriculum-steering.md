# Frontier Apprenticeship OS — August 2026 Curriculum Steering

## Decision

**Remain in Module 000 — Foundation Bridge Track.**

The advanced aerospace/frontier sequence is not yet unlocked because the repository does not contain enough completed foundation evidence to verify the bridge completion standard.

This is an evidence decision, not a judgment that no learning occurred. The latest visible repository activity is the June 4 setup of Module 000; no July exercise, quiz, memo, simulation, or mastery artifacts are currently committed.

## One-Year Goal

The target remains:

> Frontier-adjacent competence in AI-assisted autonomous space infrastructure engineering, demonstrated through an autonomous depot network simulator and technical white paper.

The destination is unchanged. The near-term curriculum is being narrowed so the apprentice can build the mathematical, programming, and simulation fluency needed to reach it.

## Current Evidence Assessment

### Verified in the repository

- Foundation Bridge curriculum exists.
- Lessons 001–006 exist.
- Exercise, quiz, and memo directories exist.
- The capstone specification exists.

### Not yet verified in the repository

- Apprentice-written Python exercise files
- Completed quiz answers
- Concept memos in the apprentice's own words
- Debugging evidence
- Motion or gravity simulations
- A Module 000 mastery review

Because these items are not visible, the curriculum cannot responsibly infer that Python, notation, vectors, motion, forces, gravity, or simulation are becoming comfortable.

## August Module Emphasis

August should be treated as a **foundation execution month**, not an expansion month.

### Allocation

- 35% Python fluency and debugging
- 25% notation and vector literacy
- 20% motion and discrete simulation
- 10% forces and gravity intuition
- 10% engineering explanation and artifact quality

## Four-Week Plan

### Week 1 — Re-enter and Verify

Complete and commit Lessons 001–006.

Required evidence:

- six manually typed Python exercise files
- six quiz files
- one short memo explaining `r_rel`, `||r_rel||`, and `v_rel` in plain English
- one correction log describing at least one error found and fixed

Do not optimize or refactor prematurely. The goal is correct understanding.

### Week 2 — Python as an Engineering Tool

Focus:

- functions
- parameters and return values
- conditionals
- loops
- dictionaries as telemetry packets
- defensive checks

Required artifact:

`simulations/foundation/vector_state_tools.py`

It should contain small, understood functions for:

- vector subtraction
- vector magnitude
- relative position
- relative velocity
- distance-zone classification

### Week 3 — From Snapshot to Simulation

Focus:

- time steps
- updating position from velocity
- updating velocity from acceleration
- recording telemetry
- plotting a trajectory
- understanding why step size matters

Required artifact:

`simulations/foundation/simple_vehicle_motion.py`

The apprentice must be able to explain every state update without relying on AI-generated prose.

### Week 4 — Foundation Capstone Slice

Build:

`simulations/foundation/depot_approach_monitor_v0_1.py`

Minimum capabilities:

- depot and vehicle state
- relative position
- range
- relative velocity
- repeated time steps
- approach-zone classification
- basic abort warning
- telemetry output

Supporting memo:

`memos/000-foundation-bridge/depot-approach-monitor-v0-1.md`

The memo should explain assumptions, what the program can and cannot determine, and what would be required for a more realistic model.

## Capstone Direction

The capstone remains the Autonomous Depot Network Simulator, but August work should only build its lowest-level primitives.

The depot approach monitor is the correct capstone slice because it creates reusable concepts without pretending to model orbital rendezvous yet:

- object state
- relative state
- time evolution
- safety logic
- telemetry
- documented assumptions

No orbital mechanics, CR3BP, Kalman filtering, or advanced autonomy should be introduced as required problem sets this month. They may appear only as plain-English previews showing why the current foundation matters.

## August Evidence Goals

By the next monthly review, the repository should contain at minimum:

1. Lessons 001–006 exercise artifacts
2. Lessons 001–006 quiz answers
3. One notation/vector concept memo
4. One debugging/correction log
5. `vector_state_tools.py`
6. `simple_vehicle_motion.py`
7. `depot_approach_monitor_v0_1.py`
8. A short technical memo for the approach monitor
9. At least five tests covering vector and range calculations
10. A final Module 000 self-explanation recorded in writing

## Advancement Gate

Module 000 should advance toward Module 01 only when the apprentice can, without copying a solution:

- explain position, velocity, acceleration, relative position, relative velocity, and magnitude
- manually write the relevant Python calculations
- use functions and loops to run a simple time-stepped simulation
- identify and fix basic Python errors
- test known cases such as a `[3, 4, 0]` vector having magnitude `5`
- explain assumptions and limitations in plain English

A score below 3/5 in conceptual understanding, notation fluency, Python implementation, debugging, or artifact quality triggers repair work rather than advancement.

## Steering Summary

The one-year goal and final capstone remain sound. The immediate risk is not that the program is too basic; it is that lesson generation outruns committed evidence and demonstrated understanding. August therefore prioritizes execution, review, and a small working depot-approach artifact before any return to the advanced sequence.
