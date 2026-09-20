# ValeAnalize V11 FIXED

This build fixes the previous V11 deployment faults:
- header mark is the clean pick/waveform mark, with no clipped ValeAnalize text inside it;
- main artwork is rebuilt with a clean top margin so the chrome loop is not cut at the image edge;
- iOS/Android PWA icons and Apple touch icon use the clean mark;
- Home page layout removes the artificial app-height/overscroll behaviour that created excess scrolling;
- Import accepts a broad set of audio extensions;
- browser-native decoding is attempted first; unsupported codecs fall back to FFmpeg.wasm;
- FFmpeg fallback uses @ffmpeg/core 0.12.6 with CORS-safe Blob URLs;
- service-worker cache is versioned as V11 FIXED so older V7/V8/V9/V10 assets are not reused.

The app cannot guarantee decoding DRM-protected or damaged files, but the decoder path is designed to handle common and legacy audio codecs including MP3, WAV/PCM, WMA, AAC/M4A, FLAC, AIFF, OGG/Opus and other FFmpeg-supported formats.
