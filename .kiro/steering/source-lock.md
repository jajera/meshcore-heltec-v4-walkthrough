---
inclusion: always
---

# Source lock

Ground hardware and firmware claims here. Unsourced behaviour does not ship as verified.

## Citation rules

1. Prefer primary docs: Heltec product pages, MeshCore docs / flasher UI labels from
   screenshots taken in this repo.
2. When a live setup contradicts a draft number, update this file and the page in the same change.
3. Mark uncertain lines clearly until observed on the board.

## Verified facts

| Fact | Status | Source notes |
| --- | --- | --- |
| Desk unit is plain **Heltec V4** (2MB PSRAM, Espressif USB `303a:1001`) | observed | `esptool` Features: Embedded PSRAM 2MB; `lsusb` / `ttyACM*` MAC `10:bd:a3:5b:13:e0` |
| Bootloader: hold USER/PRG, tap RST, release USER | Heltec + prior live | Heltec QS |
| MeshCore flasher lists **Heltec v4** with Companion BLE/USB, Repeater, Room Server, KISS | observed + catalog | screenshots `identify-flasher-device.png`, `flash-device-firmware.png`; `config.json` |
| Companion Bluetooth role title is **Companion Bluetooth** (`companionBle`) | observed | flasher Choose role UI |
| Flashed Companion BLE **v1.17.1** (`heltec_v4_companion_radio_ble-v1.17.1-d929643-merged.bin`) | observed | esptool write_flash verified hash |
| NZ suggested preset **New Zealand (Narrow)** — 917.375 MHz / SF7 / BW62.5 / CR5 | MeshCore docs | [Radio Presets](https://docs.meshcore.io/radio_presets/) |
| Web Serial needs Chrome / Chromium / Edge | MeshCore getting-started | MeshCore Europe get-started; Web Serial |

## Open TBDs

- Phone BLE pair + advert / first chat — confirm on handset (not simulatable from desk agent).
- First-boot OLED strings under MeshCore Companion — not captured over USB serial this pass (boot ROM only on ACM).
- App radio-preset UI screenshot for **New Zealand (Narrow)**.
