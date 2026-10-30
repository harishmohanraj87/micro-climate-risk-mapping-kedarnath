# Evidence-based repository audit

**Audit basis:** repository contents and Git history available on 30 October 2026. Historical planning supplied separately is recorded below as unverified context; repository files are the basis for implementation claims.

## Inventory

| Required audit item | Evidence in current repository | Finding |
| --- | --- | --- |
| Datasets and dimensions | No data files or data directories | No observation count, locations, dates, sampling frequency, features, or missing-value information can be established. |
| Confirmed data sources | No source metadata, download records, citations, or data files | No external data source is confirmed as used. IMD, Sentinel-2, NASA Earthdata, Bhuvan/MOSDAC, and agricultural records are only proposed sources. |
| Features and target | No tables, code, or data dictionary populated with fields | No actual features or target variable exist. Rainfall, temperatures, humidity, NDVI, elevation, growth stage, and derived indicators are proposed candidates only. |
| Preprocessing | No executable scripts or notebooks | No missing-value handling, encoding, feature selection, or split procedure is implemented. |
| Models | No model code, environment, or run records | Decision Tree, Random Forest, XGBoost, TabPFN, and TabNet are not implemented, trained, or evaluated here. |
| Metrics and results | No results files, figures, tables, or model artefacts | No performance metrics or research findings are verifiable. |
| Plots, maps, outputs | No output directories or visual assets | No plots, maps, classifications, or reports exist. |
| Reproducible execution | No dependency manifest, configuration, or entry point | The project is not executable or reproducible from the current revision. |

## Historical plan compared with current implementation

| Historical planning detail | Repository-supported status |
| --- | --- |
| Kedarnath/Mandakini Valley, Rudraprayag | Proposed geographical focus; no stored study boundary. |
| Guptkashi, Ukhimath, Phata, Rampur, Narayankoti, Kalimath | Mentioned in planning; no data verifies these locations. |
| Rajma | Mentioned in planning; no crop or outcome data verifies it. |
| 216 observations (six villages × 36 months) | Not verified; no data supports this count. |
| Approximately 126 observations | Not verified; conflicts with the 216-observation planning figure and no data resolves the discrepancy. |
| IMD weather and Sentinel-2/NDVI | Proposed inputs; no files or provenance confirm use. |
| Five-class or three-class risk scale | Proposed alternatives; no target construction or classification scheme is implemented. |
| 80:20 train/test split, preprocessing, feature selection | Proposed workflow; no code demonstrates it. |
| Decision Tree, Random Forest, XGBoost, TabPFN, TabNet | Discussed candidate methods; none is implemented or evaluated. |

## Methodological requirements before empirical claims

1. Define whether the target is recorded crop loss, an observed risk assessment, a rule-based environmental label, or another proxy. A proxy must not be described as crop-loss ground truth.
2. Resolve the observation-count discrepancy from the actual dataset and document locations, dates, units, source, licence, and missingness.
3. Record the risk-class construction, thresholds, and whether inputs used to form the label are also included as features; otherwise target leakage is likely.
4. Use a validation plan that accounts for clustered villages and temporal dependence. A random 80:20 row split may overestimate generalisation for repeated village/month observations.
5. Fit all preprocessing and feature selection inside training partitions, preserve an untouched evaluation set where feasible, and report uncertainty alongside metrics.

## Files inspected

- `README.md` and its two preceding revisions in Git history.
- `LICENSE` and `.gitignore`.
- Documentation added in the preceding documentation update.

No Python, notebook, data, environment, reference, or result files exist in the audited tree.
