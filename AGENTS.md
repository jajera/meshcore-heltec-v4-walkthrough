# Agent Context

Zensical walkthrough for **Heltec WiFi LoRa 32 V4** first flash and MeshCore
**Companion (Bluetooth)** setup — published at
[meshcore-heltec-v4-walkthrough.johna.kiwi](https://meshcore-heltec-v4-walkthrough.johna.kiwi/).

## Read these first

Kiro loads `.kiro/steering/` automatically; other agents should read them directly.
Cursor also has `.cursor/rules/` for the same conventions.

| File | When it applies | What it covers |
| --- | --- | --- |
| `.kiro/steering/product.md` | always | Story, scope, non-goals, visual bias |
| `.kiro/steering/tech.md` | always | Stack, commands, CI |
| `.kiro/steering/structure.md` | always | Layout, reading order, naming |
| `.kiro/steering/source-lock.md` | always | Citation rules, verified facts, open TBDs |
| `.kiro/steering/docs-pattern.md` | `docs/**` | Page shapes for this walkthrough |
| `.kiro/steering/markdown-tables.md` | `docs/**` | GFM table hygiene |
| `.kiro/steering/lab-safety.md` | flash / serial / RF | USB, radio preset, TX caution |

Start readers at **Overview**, then follow nav order through flash and verify.

## Non-negotiables

1. **Cite product behaviour.** Do not invent flasher labels, bootloader steps, or
   radio presets from recall — check `source-lock.md` and official Heltec / MeshCore docs.
2. **Mark unverified work.** Steps not yet run on the physical board stay marked
   unverified until the live evidence pass.
3. **Prefer visuals.** Screenshots, short numbered steps, and tables over paragraphs.
4. **Respect reading order.** Overview → Prerequisites → Identify → Bootloader → Flash →
   First boot → Configure → Phone app → Verify → Troubleshoot → Reference.
5. **V4 only.** This guide targets plain **Heltec v4** in the MeshCore flasher. Do not
   expand into R8 comparison content.

## Facts that trip people up

- Desk board is plain **Heltec V4** → flasher target **Heltec v4**.
- V4 dropped CP2102 — enter **bootloader** before the web flasher (USER hold, RST, release USER).
- Web Serial needs **Chrome / Chromium / Edge**, not Firefox.
- First path: flash **Companion · Bluetooth** (`companionBle`), not Repeater or Room Server.
- After bootloader entry the serial port name may change — reselect it.
- Set radio preset for local law before transmitting (**New Zealand (Narrow)** for NZ).
- MeshCore and Meshtastic are incompatible meshes — reflash to switch.

The complete list, with sources, is in `.kiro/steering/source-lock.md`.

## Plan of record

`.kiro/specs/meshcore-heltec-v4-walkthrough/` holds `requirements.md`, `design.md`,
and `tasks.md`. Work phases in order; the live board evidence pass is last.

## Validation

```bash
python3 -m venv .venv
.venv/bin/pip install -r requirements.txt
.venv/bin/zensical build
```
