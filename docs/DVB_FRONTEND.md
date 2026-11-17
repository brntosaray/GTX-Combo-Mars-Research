# DVB-S/S2 and DVB-T/T2 on Android Mars

**Status:** Historical operator-reported recovery experiments; reproduction and raw assets are not included in this public repository.

## Background

The GTX Combo combines satellite and terrestrial reception on a vendor Android Mars system. The operator's investigations involved `gtm_hardware_fe.ko`, `aml_hardware_dmx.ko`, `cfg_dvb.ini` and device-tree settings. These components form a matched device-specific system, **not** interchangeable isolated files.

## Reported observations

- A previously working Mars build dated 2026-09-17 was used as a satellite and terrestrial reference.
- The operator reported restoring DVB-T/T2 operation and preserving DVB-S/S2 operation during experiments; details of the exact successful driver/config/DTBO combination need original logs and file validation before being called a reproducible public fix.
- Mars 3.5.0 (2026-10-13) initially disrupted some channel and terrestrial behavior and replaced frontend-related assets; some remote mapping also regressed.
- Historic logs referenced Sony `CXD28xx`-family terrestrial behavior. A driver log string is **not** sufficient proof of the exact physically populated demodulator or tuner without board/driver confirmation.
- Satellite reception preservation is a strict baseline: experiments on terrestrial support must not silently remove, unload or replace a proven satellite FE.

## Technical questions for contributors

1. Which Mars FE / demux / configuration revisions match each firmware release?
2. How can the precise terrestrial frontend chain and bus connections be independently proven from sanitized kernel logs and board evidence?
3. Which change actually restored DVB-T/T2 across the relevant Mars releases, and why?
4. Can a maintainable source-level fix be proposed without distributing vendor-controlled binary modules?

## Boundaries

No executable `insmod`, `rmmod`, firmware patch, DTB change or flash recipe is provided here. **Do not use another device's driver binaries** based on this report. Verify exact build compatibility and preserve working satellite functionality.
