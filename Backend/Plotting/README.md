# Backend/Plotting

Functions for visualizing 2D spectral data, frequency maps, beat signals, and related diagnostics.

## Core 2D Plotting

- `MDplot.m` — basic 2D spectral plot (legacy version; prefer `MDplot_v2.m`)
- `MDplot_v2.m` — 2D spectral plot with improved display options (current version)
- `MDplotmv.m` — multi-view 2D spectral plot for comparing multiple spectra side-by-side
- `MDfreqplot.m` — frequency-domain 2D plot
- `plot2Dt.m` — 2D plot in the time domain
- `plot2Dw.m` — 2D plot in the frequency domain; the most feature-rich 2D plotting function

## Beat / Oscillation Visualization

- `beatcontours_exp.m` — plots beat signal contours extracted from experimental data
- `qbexam.m` — quantum beat examination plot for inspecting oscillatory residuals

## Normalization

- `norm2DES.m` — normalizes 2DES spectra for display
- `norm2DESfreq.m` — normalizes 2DES spectra in the frequency domain
- `normdim.m` — normalizes an array along a specified dimension

## Smoothing

- `smooth_2D_v3.m` — 2D smoothing (legacy version; prefer `smooth_2D_v4.m`)
- `smooth_2D_v4.m` — 2D smoothing (current version)
- `smoothcase.m` — case-based smoothing dispatcher for time-domain data
- `smoothfreqcase.m` — frequency-domain smoothing dispatcher (legacy version; prefer `smoothfreqcase_v2.m`)
- `smoothfreqcase_v2.m` — frequency-domain smoothing dispatcher (current version)

## Utilities

- `NanReplace.m` — replaces NaN values with a fill value to avoid display artifacts
- `ButtonDownFcn2DES_live.m` — interactive mouse click callback for live 2DES plots in `AnalysisHub.mlx`
- `mouseMove.m` — mouse movement callback used in interactive spectral plots
- `cmap2d.m` — 2D colormap utility for diverging spectral color scales
- `plot_areaerrorbar.m` — plots area-style shaded error bars around a trace
- `progressbar.m` — progress bar display utility for long-running loops
- `genericplot.m` — minimal generic plot wrapper for quick visualization
