# ValeAnalize V9 — GitHub Pages build

V9 is built directly from the V8 FIXED baseline. The existing DSP, GP-50 candidate engine, JSON export and Web MIDI functionality are preserved.

## V9 requested fixes
- Repaired the smudged/uneven chrome loop at the top of the guitar-pick artwork.
- Removed the duplicate `HEAR IT. ANALYSE IT. PLAY IT.` line from inside the large artwork because the same tagline already appears in the Home content.
- Embedded the cleaned V9 artwork directly into `index.html` so the deployed page does not depend on a separate artwork file for the main hero.
- Updated the service-worker cache name to V9 so an old V7/V8 cached page is not deliberately reused.

## GP-50 scope
The GP-50 MIDI screen remains intentionally conservative: it uses standard Web MIDI / Program Change support and does not invent undocumented SysEx parameter commands.

## Deploy
Upload the **contents** of `ValeAnalize_GitHub_V9` to the GitHub Pages repository, replacing the previous V8 files. If GitHub Pages is already configured, allow the deployment to finish before testing the URL.
