# Mapping Windows of Vulnerability: Micro-Climate Risk Mapping for Himalayan Agriculture

## Research status

**Planning and documentation stage.** This revision contains no datasets, source code, notebooks, trained models, generated maps, or validated experimental results. It describes a proposed research direction for the Kedarnath/Mandakini Valley area of Uttarakhand, India; it does not establish predictive performance or agricultural outcomes.

## Contents

- [Overview](#overview)
- [Evidence inventory](#evidence-inventory)
- [Research questions and objectives](#research-questions-and-objectives)
- [Study area](#study-area)
- [Proposed data and provenance](#proposed-data-and-provenance)
- [Proposed methodology](#proposed-methodology)
- [Experimental design and evaluation](#experimental-design-and-evaluation)
- [Current evidence and results](#current-evidence-and-results)
- [Reproducibility](#reproducibility)
- [Repository structure](#repository-structure)
- [Limitations](#limitations)

## Overview

Mountain agriculture can be exposed to highly local variation in temperature, precipitation, terrain, and vegetation conditions. This proposed TBI Summer Research Internship project would develop a transparent workflow for combining meteorological, satellite-derived, terrain, and—if available—agricultural impact data to explore micro-climate-related agricultural risk in the Kedarnath/Mandakini Valley region.

The intended output is a research workflow and, only after suitable data and validation are available, spatial risk indicators or maps. Any future map should be interpreted as an association-based decision-support product, not as evidence of causal effects or a guarantee of crop-loss prediction.

### Abstract

This repository records the planned documentation and reproducibility framework for a micro-climate risk-mapping study in Himalayan agriculture. The proposed study would integrate documented meteorological observations, satellite-derived vegetation indicators, terrain information, and appropriately sourced agricultural outcome data. It has not yet implemented data acquisition, preprocessing, modelling, mapping, or validation. The project therefore makes no claims about model accuracy, risk estimates, or real-world agricultural impacts.

## Evidence inventory

The [repository audit](docs/repository_audit.md) is the authoritative inventory of what is currently present. It confirms that there are no data files, scripts, notebooks, dependency manifests, trained models, metrics, plots, or maps to inspect. Historical planning has mentioned six villages, Rajma, 216 or approximately 126 observations, IMD/Sentinel-2 data, a five-class risk scale, and several machine-learning models; these are unverified planning details, not established implementation facts.

## Research questions and objectives

### Questions

1. Which documented meteorological, satellite, and terrain variables are associated with an explicitly defined agricultural risk outcome?
2. If an outcome and sufficient historical data become available, can models estimate risk at a useful spatial and temporal resolution without invalid spatial or temporal leakage?
3. How do modelled risk indicators vary across documented elevation and terrain strata in the study area?

### Objectives

- Define the outcome, study boundary, spatial unit, and temporal unit before analysis.
- Build a provenance-preserving dataset from licensed or permitted sources.
- Evaluate baseline and candidate models using splits that respect spatial and temporal dependence.
- Communicate uncertainty, limitations, and intended uses of any derived maps.

## Study area

The proposed focus is the Kedarnath/Mandakini Valley area within Rudraprayag district, Uttarakhand, India. Historical planning named Guptkashi, Ukhimath, Phata, Rampur, Narayankoti, and Kalimath, but no dataset or spatial boundary in this repository verifies their inclusion. Likewise, Rajma has been identified in planning but is not supported by a current data dictionary or analysis artifact. A study polygon, coordinate reference system, elevation range, agricultural calendar, and observation period must be recorded with the data release and analysis configuration before results can be reproduced.

## Proposed data and provenance

Historical project planning identifies IMD, NASA Earthdata products (including MODIS and Landsat), Copernicus Sentinel-2, ISRO Bhuvan/MOSDAC, and agriculture or ground-observation records from relevant authorities as possible sources. They are not downloaded or verified inputs.

No source files, licences, retrieval dates, product versions, spatial coverage, or access permissions are stored here. See [the data dictionary](docs/data_dictionary.md) for the information that must be supplied before a dataset is used.

## Proposed methodology

The planned workflow is documented in [docs/methodology.md](docs/methodology.md): define the risk target and analysis unit; acquire provenance-rich data; align features and targets without future information; perform split-safe preparation; evaluate suitable models with spatial and/or temporal holdouts; and map only defined, validated outputs.

Decision Tree, Random Forest, XGBoost, and TabPFN have been mentioned as possible candidate methods. None is implemented or evaluated in this repository. Their suitability depends on the eventual sample size, feature types, target definition, validation design, and compute environment.

## Experimental design and evaluation

No experiment configuration or metrics currently exist. The target must determine the task type and metrics. Accuracy alone is inadequate for imbalanced classification; prevalence-aware metrics, calibration, uncertainty, and confusion matrices should be considered where applicable.

Preprocessing transformations, imputation, feature selection, and hyperparameter tuning must be fit using training partitions only. Random row-level splits may overstate performance when records are spatially or temporally correlated. The validation protocol, random seeds, software versions, and selected metrics should be committed alongside future experiments.

## Current evidence and results

There are **no results to report**. The repository has no input data, executable analysis, trained-model artefacts, figures, maps, tables, or evaluation outputs. Claims about variable importance, crop-loss prediction, forecast lead time, or model performance would be unsupported at this stage.

## Reproducibility

An end-to-end execution path cannot yet be provided because there is no code, dependency manifest, configuration, or accessible data. [docs/reproducibility.md](docs/reproducibility.md) records the required additions and intended execution order. Do not treat the repository as runnable until those materials are added and tested.

## Repository structure

```text
.
├── README.md
├── LICENSE
├── CONTRIBUTING.md
└── docs/
    ├── data_dictionary.md
    ├── limitations.md
    ├── methodology.md
    └── reproducibility.md
```

Directories such as `data/`, `src/`, `notebooks/`, and `results/` are not present in the current revision and should be introduced only with documented content.

## Limitations

The principal current limitation is absence of implementation and evidence. A future study will also need to address outcome validity, limited samples, missing or uneven observations, spatial and temporal dependence, class imbalance, satellite cloud contamination, scale mismatch, and transferability. See [docs/limitations.md](docs/limitations.md).

## Contributing and license

Contributions should follow [CONTRIBUTING.md](CONTRIBUTING.md), particularly its requirements for provenance and reproducibility. This repository is licensed under the [MIT License](LICENSE). Licences and terms for external datasets and software remain the responsibility of their respective providers and must be checked before use.

## Contact

The repository history and existing README identify Harish Mohanraj and Shivang Negi. No institutional affiliation, project contact channel, funding source, or publication status is documented in this repository.
