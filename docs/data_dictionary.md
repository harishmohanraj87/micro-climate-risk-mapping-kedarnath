# Data dictionary and provenance requirements

## Current inventory

No datasets or feature tables are committed to this repository. Consequently, no feature names, units, ranges, collection dates, target variable, geographic coordinates, or sample counts have been verified.

## Proposed source categories

The table records only source categories mentioned in historical project planning. It does not confirm access, suitability, licensing, or use in an analysis.

| Category | Potential examples named in project notes | Status | Required documentation before use |
| --- | --- | --- | --- |
| Meteorology | IMD; MOSDAC | Not present | Station/product identifier, variables and units, timestamps/time zone, quality flags, coverage, licence, access method |
| Optical satellite imagery | Sentinel-2; Landsat; MODIS | Not present | Collection/product/version, processing level, bands/index formula, cloud handling, acquisition dates, spatial resolution, licence |
| Terrain or contextual layers | Not specified | Not present | Provider, resolution, coordinate reference system, processing and licence |
| Agricultural observations | ICAR, State Agriculture Department, ground-truth records | Not present | Outcome definition, observation protocol, temporal/spatial support, permissions, privacy treatment, missingness |

## Unverified candidate variables

Historical planning mentioned rainfall, maximum and minimum temperature, humidity, NDVI, elevation, crop growth stage, and derived climate-risk indicators. No data file or code confirms that any of these variables exists or defines its units, calculation, coverage, or role. They must not be treated as the current project schema.

## Minimum schema for a future analysis table

Document each field using this template before committing a derived dataset or model input.

| Field | Description | Type and unit | Source/product version | Spatial support | Temporal support | Processing | Missing-data rule | Available at prediction time? |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `example_field` | Replace with a precise definition | Not yet defined | Not yet defined | Not yet defined | Not yet defined | Not yet defined | Not yet defined | Not yet defined |

The target must be marked separately and described as observed, derived, or proxy. A post-event assessment must not be used as an input feature or to construct features unavailable at the prediction horizon.
