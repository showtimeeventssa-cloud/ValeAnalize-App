# ValeAnalize V10

ValeAnalize V10 is the clean V10 build for Valeton GP-50 tone matching.

## V10 fixes
- Repaired the main artwork top edge and removed the stray half-circle artifacts.
- Removed the duplicate HEAR IT. ANALYSE IT. PLAY IT. line from the artwork; the app keeps one clean tagline in the Home body.
- Rebuilt the header mark so it no longer uses the incomplete text-cropped icon.
- Reduced Home-page overscroll/blank-end behaviour and disabled vertical overscroll chaining.
- Removed duplicate Import markup and all web-citation text from the UI.
- Preserved the single-script architecture so raw JavaScript cannot leak onto the page.

## V10 tone-matching upgrade
- Higher frame count in High Accuracy mode.
- Multi-band spectral fingerprinting.
- Harmonicity and transient proxies.
- Empirical Reference vs GP-50 Capture calibration.
- Similarity score is shown only when a real GP-50 capture is supplied; V10 does not invent a confidence percentage from a single mastered song.
- GP-50 candidate generation remains conservative where exact Valeton model/parameter data has not been validated.

## Important accuracy note
A finished/mastered recording does not uniquely reveal the original guitar, amp, cabinet/IR, microphone, room, mix processing or GP-50 settings. The most reliable practical workflow is: analyse the reference -> build a candidate -> record the GP-50 candidate -> compare the two recordings -> adjust -> repeat.

## Deployment
Replace the GitHub Pages repository contents with this complete folder. Do not mix files from older ValeAnalize versions.
