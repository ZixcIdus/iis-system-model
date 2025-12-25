# Assumptions

This document describes the core assumptions underlying the IIS model.
All assumptions are explicit and intentional.

## System abstraction
- The modeled system is treated as a black box.
- Internal biological, neurological, or psychological mechanisms
  are not explicitly represented.
- Only indirect observable proxies are considered.

## Input parameters
- Input parameters are assumed to be measurable indirectly.
- Parameters represent relative, not absolute, quantities.
- Inputs are assumed to be dimensionless after normalization.

## Normalization
- All input parameters are normalized to the range [0, 1].
- Normalization logic is external to the IIS core model.
- Consistent normalization across parameters is assumed.

## Aggregation logic
- Linear weighted aggregation is assumed sufficient
  for base-level system state approximation.
- Parameter weights are heuristic and not empirically optimized.
- No automatic weight adaptation is performed.

## Interpretation
- IIS output values are assumed to be meaningful only
  in a comparative or exploratory context.
- Absolute interpretation of the index is explicitly excluded.

## Model scope
- The base model assumes a static snapshot of system state.
- Temporal behavior is intentionally excluded
  to preserve interpretability and control.
