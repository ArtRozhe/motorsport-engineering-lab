# Learning Roadmap

## Direction

The current direction is toward **Motorsport Data & Performance Software Engineering**.

The objective is to combine existing professional software engineering experience with competence in:

- Python and scientific computing;
- telemetry and time-series analysis;
- mathematics for engineering;
- numerical methods;
- signal processing;
- vehicle dynamics fundamentals;
- motorsport performance analysis;
- engineering visualization;
- real-time telemetry systems;
- technical English.

This roadmap is intentionally more detailed in the near term than in the long term.

The further the planning horizon, the greater the uncertainty.

---

## Planning model

### Near term: 0–12 weeks

Plan in detail.

### Medium term: 3–6 months

Define directions and measurable outcomes, but adjust based on actual progress.

### Longer term: 6–18 months

Treat as a hypothesis rather than a fixed curriculum.

Market requirements, demonstrated strengths, weaknesses, and personal interest should influence the direction.

### Time budget and phase completion

The sustainable budget is **7–9 hours per week** — roughly 100 hours across the first 12 weeks.

Week numbers in this roadmap are **indicative, not deadlines**. A phase is complete when its target outcome is demonstrated. Depth of understanding is not cut to keep to a schedule.

To keep drift visible, the structured review happens after Phase 3 or at week 16, whichever comes first.

---

## Phase 0 — Baseline

Before planning Phase 1 in detail, run a short baseline diagnostic without preparation or AI assistance:

- functions and graphs;
- derivatives and integrals;
- vectors;
- units and dimensional reasoning applied to telemetry.

The purpose is not to pass or fail. It sets the starting point for Phase 1.

---

## Phase 1 — Foundations

**Indicative horizon:** Weeks 1–4 (not a deadline)

### Software

- engineering Python;
- environments and packages;
- type annotations;
- NumPy;
- DataFrame workflows;
- basic visualization;
- testing;
- initial telemetry ingestion.

### Mathematics

- functions and graphs;
- units and dimensional reasoning;
- coordinate systems;
- vectors;
- derivatives;
- integrals as engineering concepts;
- numerical differentiation;
- numerical integration.

### Telemetry

- channels;
- timestamps;
- sampling;
- distance;
- speed;
- RPM;
- gear;
- throttle;
- brake;
- position;
- basic data-quality inspection.

### Motorsport

- lap and sector structure;
- braking;
- corner entry;
- apex;
- corner exit;
- throttle application;
- basic racing line concepts;
- tyres and stints;
- track evolution.

### Target outcome

Independently take two real laps and:

1. inspect the telemetry;
2. identify important data-quality characteristics;
3. synchronize the laps on a meaningful axis;
4. visualize relevant channels;
5. calculate lap delta;
6. identify where time was gained or lost;
7. explain the process and its limitations.

### Plan

