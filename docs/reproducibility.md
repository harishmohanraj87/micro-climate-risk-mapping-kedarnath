# Reproducibility guide

## Current status

The repository does not currently provide runnable software, an environment file, configuration, data-access procedure, or expected outputs. It is therefore not possible to reproduce an analysis from this revision, and no installation command is asserted here.

## Required execution contract for future work

Before describing the project as reproducible, add and verify:

1. A dependency manifest with exact or constrained versions and a supported runtime version.
2. An entry point for acquisition (where permitted), preparation, training, evaluation, and map/report generation.
3. A non-secret configuration defining data locations, study boundary, dates, features, target, split strategy, hyperparameters, output path, and seed.
4. Data-access instructions identifying manual downloads, credentials, restricted data, licences, and checksums where practical.
5. A deterministic small public or synthetic smoke-test fixture when full data cannot be redistributed.
6. A run manifest recording code revision, dependency versions, input versions, configuration, seed, and output locations.

## Intended order of execution

This template cannot be run until scripts exist:

1. Obtain permitted source data and record provenance.
2. Validate source files and prepare an analysis-ready dataset.
3. Create spatial/temporal training, validation, and test partitions.
4. Fit preprocessing and models using training data only.
5. Evaluate on untouched holdouts and save metrics plus diagnostics.
6. Generate maps and reports from the recorded configuration.

## Seeds and determinism

No seeds are presently defined. Future stochastic steps should accept an explicit seed and log it. Exact reproducibility can vary across operating systems, hardware, libraries, and accelerator implementations; record these details for each reported result.
