# IIS Core Model

## Scope
The IIS (Information and Measurement System) is an abstract engineering model
designed to aggregate heterogeneous, indirectly observable parameters into
a unified scalar index representing the relative functional state of a system.

The model is conceptual and analytical in nature.
It does not aim to describe biological mechanisms directly
and does not provide medical or psychological conclusions.

## System abstraction
The modeled system is treated as a black box with observable proxies.
Internal biological, neurological, or psychological mechanisms
are not explicitly modeled.

The IIS operates exclusively on normalized input parameters
and does not interact with the system physically.

## Inputs
The base version of IIS operates on the following normalized parameters:

- **A** — activity-related parameter  
  Represents relative activity or engagement level.

- **Γ** — stress-related parameter  
  Represents relative stress or load intensity.

- **H** — stability parameter  
  Represents relative physiological or systemic stability.

- **V** — variability parameter  
  Represents variability or fluctuation in observed states.

All parameters are dimensionless and normalized to the range [0, 1].

## Normalization
Input parameters are normalized prior to aggregation.
Normalization logic is external to the IIS core model
and must be consistent across all inputs.

The IIS does not define measurement methods,
only the aggregation logic.

## Aggregation
The core aggregation is defined as a weighted linear combination
of normalized parameters:

IIS_raw = w₁·A + w₂·Γ + w₃·H + w₄·V

where weights reflect relative contribution of each parameter.

## Non-linear mapping
To constrain the output and ensure interpretability,
a sigmoid function is applied:

IIS = σ(IIS_raw)

where σ(x) = 1 / (1 + e^(-x))

## Output interpretation
The output value IIS ∈ (0, 1) represents a relative index
of the aggregated functional state of the system.

The value has no absolute meaning
and must only be interpreted comparatively
within the documented assumptions and limitations.

## Model intent
The IIS model is intended as:
- an analytical aggregation framework,
- a conceptual layer for further system modeling,
- a demonstration of system-level reasoning under constraints.
