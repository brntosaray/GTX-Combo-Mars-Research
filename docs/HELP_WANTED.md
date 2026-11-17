# Open questions for GTMedia / Android / DVB developers

This is a request for **source-level review and maintainable fixes**, not an official device-support claim.

1. **Terrestrial chain:** Can a contributor identify the exact GTX Combo DVB-T/T2 demod/tuner configuration from matching build logs and board identifiers, without relying on driver names alone?
2. **Mars OTA regressions:** Which FE module, DVB config and device-tree changes differ between the 2026-09-17 working reference and 2026-10-13 Mars 3.5.0? How can they be validated without publishing vendor binary firmware?
3. **Android keylayout:** Which scan-code definition or Android input-device selection behavior caused fallback from the `Vendor_0508_Product_0110.kl` device mapping? Is there a clean source-level/regression-test fix?
4. **IR F1:** Which source/device-tree mapping ensures the receiver selects the correct IR key table at boot, avoiding binary boot-area changes?
5. **Signal display:** What conversion units and clipping rules should the tuner-manager layer use to show meaningful SNR-derived quality?
6. **Shutdown:** Which logs distinguish a delayed Android shutdown from vendor standby/fan/LED control without manipulating hardware?

We welcome code reviews, reproducible procedures, source patches, sanitized logs and specific requests for missing evidence. State device model and build, and distinguish GT Combo from GTX Combo.

[CoreELEC DVB findings](https://github.com/brntosaray/GTX-Combo-CoreELEC-Research) and [OpenATV research](https://github.com/brntosaray/GTX-Combo-OpenATV-Research) belong to distinct projects.
