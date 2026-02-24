# Backend/Convenience

General-purpose utility functions used throughout the toolkit.

## Versioning Convention

Higher version numbers indicate more current implementations. Where both a versioned and an unversioned copy of a function exist, prefer the versioned one.

## Functions

- `MDSEASRead.m` — reads MDS/EAS data files into MATLAB structures
- `Probe_slice_normalization.m` — normalizes probe axis slices of 2D spectral data
- `buttonchoice.m` — UI button choice dialog helper for interactive scripts
- `findind.m` — find index utility (legacy version; prefer `findind_v2.m`)
- `findind_v2.m` — find index utility (current version)
- `findinds.m` — find multiple indices matching a set of values
- `frobnorm_v2.m` — Frobenius normalization utility; **note:** `frobnormv2l.m` in `Backend/FFT/` is the canonical version used in the FFT pipeline
- `getopts.m` — options parsing utility for handling function argument key/value pairs
- `pumpslices.m` — extracts pump frequency slices from 2D spectral data
- `savearray.m` — array save utility (legacy version; prefer `savearray_v2.m`)
- `savearray_v2.m` — array save utility (current version)
- `savestruct.m` — struct save utility (legacy version; prefer `savestruct_v2.m`)
- `savestruct_v2.m` — struct save utility (current version)
- `scanave_t2.m` — scan averaging over the t2 (waiting time) dimension
- `timeshift_v1.m` — shifts the time axis by a specified offset
- `trim2d.m` — trims a 2D array to a specified frequency or index range
- `unpackOAS.m` — unpacks OAS result structs into component arrays
- `unpackStruct.m` — generic utility to unpack fields of any struct into the caller workspace
