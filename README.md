# IIS — Information and Measurement System

## Overview
IIS is an engineering model for aggregating heterogeneous system parameters
into a unified scalar index describing the functional state of a system.

The project focuses on structural clarity, constraints, and interpretability.
It is **not** a medical diagnostic tool and **not** an AI-based system.

## Purpose
The purpose of this project is to demonstrate:
- system-level modeling of complex states,
- aggregation of indirect and heterogeneous parameters,
- transparent assumptions and limitations in engineering models.

IIS is intended as a conceptual and analytical foundation,
not as a production-ready solution.

## Core idea
The model transforms normalized input parameters into a single index using:
1. weighted linear aggregation,
2. non-linear normalization via a sigmoid function.

This approach allows flexible interpretation while maintaining
structural simplicity and control over model behavior.

## Model description
The detailed mathematical formulation and parameter definitions
are provided in the following documents:
- `docs/model.md`
- `formulas/core_model.tex`

## Inputs
Input parameters represent indirectly measurable aspects of system state.
All parameters are normalized to the range [0, 1].

Parameter semantics, normalization logic, and assumptions
are described in `docs/model.md`.

## Output
The output value IIS ∈ (0, 1) represents a relative indicator
of the aggregated functional state of the system.

The index does **not** provide absolute measurements or diagnoses
and must be interpreted within documented constraints.

## Assumptions
All core assumptions underlying the model are explicitly documented in:
- `docs/assumptions.md`

## Limitations
Known limitations, boundary conditions, and non-applicable scenarios
are described in:
- `docs/limitations.md`

## Ethical constraints
Ethical and usage constraints, including age-related and contextual limitations,
are described in:
- `docs/ethics.md`

## Project status
Current status: **Conceptual engineering model**

- No production code
- No empirical validation
- Focus on structure, reasoning, and transparency

## Contribution
Feedback on model structure, assumptions, and limitations is welcome.
This project prioritizes critical review over feature expansion.

## Author
Zixcidus
