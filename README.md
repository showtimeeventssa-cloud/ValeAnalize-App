# ValeAnalize V3 — GP-50 Database Foundation

The approved ValeAnalize visual identity is preserved.

## V3 additions
- `data/gp50-database.json` — structured GP-50 V1.0.5 device/effect database foundation.
- GP-50 chain order and movable/fixed module rules.
- Effect model catalog across NR, PRE, DST, N→S, AMP, CAB, EQ, MOD, DLY and RVB.
- Amp and cabinet model catalog.
- Factory SnapTone names captured from the manual.
- MIDI CC map from the GP-50 MIDI Control Information List.
- First deterministic audio measurement layer: RMS, peak and zero-crossing rate.
- First deterministic candidate-ranking layer.
- V3 UI library cards and candidate-matcher status.

## Accuracy discipline
V3 does **not** claim that RMS/peak/ZCR alone can identify an exact studio tone. They are foundation measurements. The next DSP stage must add FFT/spectral profile, harmonic analysis, transient analysis, delay/reverb estimation and eventually calibration against the user's actual GP-50.

## Sources
The database was constructed from the Valeton GP-50 Firmware V1.0.5 manual/effect list and MIDI control list, with the official Valeton product page used for hardware capability verification.


## V3 DSP analysis
V3 adds a local browser DSP layer using Web Audio: FFT spectral averaging, spectral centroid/rolloff, spectral flatness, frame dynamics, crest factor, zero-crossing rate, transient flux, autocorrelation pitch estimation, envelope-repeat delay detection, and a conservative reverb/ambience estimate. The resulting fingerprint is mapped to the verified GP-50 database to generate a candidate amp/cab/effect profile. It remains a measurement/candidate stage, not a claim of recovering hidden original studio settings.
