# Troubleshoot

| Symptom | Likely cause | Fix |
| --- | --- | --- |
| Browser shows no serial device | Charge-only cable or missing `dialout` | Data USB-C; add user to `dialout` and re-login |
| Flasher cannot open port | Not in bootloader / wrong port after RST | [Bootloader](bootloader.md); reselect Espressif `ttyACM*` |
| Flash fails mid-way | Cable / port / erase interrupted | Retry flash; keep cable seated |
| App never finds the device | Wrong role (Repeater / Room Server) or BLE off | Reflash **Companion · Bluetooth**; enable phone Bluetooth |
| Connected but no mesh peers | Alone on air or wrong preset | Confirm **New Zealand (Narrow)** (or local preset); need another MeshCore node |
| Illegal / dead air | Wrong band for your country | Use MeshCore [radio presets](https://docs.meshcore.io/radio_presets/); do not invent frequencies |
| Still on Meshtastic UI / behaviour | Board not re-flashed with MeshCore | Full Companion flash from [meshcore.io/flasher](https://meshcore.io/flasher) |

Still stuck? Re-check [Prerequisites](prerequisites.md) and [Flash](flash.md).