Planned after the [Phase 0 baseline](progress.md#phase-0-baseline--2026-10-06-to-2026-10-08). Each step answers a question about real data; the mathematics is introduced where the data needs it.

**Dataset:** human laps from [Assetto Corsa Gym](https://huggingface.co/datasets/dasgringuen/assettoCorsaGym) (CC BY 4.0), in MoTeC `.ld` format. Several drivers lapped the same car and track, which allows lap-to-lap and driver-to-driver comparison. It is simulator data: methods transfer to real cars, conclusions about vehicle behaviour do not. Real F1 data (OpenF1 / FastF1) is kept as the unfamiliar-data test at the end of the phase.

| # | Step | Baseline gap addressed |
|---|------|------------------------|
| 1 | Working Python project setup: packaging, pytest, first test | — |
| 2 | Obtain the dataset, document it in `data/README.md`, identify the processing done by the source and the parser | Data policy |
| 3 | Raw inspection: timestamps, sampling intervals, per-channel sample rates, gaps, duplicates, units | Sampling period vs frequency, timestamps |
| 4 | Longitudinal acceleration from speed: forward vs central differences, effect of resolution | Meaning of the derivative, finite differences, quantisation noise |
| 5 | Distance from speed by numerical integration, compared with the lap distance channel; differentiate it back as a self-check | Integration as accumulated area, trapezoidal rule |
| 6 | Track map from position; distances between samples as vectors | Vectors, distance between two positions |
| 7 | Synchronise two laps on distance with linear interpolation; lap delta; where time is gained or lost | Phase 1 target outcome |

Linear interpolation is pulled forward from Phase 2 because lap synchronisation depends on it. Trigonometry, frame rotation and periodic signals stay in Phase 2.

Motorsport reading (lap structure, braking, corner entry, apex, exit) runs alongside steps 3–7 rather than as a separate block.

The estimate is 5–6 weeks at the current time budget.

### Resources

First encounter with a concept may use Russian sources; application and explanation are in English.

| Step | Concept | Resource |
|------|---------|----------|
| 3 | Sampling, quantisation | S. W. Smith, *The Scientist and Engineer's Guide to Digital Signal Processing* (free at dspguide.com), ch. 3 |
| 4–5 | Derivative and integral, intuition | Я. Б. Зельдович, *Высшая математика для начинающих и её приложения к физике*, chapters on derivatives and integrals; 3Blue1Brown, *Essence of Calculus* (video), ch. 1–8 |
| 4–5, 7 | Numerical methods in Python | Kong, Siauw, Bayen, *Python Programming and Numerical Methods* (free at pythonnumericalmethods.studentorg.berkeley.edu), ch. 20 (differentiation), 21 (integration), 17 (interpolation) |
| 6 | Vectors | 3Blue1Brown, *Essence of Linear Algebra* (video), ch. 1–2 |
| 3–7 | Racecar data practice | J. Segers, *Analysis Techniques for Racecar Data Acquisition* (SAE) |

---

## Phase 2 — From telemetry to analysis

**Indicative horizon:** Weeks 5–8 (not a deadline)

### Data and signals

- interpolation;
- resampling;
- irregular sampling;
- noise;
- smoothing;
- low-pass filtering;
- numerical differentiation;
- numerical integration;
- basic descriptive statistics.

### Geometry and dynamics

- velocity and acceleration vectors;
- longitudinal acceleration;
- lateral acceleration;
- curvature;
- corner radius;
- basic load transfer;
- grip;
- traction;
- braking;
- understeer and oversteer;
- basic aerodynamic concepts.

### Performance analysis

Develop methods for estimating and comparing:

- braking zones;
- braking points;
- minimum corner speed;
- throttle application;
- exit speed;
- major gain/loss regions.

Explicitly distinguish observation from interpretation.

### Target outcome

Given two laps, produce a structured comparison of the major differences and explain which conclusions are supported by the available telemetry and which remain hypotheses.

---

## Phase 3 — Engineering software

**Indicative horizon:** Weeks 9–12 (not a deadline)

Turn understood analysis methods into usable engineering software.

Potential areas:

- reusable Python analysis modules;
- API layer;
- React/TypeScript engineering UI;
- synchronized telemetry charts;
- track visualization;
- lap comparison;
- corner analysis;
- testing;
- profiling;
- caching;
- data validation;
- documentation;
- containerization where useful.

Avoid infrastructure that does not yet solve a real problem.

### Target outcome

**Telemetry Workbench v0.1**

A small but technically understood application for exploring and comparing racing telemetry.

Every important part of the analysis should be explainable and defensible.

---

## Review after Phase 3

After Phase 3, or at week 16 at the latest, perform a structured review.

Evaluate:

- Python competence;
- mathematical understanding;
- telemetry analysis;
- signal-processing fundamentals;
- software architecture;
- motorsport understanding;
- vehicle dynamics understanding;
- technical English;
- independence from AI assistance;
- personal interest in each area.

Repeat a market scan of relevant motorsport roles and compare requirements with demonstrated skills.

Do not automatically continue the original roadmap.

Choose the next phase based on evidence.

---

## Possible Phase 4 directions

These are intentionally provisional.

Potential topics include:

- real-time telemetry;
- WebSockets and streaming;
- binary data formats;
- high-frequency data;
- time-series storage;
- deeper statistics;
- advanced signal processing;
- deeper vehicle dynamics;
- scientific visualization;
- Python performance;
- simulation;
- motorsport-specific analysis tools;
- C++ where justified;
- MATLAB/Simulink where justified.

The correct subset should be selected later.

---

## Longer-term hypothesis

If progress and interest support the direction:

**0–3 months**

Build foundations and complete the first telemetry analysis system.

**3–6 months**

Develop deeper data, signals, performance, and real-time competence.

**6–12 months**

Develop one strong engineering project, deepen domain knowledge, perform technical interview practice, and begin selective market validation.

**12–18 months**

Potentially pursue relevant roles in:

- motorsport engineering software;
- telemetry/data software;
- performance software;
- simulation tooling;
- scientific visualization;
- race-support software.

Formula 1 is one possible destination, not the only definition of success.

---

## Working principle

Do not study a technology because it appears on a roadmap.

Introduce it when one of three things is true:

1. it solves a problem encountered in the project;
2. it is foundational knowledge required to understand the problem correctly;
3. repeated market evidence shows that it is important for the target role.
