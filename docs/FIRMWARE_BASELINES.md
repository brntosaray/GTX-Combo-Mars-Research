# Mars firmware versions and reported baselines

**Target:** GTMedia GTX Combo • Amlogic S905X3 • Android 9. Dates and hashes below are **historical references**, not fresh verification of a binary package in this public repository.

| Context | Previously reported observation | What is not implied |
| --- | --- | --- |
| September 2026 / Mars build dated 2026-09-17 | An operator-known working DVB-S/T2 reference state with FE/config/DTBO information | Identical behavior on later OTA versions |
| Mars 3.5.0 OTA / build dated 2026-10-13 | Changes to channel operation and terrestrial detection were reported; remote mapping had to be rechecked | Every board experiences the same regression |
| Mars 3.5.1 | Remote shortcut experiments were discussed; features and changes require matching device logs | Official support for every custom mapping |
| CoreELEC 22 / OpenATV | **Different research tracks** | Their Linux drivers cannot simply be renamed and used as Mars driver modules |

## Recorded FE module identifiers

- September working-reference FE module SHA-256: `0e0aefdcab8bb41e773f14d5bc4cdfc8325156f1bda83f4092b81cec649ff232` — **DOCUMENTED_IDENTIFIER**, not rehashed here.
- Separately discussed FD83 module SHA-256: `ebe6bfdb75fe9ea8b281580238fc9c9c3afaa79043f18f0186ba462e29bf66d8`. Do not assume that this file belongs to the same successful complete image/config pairing.
- FE after 2026-10-13 OTA was recorded as SHA-256: `5b12349769a7fea5fd192bb8fbdbeb7904369b344d37a87ec60d31a245c165df` — not newly checked.
- A previously noted `cfg_dvb.ini` digest is **truncated** in archived notes: `b571e1d7…64142`. This is **not** a usable SHA-256 value and must not be treated as an exact checksum.

## Release and test discipline

Record a *matched set* of firmware build, frontend driver, demux driver, config, device tree, and boot path. A file name or hash alone does not show why a configuration worked.

No OTA or firmware files are included here. This is not a mirror of GTMedia releases or a patch distribution site.
