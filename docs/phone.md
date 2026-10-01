# Phone app

Pair the MeshCore Companion so the phone is your day-to-day client.

## Clients

| Client | Notes |
| --- | --- |
| MeshCore Android / iOS app | Preferred for BLE Companion |
| [app.meshcore.nz](https://app.meshcore.nz) | Web client (BLE where the browser supports it) |

Official companion pointers also appear on the [MeshCore README](https://github.com/meshcore-dev/MeshCore).

## Steps

**Verified on this desk** with Companion BLE **v1.17.1** and an iPhone: connect → device
setup → **New Zealand (Narrow)** → heard local repeater traffic.

1. Flash completed as **Companion · Bluetooth** ([Flash](flash.md)).
2. Board powered; OLED shows **`MeshCore-`** plus hex (or your renamed node) and a
   **Pin:######**. Phone Bluetooth on; allow MeshCore Bluetooth permission when iOS asks.
3. Open the MeshCore app → **Connect** / add device → select the matching **`MeshCore-…`**
   entry.
4. Enter the **PIN from the OLED** (not `123456` when the screen shows a pin — that default
   is for headless boards).
5. When setup asks for a **name**, enter the **node name** others will see on the mesh — not
   a legal personal-name field. Finish [Configure](configure.md) (preset) if not done yet.

## Stuck on Connecting

1. Force-quit the MeshCore app.
2. iPhone **Settings → Bluetooth** → forget any **MeshCore-…** entry.
3. Toggle phone Bluetooth off, then on.
4. Tap **RST** on the board (or power-cycle USB).
5. Wait for the OLED pin again, then reconnect and enter the new pin promptly.

## Contacts and messages

- Import a shared contact with a `meshcore://contact/add?…` link or QR (Contacts → add from
  clipboard / scan).
- `type=1` is a Companion chat contact. Repeaters appear separately — useful for path, not
  as a person to DM.
- **Failed** send with no ACK: confirm **New Zealand (Narrow)**, antenna on, **Flood Advert**,
  then **Reset path** on that contact and retry. You need RF reach (direct or via a repeater
  such as a local peak site).

If the app never sees the radio, you may have flashed Repeater / Room Server — reflash
Companion Bluetooth. See [Troubleshoot](troubleshoot.md).

Next: [Verify](verify.md).
