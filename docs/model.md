# IIS Core Model

## Scope
The IIS (Information and Measurement System) is an abstract engineering model
designed to aggregate heterogeneous, indirectly observable parameters
into a unified scalar index representing the **relative functional state**
of a system.

The model is conceptual and analytical in nature.
It does not aim to describe biological mechanisms directly
and does not provide medical or psychological conclusions.

## System abstraction
The modeled system is treated as a black box with observable proxies.
Internal biological, neurological, or psychological mechanisms
are not explicitly modeled.

The IIS operates exclusively on normalized input parameters
and does not physically interact with the modeled system.

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

All parameters are dimensionless and normalized
to the range \([0, 1]\).

## Normalization
Input parameters are normalized prior to aggregation.
Normalization logic is external to the IIS core model
and must be consistent across all inputs.

The IIS does not define measurement methods
and is limited strictly to aggregation logic.

## Aggregation
The core aggregation is defined as a weighted linear combination
of normalized parameters:

$$
\mathrm{IIS}_{raw} = w_1 A + w_2 \Gamma + w_3 H + w_4 V
$$

where weights reflect the relative contribution
of each parameter to the aggregated index.

## Non-linear mapping
To constrain the output range and ensure interpretability,
a sigmoid function is applied:

$$
\mathrm{IIS} = \sigma(\mathrm{IIS}_{raw})
$$

where:

$$
\sigma(x) = \frac{1}{1 + e^{-x}}
$$

## Output interpretation
The output value \(\mathrm{IIS} \in (0, 1)\) represents
a **relative index** of the aggregated functional state
of the modeled system.

The value has no absolute meaning
and must only be interpreted comparatively
within the documented assumptions and limitations.

## Model intent
The IIS model is intended as:

- an analytical aggregation framework,
- a conceptual layer for further system modeling,
- a demonstration of system-level reasoning under constraints.
