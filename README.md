# ValeAnalize

**HEAR IT. ANALYSE IT. PLAY IT.**

A free GitHub-ready PWA concept for analysing a guitar reference and building a Valeton GP-50 preset.

## Included
- `index.html` — main app; the primary ValeAnalize logo is embedded directly as a data-URI SVG so it renders immediately without waiting for an image file.
- `manifest.webmanifest` — PWA metadata for installable home-screen use.
- `sw.js` — basic offline cache.
- `icons/` — launcher/home-screen artwork.

## Visual identity
Dark cinematic black/blue interface, chrome guitar-pick + waveform mark, cyan/blue highlights, and the ValeAnalize wordmark.

## GP-50 accuracy note
The UI is designed around the documented GP-50 capabilities. A true tone-matching engine still needs the actual DSP/audio-analysis layer and a validated GP-50 parameter/effect database. The current interface is deliberately honest: the displayed match is a prototype estimate, not a claim that a finished song can reveal the original studio settings exactly.

Valeton's GP-50 documentation states that the unit supports 100 patch slots, 55 factory patches, over 100 effects, up to 9 simultaneous modules, IR loading, NAM loading, USB audio and USB MIDI, plus iOS/Android editing. See the official Valeton GP-50 documentation before implementing direct preset transmission.
