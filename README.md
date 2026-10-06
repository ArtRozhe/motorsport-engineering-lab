# Motorsport Engineering Lab

A hands-on learning and experimentation repository focused on motorsport telemetry, data analysis, signal processing, vehicle performance, and engineering software.

## About

I'm a software engineer with a background primarily in frontend and product engineering, expanding my skills into motorsport data and performance engineering.

This repository documents that process through practical experiments, engineering exercises, and software built around real racing data.

The goal is **not to build a polished telemetry product as quickly as possible**. The goal is to understand the engineering behind it.

That means working through the mathematics, data, algorithms, assumptions, and limitations myself — not just producing software that appears to work.

## What I'm learning

The current areas of focus are:

- Python for scientific and engineering computing
- telemetry and time-series data analysis
- numerical methods
- signal processing
- motorsport telemetry concepts
- vehicle dynamics and performance fundamentals
- engineering data visualization
- real-time data processing and telemetry software architecture
- technical communication in English

The scope will evolve as my understanding of the domain grows.

## Learning approach

This repository is intentionally a laboratory rather than a finished product.

The process matters as much as the result.

Experiments, intermediate implementations, incorrect assumptions, failed approaches, and subsequent corrections may remain visible in the repository when they provide useful evidence of the engineering process.

A typical learning cycle looks like this:

1. Understand the problem.
2. Form an initial hypothesis.
3. Work through the relevant mathematics or engineering concepts.
4. Implement the solution.
5. Validate it against the data.
6. Investigate unexpected results.
7. Document what worked, what failed, and what remains uncertain.
8. Refactor useful experimental work into maintainable software.

## AI usage

AI tools are used in this repository as learning, research, and review tools — not as a substitute for engineering work.

Tasks are divided into three modes:

### 🧠 SOLO

The task develops a skill I am actively learning.

I work through the reasoning and implementation independently. AI may help explain concepts or provide progressively stronger hints, but it should not provide the implementation or final solution.

### 🤖 REVIEW ONLY

I complete the task first.

AI may then review the implementation, challenge assumptions, identify weaknesses, suggest tests, or discuss alternative approaches.

I remain responsible for making the changes.

### 🤖 AI OK

AI assistance may be used more freely for work outside the current learning objective, such as routine boilerplate or areas in which I already have sufficient experience.

The purpose of these rules is simple: **working software is not evidence of learning if I cannot explain, reproduce, debug, and defend the engineering decisions behind it.**

Git history shows honestly who did the work. Commits where AI wrote the content carry a `Co-Authored-By` trailer; commits with limited AI help carry an `AI-Assisted:` trailer describing it; commits without a trailer are my own work.

More detailed instructions for AI-assisted work are documented in [`CLAUDE.md`](./CLAUDE.md).

## Engineering principles

A few principles guide the work in this repository:

### Evidence before interpretation

Telemetry analysis should distinguish between:

- **measured values** — directly present in the source data;
- **derived values** — calculated from measured data;
- **assumptions** — conditions accepted for an analysis;
- **interpretations** — possible explanations of what the data means.

An interpretation should never be presented as a measured fact.

### Understand before abstracting

Experiments may begin in notebooks or small scripts.

Reusable concepts should only be extracted into the main codebase after the underlying problem is sufficiently understood.

### Validate the data

Before trusting an analysis, inspect:

- units;
- sampling intervals;
- missing samples;
- outliers;
- interpolation;
- filtering;
- numerical error;
- limitations of the original data source.

### Prefer understanding over complexity

The project should not adopt technologies simply because they are common in production systems.

New infrastructure should be introduced when a real problem creates a reason to learn or use it.

## Repository structure

The repository starts intentionally small and will evolve with the work.

```text
motorsport-engineering-lab/
├── data/
│   └── README.md         # dataset sources, licenses, limitations (data itself is not committed)
├── docs/
│   ├── roadmap.md        # learning direction
│   ├── progress.md       # demonstrated competence, with evidence
│   └── engineering-log.md
├── CLAUDE.md             # working agreement for AI assistance
└── README.md
```

Planned as soon as there is work to put in them:

- `experiments/` — exploratory scripts (`.py` files with `# %%` cells);
- `src/motorsport_lab/` — reusable, understood and tested analysis code;
- `tests/`.

As experiments and applications emerge, the structure will grow to reflect actual requirements rather than a speculative architecture.

## Current status

**Phase:** 0 — Baseline

A short diagnostic sets the starting point. Phase 1 (Foundations) follows, with an initial focus on:

- Python for engineering work
- working with real telemetry data
- numerical foundations
- telemetry sampling and time-series concepts
- first lap-analysis experiments

See [`docs/roadmap.md`](./docs/roadmap.md) for the current learning direction and [`docs/progress.md`](./docs/progress.md) for demonstrated progress.

## Long-term direction

The current direction is toward software engineering roles around motorsport data and vehicle performance, including areas such as:

- telemetry analysis;
- performance analysis tooling;
- engineering software;
- scientific visualization;
- simulation support;
- real-time telemetry systems.

Formula 1 is an area of particular interest, but the skills developed here are intentionally not tied to a single racing series.

The longer-term direction will be adjusted based on what I learn, which parts of the domain prove most interesting, and what the motorsport engineering market actually requires.
