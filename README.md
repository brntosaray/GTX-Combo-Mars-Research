# GTMedia GTX Combo — Mars (Android 9) Community Research

**Community:** [Discussions](https://github.com/brntosaray/GTX-Combo-Mars-Research/discussions) · [Welcome topic (ready to publish)](docs/COMMUNITY_WELCOME.md) · [Issues](https://github.com/brntosaray/GTX-Combo-Mars-Research/issues)


**Independent community documentation • GTMedia GTX Combo • Amlogic S905X3 • Android 9 / Mars firmware**

> **Status as of 17 November 2026:** Historical operator-reported fixes exist for DVB-T/T2 reception, Bluetooth/IR remote input and reported signal-quality display. Power-management issues remain unresolved. This project is **not an official GTMedia release**, an OTA package, or a universal repair kit.

## Purpose

Share technical observations from work on the **GTMedia GTX Combo** and make firmware regressions, known-good configuration identifiers, remote mappings and reproducible bug reports easier to review. **GT Combo and GTX Combo must not be assumed hardware/firmware equivalent.**

This public repository is **strictly separate** from the operator's private engineering workspace. It also deliberately does not combine Android Mars fixes with the separate [CoreELEC](https://github.com/brntosaray/GTX-Combo-CoreELEC-Research) and [OpenATV/Enigma2](https://github.com/brntosaray/GTX-Combo-OpenATV-Research) research.

## Snapshot

| Area | Observed or previously reported outcome | Status |
| --- | --- | --- |
| DVB-S/S2 | Working satellite baseline was preserved during Android FE investigation | Historical operator report |
| DVB-T/T2 | Earlier module/configuration tests recovered terrestrial functionality; OTA 3.5.0 caused regressions needing investigation | Historical operator report |
| Bluetooth remote | Corrected duplicate scan-code entries in device-specific keylayout; color keys restored | Historical operator report |
| IR F1 | Analyzed IR key code and repaired device-tree mapping for the top TV V+ / F1 button | Historical operator report |
| Quality indicator | Reported correction to signal quality display / SNR scaling in Mars 3.5.0 | Historical operator report |
| Power off | Delayed shutdown, fan and front-panel indicators observed | **Open / not fully resolved** |
| Other versions / boards | Compatibility not established | **Not verified** |

See [firmware and version notes](docs/FIRMWARE_BASELINES.md), [DVB findings](docs/DVB_FRONTEND.md), [Bluetooth remote](docs/BLUETOOTH_REMOTE.md), [IR F1](docs/IR_F1_REMOTE.md), [signal indicator](docs/SIGNAL_QUALITY.md), [power management](docs/POWER_MANAGEMENT.md), and [help wanted](docs/HELP_WANTED.md).

## Evidence levels

This public upload is based on **earlier operator-provided conversations and a private project index**, not a newly connected receiver, a complete raw-log archive or a fresh firmware binary comparison. Dates and hashes are reproduced as reported and must be checked against original files before declaring a particular build universally compatible. [Evidence policy](docs/EVIDENCE_POLICY.md).

## Publication and safety boundaries

- **Not distributed:** proprietary Android/Mars firmware, OTA files, extracted applications, kernel module binaries (`.ko`), DTB/DTBO/partition images, copyrighted firmware, private device logs, personal information or recovery packages.
- An identifier or SHA-256 hash **does not** grant permission to redistribute a file.
- There are **no runnable system-patching, bootloader, flash or driver-replacement scripts** in this initial public snapshot.
- Never apply build-mismatched FE / DTBO combinations or remove a functioning satellite frontend based on these notes.
- Source patches and improvements should be reviewed against the exact board and firmware. **No project-wide redistribution license is assigned yet.**

Independent research, unaffiliated with GTMedia. Contributions are welcome as sanitized observations, source-level analysis and maintainable fixes.
