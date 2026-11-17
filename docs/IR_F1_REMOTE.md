# Infrared TV V+ / F1 remote mapping — historical result

**Status:** OPERATOR_REPORTED successful mapping repair on one GTMedia GTX Combo. No firmware/device-tree binary or patching tool distributed.

## Historical inputs

A separate IR remote button identified by the operator as the upper **TV V+ / F1** function was observed in earlier tests with:

| Field | Historic value |
| --- | --- |
| IR custom code | `0xfc03` |
| IR scan code | `0x5d` |
| Linux `KEY_F1` | `59` |
| Android `KEYCODE_F1` | `131` |
| Device-tree mapping context | `RCU_001_V1_KEY_PARS` |

The historic operator report says the selected device-tree mapping was corrected and F1 started working.

## Important boot-storage finding

Previous operator investigation found that changing a DTB view in the normal boot partition alone did not affect this active Amlogic boot path: the bootloader also used redundant device-tree data in an internal reserved area. **This is a hardware-specific historical diagnosis, not a recommendation to edit those areas.** No raw partition offsets or write instructions are published here.

Other function-key shortcut codes may vary by firmware build and are not a verified universal reference.

## Preservation

Do not flash DTB, reserved boot data, or edit IR tables using this summary. A safe upstream fix would require exact source provenance, boot-flow confirmation, signed/offline review as appropriate, and receiver-specific testing.
