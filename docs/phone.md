# Phone app

Pair the MeshCore Companion so the phone is your day-to-day client.

## Clients

| Client | Notes |
| --- | --- |
| MeshCore Android / iOS app | Preferred for BLE Companion |
| [app.meshcore.nz](https://app.meshcore.nz) | Web client (BLE where the browser supports it) |

Official companion pointers also appear on the [MeshCore README](https://github.com/meshcore-dev/MeshCore).

## Steps

!!! warning "Handset unverified"

    BLE pair UX is handset-only. Confirm on your phone.

1. Flash completed as **Companion · Bluetooth** ([Flash](flash.md)).
2. Board powered; Bluetooth enabled on the phone.
3. Open the MeshCore app → scan / add device → select your Heltec Companion.
4. Accept the pairing prompt if shown.
5. Confirm the device appears connected, then finish [Configure](configure.md) if you have
   not set the radio preset yet.

If the app never sees the radio, you may have flashed Repeater / Room Server — reflash
Companion Bluetooth. See [Troubleshoot](troubleshoot.md).

Next: [Verify](verify.md).
