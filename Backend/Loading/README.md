# Backend/Loading

Functions for loading and configuring Phasetech QuickControl data.

> **Note:** The `data` and `dataworkup` directory paths in `AnalysisHub.mlx` must be updated to match the locations on your local machine before use.

## Functions

- `MDSload.m` — main data loading function; reads Phasetech QuickControl output files and organizes the results into MATLAB structs for downstream processing
- `mdsparams.m` — defines and returns parameter structs that configure the MDS data loading process (scan parameters, frequency axes, etc.)
