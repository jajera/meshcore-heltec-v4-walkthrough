# Reference

## Primary links

| Resource | URL |
| --- | --- |
| MeshCore flasher | <https://meshcore.io/flasher> |
| Flasher engine | <https://flasher.meshcore.io/> |
| MeshCore docs | <https://docs.meshcore.io/> |
| Radio presets | <https://docs.meshcore.io/radio_presets/> |
| Web app | <https://app.meshcore.nz> |
| Repeater / room USB config | <https://config.meshcore.dev> |
| Firmware source | <https://github.com/meshcore-dev/MeshCore> |
| Heltec WiFi LoRa 32 V4 | Heltec product / wiki pages for the V4 board |

## This walkthrough

| Item | Value |
| --- | --- |
| Board | Heltec WiFi LoRa 32 V4 |
| Flasher target | **Heltec v4** |
| Role | **Companion · Bluetooth** (`companionBle`) |
| NZ preset | **New Zealand (Narrow)** — 917.375 MHz / SF7 / BW62.5 / CR5 / path hash 2 |
| Desk firmware | Companion BLE **v1.17.1** |
| Desk BLE advert (pre-rename) | `MeshCore-6137C0F2` |
| USB ID (desk) | `303a:1001` Espressif USB JTAG/serial |

## Related roles (out of path)

Same **Heltec v4** flasher entry also offers Companion USB, Repeater, Room Server, and KISS.
Configure Repeater / Room Server via the USB config tool after flashing those roles — not
covered in this Companion guide.
