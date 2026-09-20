# ValeAnalize V13 — Working Audio Analysis Build

V13 is a functional cumulative build from V12 focused on the workflow that was missing: **import → decode → analyse → build GP-50 candidate → test on pedal → capture → calibrate**.

## What changed
- Importing a track now immediately moves to Analyse and starts the analysis.
- Analysis is asynchronous/chunked so the UI stays responsive on phones/tablets instead of appearing frozen.
- Native browser decoding is attempted first; unsupported codecs use the FFmpeg WASM fallback.
- Added **My Guitar** profile: type, brand/model, pickups, pickup position, tuning, strings, scale and output level. The profile is saved locally and is used when building the candidate.
- Candidate presets now show a concrete starting amp, cab, drive strategy, gain, bass/mid/treble/presence, gate and 5-band guitar EQ starting points.
- The generated preset is explicitly a starting point; real GP-50 capture/calibration is used for refinement.
- Version/cache bumped to V13.

## Important accuracy note
A mastered full song does not uniquely reveal the original guitar, amp, cab, mic, processing or studio preset. V13 therefore does not invent an exact studio preset. It extracts measurable features and builds a GP-50 candidate, then uses a real GP-50 recording for empirical correction.

The GP-50 officially supports over 100 effects, up to 9 modules, 20 user IRs, up to 80 NAM/SnapTone slots, 2-in/2-out USB audio and USB MIDI.

## Test workflow
1. Open the app.
2. Go to **Import**.
3. Set **My Guitar** to the actual guitar/pickups/position.
4. Choose Full Song, Guitar Track, or Custom Section.
5. Pick the audio file. V13 automatically starts analysis.
6. When complete, open **GP-50 Presets**.
7. Set the suggested starting patch on the physical GP-50.
8. Record the GP-50 output and load that capture under **Real GP-50 Calibration**.
9. Use the measured differences to refine the patch.

Do not mix V12/V11 files into this build. Replace the GitHub repository with the complete V13 package.


V14 logo-safe rebuild: main artwork has a generous safe-area around the chrome loop; header mark and every PWA icon use the same padded clean mark. The app never relies on object-fit:cover for the logo artwork.

## Standard guitar presets added
The My Guitar profile now includes standard selectable presets for:
- Squier by Fender Debut
- Ibanez Acoustic
- Sigma Acoustic
- Ditson Acoustic

The acoustic entries are intentionally generic because pickup/preamp specifications vary by exact model. They can be adjusted after selection. The Squier Debut profile is set as an SSS passive electric profile; Fender's official Debut specifications list three ceramic single-coil pickups and a 5-position switch.

## Standard guitar presets added
The My Guitar profile now includes standard selectable presets for:
- Squier by Fender Debut
- Ibanez Acoustic
- Sigma Acoustic
- Ditson Acoustic

The acoustic entries are intentionally generic because pickup/preamp specifications vary by exact model. They can be adjusted after selection. The Squier Debut profile is set as an SSS passive electric profile; Fender's official Debut specifications list three ceramic single-coil pickups and a 5-position switch.


## V15 ALL FIXES
- Standard My Guitar presets: Squier by Fender Debut (Stratocaster), Ibanez Acoustic, Sigma Acoustic, Ditson Acoustic.
- Removed the duplicate audio-file change handler that could start two analysis flows and overwrite the UI state.
- Import now runs one automatic analysis flow and opens the generated GP-50 candidate after completion.
- Analysis is guarded against concurrent runs and uses the selected guitar profile.
- Saved guitar profiles restore the selected preset as well as the editable parameters.
- Logo-safe V14 artwork/icons are preserved.
- GP-50 database metadata updated to V15.
- GP-50 facts are based on Valeton documentation; exact original studio settings are not claimed recoverable from a mastered song.
