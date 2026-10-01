# First boot

After a successful Companion flash, reset the board and confirm it starts.

## Steps

1. Antenna attached.
2. Tap **RST** (or power-cycle over USB).
3. Watch the OLED — firmware draws **Loading...**, then the node name and a Bluetooth
   pairing pin when nothing is connected.

## Expect

| Check | Pass when |
| --- | --- |
| OLED | Activity after RST (not stuck black) |
| BLE advert | Nearby scanner / MeshCore app sees **`MeshCore-`** plus an 8-character hex suffix |
| USB serial | Quiet on `/dev/ttyACM*` for Companion BLE — prefer OLED and BLE, not a chatty banner |

**Verified on this desk** after Companion BLE **v1.17.1**: board advertised as
**`MeshCore-6137C0F2`** (Nordic UART service). USB serial stayed silent.

Default advert name is the first four bytes of the node public key in hex, with prefix
`MeshCore-`. Change it later under [Configure](configure.md).

If BLE never appears, re-check you flashed **Companion · Bluetooth**, not Repeater — see
[Troubleshoot](troubleshoot.md).

Next: [Configure](configure.md).
