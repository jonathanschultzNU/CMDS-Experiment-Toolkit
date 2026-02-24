# CMDS-Experiment-Toolkit

CMDS-Experiment-Toolkit is a MATLAB software package for processing 1D and 2D spectroscopy data from [Phasetech QuickControl](https://phasetechspectroscopy.com/products/quickcontrol/) outputs.

## Prerequisites

- **MATLAB** — the main entry point (`AnalysisHub.mlx`) is a MATLAB Live Script (`.mlx` format)
- **Signal Processing Toolbox** — required for FFT and filtering operations used throughout the toolkit

## Setup

1. Add the `Backend/` folder tree to the MATLAB path (use *Set Path* or `addpath(genpath('Backend'))` from the repository root).
2. Open `AnalysisHub.mlx` in MATLAB.
3. Update the `data` and `dataworkup` directory paths near the top of `AnalysisHub.mlx` to match the locations on your local machine.

## Usage

`AnalysisHub.mlx` is organized into self-contained sections that can be run individually rather than executing the entire script from start to finish. The typical analysis workflow proceeds as follows:

1. **Loading** — reads Phasetech QuickControl output files into MATLAB structs via `MDSload`
2. **Signal Generation** — computes rephasing/non-rephasing and absorbance signals
3. **FFT** — applies complex or real FFT along the coherence time axis
4. **Plotting** — visualizes 2D spectra, frequency-domain maps, and beat signals
5. **Fitting** — population subtraction, LPSVD fitting, and oscillation-associated spectra (OAS) analysis

> **Checkpoints:** The toolkit includes checkpoint saves so that processed data can be reloaded in a later session without re-running expensive steps from scratch.

> **Memory:** Processing the full sample dataset requires approximately **2 GB** of memory.

## Directory Structure

```
CMDS-Experiment-Toolkit/
├── AnalysisHub.mlx              # Main analysis entry point (MATLAB Live Script)
├── CITATION.cff                 # Citation metadata
├── CHANGELOG.md                 # Version history
├── THIRD_PARTY_LICENSES.md      # Third-party attributions
└── Backend/
    ├── Convenience/             # General-purpose utility functions
    ├── FFT/                     # Fourier transform routines
    ├── Fitting/                 # Population fitting, LPSVD, and OAS analysis
    │   └── OAS/                 # Oscillation-Associated Spectra module
    ├── Inpaint_nans/            # Third-party NaN interpolation toolbox
    ├── Loading/                 # Data loading and parameter configuration
    ├── Plotting/                # 2D spectral plotting and visualization
    └── SignalGeneration/        # Signal computation routines
```

See the `README.md` in each `Backend/` subdirectory for per-function documentation.

## Associated Publication (OAS)

The oscillation-associated spectra (OAS) module is described in:

> Kirschner, M. S. *et al.* "Phonon-induced plasmon-exciton coupling changes probed via oscillation-associated spectra." *J. Chem. Phys.* (2019). https://doi.org/10.1063/1.5116836

## Citing This Work

If you use this toolkit, please cite it using the metadata in [`CITATION.cff`](CITATION.cff).
