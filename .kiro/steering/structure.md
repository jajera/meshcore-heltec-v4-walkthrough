---
inclusion: always
---

# Structure

## Layout

```plaintext
.github/workflows/     # docs, markdown-lint, commitmsg, auto-merge
.kiro/
  settings/mcp.json
  steering/
  hooks/
  specs/meshcore-heltec-v4-walkthrough/
.cursor/rules/         # Cursor mirrors of key steering
docs/
  index.md
  prerequisites.md
  identify.md
  bootloader.md
  flash.md
  first-boot.md
  configure.md
  phone.md
  verify.md
  troubleshoot.md
  reference.md
  assets/ images under assets/images/
  stylesheets/
overrides/main.html
zensical.toml
AGENTS.md
```

## Page rules

- Reading order must match `zensical.toml` nav.
- One job per page.
- Product claims need a source (see `source-lock.md`).
- Internal links: relative (`flash.md`) or site paths (`flash/`).

## Naming

| Item | Value |
| --- | --- |
| Board | Heltec WiFi LoRa 32 V4 |
| Flasher target | Heltec v4 |
| Flasher | https://meshcore.io/flasher (embeds https://flasher.meshcore.io/) |
| Role (v1 path) | Companion · Bluetooth (`companionBle`) |
| Example serial | Espressif USB JTAG/serial (`ttyACM*`) |
