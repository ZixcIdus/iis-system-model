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

- weighted linear aggregation,
- non-linear normalization via a sigmoid function.

This approach allows flexible interpretation while maintaining
structural simplicity and control over model behavior.

## Core mathematical model
The IIS model aggregates normalized input parameters into a single
scalar index using weighted linear aggregation followed by
non-linear normalization.

### Inputs
All input parameters are normalized to the range \([0, 1]\):

- \(A\) — activity-related parameter  
- \(\Gamma\) — stress-related parameter  
- \(H\) — stability parameter  
- \(V\) — variability parameter  

### Linear aggregation
The raw aggregated value is defined as:

$$
\mathrm{IIS}_{raw} = 0.35A + 0.25\Gamma + 0.30H + 0.10V
$$

### Non-linear mapping
To constrain the output and improve interpretability,
a sigmoid function is applied:

$$
\mathrm{IIS} = \sigma(\mathrm{IIS}_{raw})
$$

where:

$$
\sigma(x) = \frac{1}{1 + e^{-x}}
$$

### Output
The resulting IIS value lies in the interval:

$$
\mathrm{IIS} \in (0, 1)
$$

The index represents a relative indicator of the aggregated
functional state and has no absolute or diagnostic meaning.

## Model description
The detailed mathematical formulation, parameter semantics,
and aggregation logic are described in:

- `docs/model.md`
- `formulas/core_model.tex`

## Inputs
Input parameters represent indirectly measurable aspects of system state.
All parameters are normalized to the range \([0, 1]\).

Parameter semantics, normalization logic, and assumptions
are described in `docs/model.md`.

## Output interpretation
The IIS output represents a relative indicator
of aggregated system state.

The index does **not** provide absolute measurements,
diagnoses, or predictive conclusions
and must be interpreted strictly within documented constraints.

## Assumptions
All core assumptions underlying the model are explicitly documented in:

- `docs/assumptions.md`

## Limitations
Known limitations, boundary conditions,
and non-applicable scenarios are described in:

- `docs/limitations.md`

## Ethical constraints
Ethical and usage constraints, including age-related
and contextual limitations, are described in:

- `docs/ethics.md`

## Project status
Current status: **Conceptual engineering model**

- No production code
- No empirical validation
- Focus on structure, reasoning, and transparency

## Contribution
Feedback on model structure, assumptions,
and documented limitations is welcome.

This project prioritizes critical review
over feature expansion or optimization.

## Author
Zixcidus

