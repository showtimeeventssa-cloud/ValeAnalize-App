# ValeAnalize V17 — Real GP-50 PRST Engine

This build retains the V16 audio-analysis/guitar workflow and adds a real GP-50 preset-file engine.

## Real GP-50 preset support
- Accepts/exports the GP-50 552-byte `.prst` container.
- Validates the GP-50 header.
- Validates and recalculates CRC-8/0x07 over bytes `0x15:` with the CRC stored at `0x14`.
- Reads/writes the 16-byte patch name at `0x19:0x29`.
- Reads/writes the 10 model records.
- Reads/writes the bypass bitmask.
- Reads/writes the 10-byte chain-order record.
- Reads/writes all 80 float32 parameter slots (10 blocks × 8).
- Reads/writes the GP-50 footswitch mask record.
- Includes the user-supplied real COUNTRY'26 `.prst` as a verified template.

## Important accuracy rule
The automatic tone matcher can generate a binary-valid GP-50 patch from a real template, but it does not claim that a mastered song uniquely reveals the original studio preset. For exact model selection and model-specific parameter names, import a real `.prst` from the GP-50/Valeton software; the editor preserves the real model IDs and exposes every stored parameter slot.

The official GP-50 supports 100 patch slots, 9 simultaneous modules, third-party IR storage and SnapTone/NAM storage, plus 2-in/2-out USB audio and USB MIDI. The official firmware/manual/software references should remain the authority for device behavior.

The GP-50 binary format implementation was cross-checked against the supplied real patch and independent reverse-engineering documentation. The independent documentation describes the 552-byte format, fixed model records, bypass record, chain-order record, 80 float parameters and CRC behavior.
