# Satellite / terrestrial signal-quality display

**Status:** Historical operator-reported adjustment to Mars quality display. This is **not a calibrated RF measurement**.

Previous tests investigated `TunerManager.adjustSignalBySnr`, reporting a fix for the displayed quality scale after changes around Mars 3.5.0.

Illustrative operator-reported UI outputs included:

| Reception | Displayed signal (S) | Displayed quality (Q) |
| --- | ---: | ---: |
| DVB-S | 39 | 100 |
| DVB-T | 22–24 | 100 |

These are **on-screen application values from one reception setup**, not universally normalized percentages, field-strength dBµV values or proof that raw SNR equals 100. DVB-T2 figures were discussed in historical comparisons, but the exact measurement conditions and direct records have not been independently recovered here.

## What contributors should separate

1. Raw frontend lock, BER / MER / SNR and driver units.
2. Vendor HAL / tuner-manager conversion logic.
3. Display scale, clipping, rounding and range.
4. Identical signal source and tuning conditions before/after a build change.

No proprietary application or binary patch is being published.
