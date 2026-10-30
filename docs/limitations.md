# Limitations and threats to validity

## Present limitation

No empirical work is available in the repository. There is no basis here for claims about risk patterns, prediction accuracy, lead time, or agricultural benefit.

## Data and measurement

- The proposed agricultural outcome has not been defined or supplied. A vegetation index, weather event, or administrative report may be a proxy rather than direct evidence of crop loss.
- Station coverage, satellite revisit intervals, cloud contamination, terrain shadow, missing records, and differing spatial resolutions can introduce measurement error and scale mismatch.
- Source licences, access conditions, versions, and preprocessing history are unrecorded; these must be verified before reuse.

## Design and modelling

- Nearby locations and adjacent times can be correlated. Random row-level splits can leak information and overestimate generalisation.
- Small samples, rare events, or unbalanced classes can make flexible models unstable and reported metrics misleading.
- Selection of features or hyperparameters using test information, including preprocessing outside a training fold, would invalidate evaluation.
- Predictions based on observational data should not be interpreted as causal effects of weather, elevation, or interventions.
- Performance in one period or geographic area may not transfer to other seasons, elevations, crops, or valleys.

## Interpretation and use

Any future risk surface should state its target, period, resolution, uncertainty, coverage, and decision limits. It should complement—not replace—local agronomic expertise, field observation, and official warnings. Sensitive household, farm, or location information requires appropriate permissions and aggregation practices before publication.
