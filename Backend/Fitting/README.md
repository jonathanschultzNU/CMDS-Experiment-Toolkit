# Backend/Fitting

Functions for population dynamics fitting, LPSVD analysis, and oscillation-associated spectra. See the [`OAS/`](OAS/) subdirectory for the self-contained oscillation-associated spectra module.

## Functions

- `MDSDimRed.m` — dimensionality reduction for MDS data prior to fitting
- `OAS.m` — entry point for oscillation-associated spectra analysis (delegates to the `OAS/` subdirectory for full implementation)
- `casepoptsubt.m` — case-based population subtraction dispatcher
- `complexbeatproc.m` — complex beat signal processing for oscillatory components
- `cutresQB.m` — cuts residuals for quantum beat analysis
- `cuttimes.m` — trims data to a specified time range
- `lpsvd_range.m` — runs LPSVD fitting over a defined frequency or time range
- `lpsvd_runStruct.m` — runs LPSVD using a parameter struct for batch processing
- `lpsvd_zoom.m` — LPSVD fitting with zoom windowing for targeted frequency regions
- `lpsvdrun.m` — core LPSVD runner; called by the higher-level LPSVD wrappers
- `pop_fit_v2.m` — population dynamics fitting (current version)
- `popsubt_v1.m` — population subtraction (current version)
- `popsubtsigs_v1.m` — population subtraction applied to multiple signals simultaneously
- `subtlog.m` — logs subtraction operations for reproducibility
- `subtpred.m` — generates subtraction predictions for comparison with data

## Subdirectory

- [`OAS/`](OAS/) — self-contained module for oscillation-associated spectra analysis
