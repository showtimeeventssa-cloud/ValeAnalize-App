# ValeAnalize V2 — GP-50 Database Foundation

The approved ValeAnalize visual identity is preserved.

## V2 additions
- `data/gp50-database.json` — structured GP-50 V1.0.5 device/effect database foundation.
- GP-50 chain order and movable/fixed module rules.
- Effect model catalog across NR, PRE, DST, N→S, AMP, CAB, EQ, MOD, DLY and RVB.
- Amp and cabinet model catalog.
- Factory SnapTone names captured from the manual.
- MIDI CC map from the GP-50 MIDI Control Information List.
- First deterministic audio measurement layer: RMS, peak and zero-crossing rate.
- First deterministic candidate-ranking layer.
- V2 UI library cards and candidate-matcher status.

## Accuracy discipline
V2 does **not** claim that RMS/peak/ZCR alone can identify an exact studio tone. They are foundation measurements. The next DSP stage must add FFT/spectral profile, harmonic analysis, transient analysis, delay/reverb estimation and eventually calibration against the user's actual GP-50.

## Sources
The database was constructed from the Valeton GP-50 Firmware V1.0.5 manual/effect list and MIDI control list, with the official Valeton product page used for hardware capability verification.
