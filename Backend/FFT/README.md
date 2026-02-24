# Backend/FFT

Fourier transform routines for 2D spectroscopy data processing.

## Functions

- `complexFFT_v2.m` — performs a complex Fourier transform along the coherence time axis of 2D spectroscopy data
- `real_FFT_v1.m` — performs a real-valued FFT; used when only the real part of the spectrum is needed
- `frobnormv2l.m` — Frobenius normalization variant used in the FFT pipeline; this is the **canonical** frobnorm implementation (also see `frobnorm_v2.m` in `Backend/Convenience/` for a related version)
