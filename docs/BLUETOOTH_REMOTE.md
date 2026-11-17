# Bluetooth remote keylayout — historical correction

**Device:** GTMedia GTX Combo, Bluetooth remote detected in past tests as USB/HID vendor `0x0508`, product `0x0110`. **Status:** OPERATOR_REPORTED successful mapping repair, October 2026; original before/after files not distributed here.

## Symptom

The Bluetooth device-specific Android keylayout `Vendor_0508_Product_0110.kl` reportedly contained duplicate scan-code definitions (66, 67, 68, 88). The parsing problem caused Android to fall back to a generic keylayout and color keys were disabled or misinterpreted.

## Reported outcome

The operator removed duplicate key definitions and verified that Android selected the device-specific keylayout after Bluetooth reconnect. Earlier technical notes listed the following mappings for the repaired keylayout:

| Scan code | Android keylayout key name (historical) |
| --- | --- |
| 66 | `NUMPAD_LEFT_PAREN` |
| 67 | `STAR` |
| 68 | `F10` |
| 88 | `F12` |
| 184 | `PROG_RED` |
| 185 | `PROG_GREEN` |
| 187 | `PROG_YELLOW` |
| 186 | `PROG_BLUE` |

The final file was historically identified by SHA-256 `33f3396044235f95f9701d90e1d8f07906d5f8803bdf3b4795c2720fcc30ca82`, which has **not been rehashed in this publication**. The full original `.kl` file has not been uploaded, so this table is not a substitute for an exact original diff.

## Caveats

- HID scan codes depend on the paired remote hardware and selected Android device-specific layout.
- The old note also recorded a separate interaction with the Android package `com.google.android.katniss`, but that is **not** distributed here as a device-wide disable procedure.
- Vendor OTA updates can restore old mapping files, so behavior must be checked for each release.
- No system partition patcher or vendor keylayout file is being distributed.
