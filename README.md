# ValeAnalize V6

V6 is built directly from the approved V5 interface.

## V6 changes
- Real browser-side audio decoding using Web Audio API.
- FFT-based spectral analysis.
- Spectral centroid and 85% rolloff.
- RMS, crest factor and dynamic-range estimate.
- Spectral flatness and zero-crossing rate.
- Basic monophonic pitch estimation by autocorrelation.
- Low/mid/high spectral energy balance.
- Deterministic GP-50 candidate generation from the measured fingerprint.
- Model-based Match Score.
- JSON export containing the measured fingerprint and generated candidate.
- Existing approved visual artwork, embedded logo and scrolling Home screen are preserved.

## Important accuracy note
The V6 Match Score is a model-based score derived from the reference recording and the generated candidate profile. It is not yet calibrated by recording the same reference through a real GP-50 and comparing the two recordings. V7 can use that calibration loop to make the score materially more meaningful.

The app does not claim to recover unknown original studio settings from a mastered commercial recording.

## GP-50 reference
The GP-50 structure and capabilities are based on Valeton's official product information and V1.0.5 manual.
