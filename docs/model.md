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

## Model pipeline overview (conceptual)

```text
+-----------------------------+
|   Indirect observations    |
|   (external to IIS scope)  |
+-----------------------------+
              |
              v
+-----------------------------+
|   Normalization layer      |
|   (external logic)         |
|   Map inputs to [0, 1]     |
+-----------------------------+
              |
              v
+-----------------------------+
|   Normalized parameters    |
|   A, Γ, H, V ∈ [0, 1]      |
+-----------------------------+
              |
              v
+-----------------------------+
|   Linear aggregation       |
|   IIS_raw = Σ w_i · x_i    |
+-----------------------------+
              |
              v
+-----------------------------+
|   Sigmoid mapping          |
|   IIS = σ(IIS_raw)         |
+-----------------------------+
              |
              v
+-----------------------------+
|   Output index             |
|   IIS ∈ (0, 1)             |
|   Relative indicator       |
+-----------------------------+
```
The diagram illustrates the conceptual processing pipeline.
Measurement methods, data acquisition, and normalization logic
are explicitly outside the IIS core scope.

## Inputs

The base version of IIS operates on the following normalized parameters:

A — activity-related parameter
Represents relative activity or engagement level.

Γ — stress-related parameter
Represents relative stress or load intensity.

H — stability parameter
Represents relative physiological or systemic stability.

V — variability parameter
Represents variability or fluctuation in observed states.

All parameters are dimensionless and normalized
to the range 
[0,1]
[0,1].

## Normalization

Input parameters are normalized prior to aggregation.
Normalization logic is external to the IIS core model
and must be consistent across all inputs.

The IIS does not define measurement methods
and is limited strictly to aggregation logic.

## Aggregation

The core aggregation is defined as a weighted linear combination
of normalized parameters:

IISraw=w1A+w2Γ+w3H+w4V
IIS
raw
	​

=w
1
	​

A+w
2
	​

Γ+w
3
	​

H+w
4
	​

V

where weights reflect the relative contribution
of each parameter to the aggregated index.

## Non-linear mapping

To constrain the output range and ensure interpretability,
a sigmoid function is applied:

IIS=σ(IISraw)
IIS=σ(IIS
raw
	​

)

where:

σ(x)=11+e−x
σ(x)=
1+e
−x
1
	​

## Output interpretation

The output value 
IIS∈(0,1)
IIS∈(0,1) represents
a relative index of the aggregated functional state
of the modeled system.

The value has no absolute meaning
and must only be interpreted comparatively
within the documented assumptions and limitations.

## Model intent

The IIS model is intended as:

an analytical aggregation framework,

a conceptual layer for further system modeling,

a demonstration of system-level reasoning under constraints.
