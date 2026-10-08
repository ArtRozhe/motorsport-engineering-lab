# Learning Progress

This document tracks **demonstrated competence**, not topics encountered.

A concept is not considered learned merely because I have read about it, discussed it with AI, followed a tutorial, or produced working generated code.

Every status change must link to concrete evidence: a commit, an engineering log entry, or a knowledge-check result. Work completed through the SOLO emergency exit does not count as evidence.

## Status definitions

**Not assessed**  
Prior experience may exist, but competence has not yet been demonstrated in this repository.

**Not started**  
No meaningful practical work yet.

**Exploring**  
Currently learning the concept and applying it with significant guidance.

**Practicing**  
Can apply the concept to familiar problems but still require review or occasional help.

**Independent**  
Can apply and explain the concept independently in unfamiliar but reasonably scoped situations.

**Strong**  
Can reason about trade-offs, limitations, edge cases, and alternative approaches with professional confidence.

---

## Python / Scientific Computing

### Engineering Python

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### NumPy

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### DataFrame processing

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### Testing numerical/data code

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

---

## Mathematics / Numerical Methods

### Units and dimensional reasoning

**Status:** Practicing

**Evidence:**

- [Phase 0 baseline](#phase-0-baseline--2026-10-06-to-2026-10-08): correct unit conversions (km/h ↔ m/s, g ↔ m/s², rpm ↔ rev/s), caught a unit error in a distance calculation, checked the units of `v²/r`, derived wheel speed from rotation rate (4.1, 4.3–4.5); reasoned about scaling from formula structure (drag `∝ v²`, power `∝ v³`, 1.3).

**Needs work:**

- Converting between sampling frequency and sampling period: 100 Hz was converted to 1 ms instead of 10 ms (4.2).

### Vectors and coordinate systems

**Status:** Not started

**Evidence:**

—

**Needs work:**

- Recognising positions and displacements as vectors: Pythagoras was applied to accelerations and velocities but not to two GPS positions ([Phase 0 baseline](#phase-0-baseline--2026-10-06-to-2026-10-08), 3.3).
- Transforming vectors between a body frame and a map frame (3.5).
- Trigonometry for vector components and angles.

### Derivatives and numerical differentiation

**Status:** Not started

**Evidence:**

—

**Needs work:**

- Stating what a derivative means ([Phase 0 baseline](#phase-0-baseline--2026-10-06-to-2026-10-08), 2.1).
- Differentiation rules: sum rule, chain rule, derivatives of `e^x` and `sin x` (2.2).
- Which point in time a finite difference actually estimates; forward vs central differences (2.3).
- Effect of sensor resolution on derived acceleration: the calculation was correct, but the conclusion that a naive derivative is dominated by quantisation noise was not drawn (2.6).

### Integration and numerical integration

**Status:** Not started

**Evidence:**

—

**Needs work:**

- Calculating the area under a speed–time graph: the intuition (area = distance) was present, but no method to compute it ([Phase 0 baseline](#phase-0-baseline--2026-10-06-to-2026-10-08), 2.4).
- Estimating distance from sampled speed, e.g. the trapezoidal rule, and its error sources (2.5).

### Interpolation and resampling

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### Statistics

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

---

## Signal Processing

### Sampling

**Status:** Not started

**Evidence:**

—

**Needs work:**

- Relationship between sampling frequency and period ([Phase 0 baseline](#phase-0-baseline--2026-10-06-to-2026-10-08), 4.2).
- What timestamps are and what irregular intervals indicate (4.2).
- Periodic signals (amplitude, frequency, period) and what happens when a signal is sampled too slowly (1.5).

### Noise and filtering

**Status:** Not started

**Evidence:**

—

**Needs work:**

- Recognising that differentiating a quantised channel amplifies noise ([Phase 0 baseline](#phase-0-baseline--2026-10-06-to-2026-10-08), 2.6).

---

## Telemetry

### Telemetry data inspection

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### Lap synchronization

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### Lap delta analysis

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### Corner analysis

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

---

## Vehicle Performance

### Corner phases

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### Longitudinal dynamics

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### Lateral dynamics

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

### Tyres and grip

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

---

## Engineering Software

Existing professional software engineering skills are not tracked comprehensively here.

Only skills specifically relevant to the new engineering domain should be recorded.

### Engineering data visualization

**Status:** Not assessed

**Evidence:**

Existing visualization/software experience exists, but competence with engineering telemetry visualization has not yet been demonstrated in this repository.

**Needs work:**

- telemetry-specific interaction patterns;
- large time-series datasets;
- scientific visualization conventions.

### Real-time telemetry systems

**Status:** Not started

**Evidence:**

—

**Needs work:**

—

---

## Technical English

Statuses here are backed by private, local-only notes on recurring patterns.

### Explaining engineering decisions

**Status:** Not assessed

**Evidence:**

—

**Needs work:**

—

### Discussing uncertainty and assumptions

**Status:** Not assessed

**Evidence:**

—

**Needs work:**

—

### Technical interview communication

**Status:** Not assessed

**Evidence:**

—

**Needs work:**

—

---

# Recurring weaknesses

### To watch: applying a known tool when the problem is framed differently

Not yet confirmed as recurring. In the [Phase 0 baseline](#phase-0-baseline--2026-10-06-to-2026-10-08), Pythagoras was used correctly for combined acceleration and velocity (3.2, 3.4) but not for the distance between two GPS positions (3.3). Distance = speed × time was used correctly (4.3) but not to find the distance covered under constant deceleration (2.4).

---

# Topics to revisit

None recorded yet.

---

# Knowledge checks

## Phase 0 baseline — 2026-10-06 to 2026-10-08

Diagnostic without preparation or outside help, completed over several sittings. Four blocks: functions and graphs, derivatives and integrals, vectors, units and dimensional reasoning. Purpose: set the starting point for Phase 1, not pass or fail.

**Strong**

- Unit conversions and dimensional checks.
- Proportional reasoning from the structure of a formula (how drag and power scale with speed).
- Substituting into formulas and checking that results make physical sense; questioned where an exponential cooling model stops matching reality.

**Rusty**

- Differentiation rules (chain rule, `e^x`, `sin x`).
- Logarithms: solved an exponential equation up to the final step, which needed `ln`.
- Stating what a derivative means.

**Missing**

- Integration as accumulated area and numerical integration (trapezoidal rule).
- Trigonometry and periodic signals: amplitude, frequency, period, sampling a periodic signal.
- Vector components and rotation between coordinate frames.
- Sampling period vs frequency and the meaning of timestamps.

**Pattern to watch:** a known tool was not applied when the problem was framed differently (see Recurring weaknesses).
