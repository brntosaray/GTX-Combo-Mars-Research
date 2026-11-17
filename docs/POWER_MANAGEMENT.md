# Power-off, fan and front-panel indicator behavior

**Status: OPEN / unresolved in the available historical evidence** (October 2026).

## Operator-observed symptoms

- Power-button menu sometimes responded after a delay or appeared to ignore the selected action.
- Shutdown sometimes took roughly two minutes.
- Fan continued rotating and a front-panel Wi-Fi indicator remained illuminated after an apparent power-off transition.

## Reported diagnostic snapshots

- `dumpsys power` at one checkpoint showed `mWakefulness=Awake` and `mIsPowered=true`. This may reflect the instant it was collected, **not** the eventual power-off state.
- `persist.sys.standby_state=on` was reported.
- An earlier read of `/sys/class/leds/sys_led/brightness` showed `255`, but it does not alone establish why an LED stayed lit.

## Not established

No completed root-cause diagnosis is available here. The behavior could involve userspace shutdown flow, vendor services, standby configuration, GPIO state or external hardware, but these remain **hypotheses**, not proven causes.

## Helpful non-invasive evidence

Future contributors could compare redacted timestamped Android shutdown logs, boot and power-state summaries, firmware versions, service logs and the actual physical state. Any request to change GPIO, boot partitions, DTB or power control requires explicit approval and hardware-specific validation.

This document does **not** provide risky live power-control experiments or a tested remedy.
