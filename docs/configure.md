# Configure

Set identity and the **local radio preset** before you transmit.

Suggested community presets come from the MeshCore App API
([Radio Presets](https://docs.meshcore.io/radio_presets/), live:
`https://api.meshcore.nz/api/v1/config`).

## NZ desk default

| Setting | Value |
| --- | --- |
| Preset | **New Zealand (Narrow)** |
| Frequency | **917.375** MHz |
| Spreading factor | **7** |
| Bandwidth | **62.5** kHz |
| Coding rate | **5** |
| Path hash size | **2** (API `network_settings.path_hash_size`) |

API description string: `917.375MHz / SF7 / BW62.5 / CR5 / 2B`. Verified against the live
config API this pass.

Do not pick **New Zealand (Gisborne)** unless that is your local mesh — same centre
frequency, different SF / BW / path hash.

Outside NZ, pick the preset that matches your region and local rules (for example
**Australia (Narrow)** on 916.575 MHz / SF7 / BW62.5 / CR7). Do not invent frequencies.

## Steps

1. Antenna on; board powered (Companion advertising — see [First boot](first-boot.md)).
2. Pair in the MeshCore app — [Phone app](phone.md).
3. In device setup / Settings, set a **node name** you recognise (mesh display name).
4. Apply **New Zealand (Narrow)** (or your local preset) and save (checkmark).
5. Confirm frequency shows **917.375** MHz before relying on TX.

Next: [Phone app](phone.md).
