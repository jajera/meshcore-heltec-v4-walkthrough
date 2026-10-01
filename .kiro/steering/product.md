---
inclusion: always
---

# Product

`meshcore-heltec-v4-walkthrough` is a Zensical guide for flashing and first-configuring a
**Heltec WiFi LoRa 32 V4** with official MeshCore **Companion (Bluetooth)** firmware.

## The story

Brand-new board on the desk. Confirm Heltec V4, enter bootloader, flash Companion BLE from
the MeshCore web flasher, set the local radio preset, pair the MeshCore app, then prove the
node is alive.

## Audience

Someone with the board, a data USB-C cable, and a Chromium browser — not assumed to know
MeshCore already.

## Shape of the project

- **Zensical + Patina** docs under `docs/`.
- No Terraform, no cloud lab.
- Live site: `https://meshcore-heltec-v4-walkthrough.johna.kiwi/`.

## In scope

- Identify Heltec V4, bootloader, web flash (**Companion · Bluetooth**), first boot, radio
  preset + name, phone/web app pair, verify, troubleshoot.
- Screenshots and serial notes captured during a live setup pass.

## Out of scope (v1)

- Repeater / Room Server deep dives (mention only that other roles exist).
- Custom firmware builds / PlatformIO trees.
- Meshtastic paths or MeshCore-vs-Meshtastic essays.
- Enclosure/solar/GPS accessory deep dives beyond first-config mention.
- Multi-node network design / AWS IoT.

## Visual bias

Prefer screenshots, short numbered steps, and tables. One job per page.
