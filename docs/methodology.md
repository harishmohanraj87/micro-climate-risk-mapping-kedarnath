# Proposed methodology

## Scope and status

This is a proposed protocol, not a record of performed analysis. The repository contains no implementation, data, or experiment outputs at the time of writing.

## 1. Define the estimand before acquiring features

Document the agricultural outcome or risk proxy, its observation method, observation time, spatial unit, and eligible population. A satellite index or weather anomaly is a feature or proxy, not automatically an observed crop-loss outcome. Define the prediction horizon so that each feature precedes the target observation.

## 2. Record data provenance

For each source, record provider, product and version, access URL or request process, licence/terms, retrieval date, coverage, spatial and temporal resolution, transformations, and any access restrictions. Retain immutable source identifiers where permitted. Do not commit confidential records or credentials.

## 3. Harmonise the analysis dataset

Select and document a coordinate reference system, spatial support, and temporal aggregation period. Align each feature to the target observation window. Record missingness, quality flags, cloud masking, and resampling choices. Maintain a data dictionary for every derived field.

## 4. Develop without leakage

Partition data by time and/or geography before fitting imputation, scaling, feature selection, target encoding, or hyperparameter selection. A random row split is generally inappropriate when adjacent places or periods share conditions. Use a final held-out spatial or temporal block where data volume permits.

## 5. Compare models fairly

Start with an interpretable baseline appropriate to the target. Candidate tree-based methods—Decision Tree, Random Forest, XGBoost, and TabPFN—should be considered only after documenting the sample size, inputs, tuning budget, and compatible software version. Apply the same folds, target definition, and feature-availability rules to every candidate.

## 6. Evaluate and communicate uncertainty

Pre-specify primary metrics before model selection. For classification, report class prevalence, a confusion matrix, precision/recall or related threshold-dependent measures, discrimination, calibration, and uncertainty where feasible. For regression, report errors, residual diagnostics, and uncertainty where feasible. Stratify evaluation only when sample counts support it.

## 7. Map responsibly

Map only the defined model output, at the analysis resolution and time period. Include a legend, coordinate system, prediction period, data coverage, uncertainty or applicability information, and a statement that modelled associations do not prove causation.

## Required future artefacts

- A source-data inventory and access instructions.
- Versioned scripts or notebooks with an explicit entry point.
- A dependency manifest and pinned environment.
- Configuration for paths, dates, spatial units, target, features, seeds, and splits.
- A results report generated from recorded runs.
