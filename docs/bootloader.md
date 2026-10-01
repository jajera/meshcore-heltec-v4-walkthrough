# Bootloader mode

Heltec V4 has no CP2102 — put the board in download / bootloader mode before the web
flasher.

## Steps

Board stays plugged in over USB-C:

1. Hold **USER** (silk may also say **PRG** / **BOOT**).
2. Tap **RST** once.
3. Release **USER**.

USB re-enumerates briefly (Espressif `303a:1001` drops, then returns). On this desk the
node came back as `/dev/ttyACM0` with a new USB device number — the browser still loses the
old handle, so reselect the Espressif / `ttyACM*` port in the flasher.

## Confirm

After the button sequence:

<div class="run" markdown>

```bash
esptool --chip esp32s3 --port /dev/ttyACM0 --before no-reset --after no-reset chip-id
```

```text {.no-copy}
Connected to ESP32-S3 on /dev/ttyACM0:
Chip type:          ESP32-S3 (QFN56) (revision v0.2)
Features:           Wi-Fi, BT 5 (LE), Dual Core + LP Core, 240MHz, Embedded PSRAM 2MB (AP_3v3)
…
Staying in bootloader.
```

</div>

If that connect fails, repeat the USER / RST / USER sequence, then reselect the port.

## Alternate

Hold **USER**, plug in USB-C, then release **USER**. Same download mode.

Next: [Flash firmware](flash.md).
