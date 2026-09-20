# ValeAnalize V7

Built from the working V6 baseline.

## V7
- Full, non-clipped guitar-pick logo in the top app header.
- Header is constrained so the logo/name cannot horizontally clip on narrow phones.
- Cleaned the three unwanted white/blue top-edge artifacts marked in the supplied Home screenshot.
- Cleaned artwork is embedded directly in `index.html`; no patched overlay logo.
- Real V6 DSP analysis retained.
- Added V7 GP-50 Calibration Lab: load an actual recording made through the GP-50 and compare it against the reference fingerprint.
- Calibration similarity uses the same measurable DSP features on both recordings.
- JSON preset export now includes calibration data when available.
- Existing GP-50 data foundation retained.

## Accuracy
The V7 calibration score is an empirical audio-profile similarity. It becomes more useful when the reference and GP-50 capture are made under controlled conditions (same guitar, pickup, playing, output/monitor path, level and section). It does not claim to recover unknown original studio settings.
