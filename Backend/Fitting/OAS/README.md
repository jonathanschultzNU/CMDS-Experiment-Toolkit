# Oscillation Associated Spectra (OAS)

This directory contains the implementation of the Oscillation-Associated Spectra (OAS) method. OAS analysis decomposes 2D spectroscopic data into frequency-resolved maps by fitting oscillatory components at each pixel, revealing how specific vibrational or electronic modes contribute across the 2D spectrum.

## Publication

> Schultz, J. *et al.* "Phonon-induced plasmon-exciton coupling changes probed via oscillation-associated spectra." *J. Chem. Phys.* (2019). https://doi.org/10.1063/1.5116836

## Files

- `OscillationAssociatedSpectrum.m` — main OAS computation function; orchestrates the full OAS pipeline for a given dataset
- `DataFittingScript_test.m` — **development artifact / internal test script; not intended for end-user use**
- `DetermineIndices.m` — determines the frequency and time indices relevant to the analysis window
- `PhaseMean.m` — computes the mean phase across ensemble or repetitions
- `ReferencePhase.m` — establishes a reference phase used to align oscillatory components
- `SingleFrequencyFT.m` — performs a single-frequency Fourier transform at a specified frequency
- `itcmp.m` — iterative component fitting routine; fits multiple oscillatory components simultaneously
- `itcmpEval.m` — evaluation function called during iterative fitting to assess residuals
- `itcmpFilterOscillations.m` — filters oscillatory components within the iterative fitting loop
- `itcmpParamConversion.m` — converts fitted parameters between internal units and physical units
- `svdecon.m` — SVD decomposition helper used to reduce dimensionality before fitting
