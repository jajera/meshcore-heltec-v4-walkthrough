# First boot

After a successful Companion flash, reset the board and confirm it starts.

## Steps

1. Antenna attached.
2. Tap **RST** (or power-cycle).
3. Watch the OLED for MeshCore / Companion status.

!!! note "Serial on this desk"

    After the v1.17.1 Companion flash, USB serial on `/dev/ttyACM*` showed ESP32-S3 ROM boot
    lines only (no chatty MeshCore banner). Prefer the OLED and the MeshCore app for “alive”
    checks.

If the board never appears over BLE later, re-check you flashed **Companion · Bluetooth**,
not Repeater — see [Troubleshoot](troubleshoot.md).

Next: [Configure](configure.md).
