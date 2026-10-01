# Configure

Set identity and the **local radio preset** before you transmit.

MeshCore companion apps expose radio presets from the MeshCore App API. Suggested community
presets are documented under [Radio Presets](https://docs.meshcore.io/radio_presets/).

## NZ desk default

| Setting | Value |
| --- | --- |
| Preset | **New Zealand (Narrow)** |
| Frequency | **917.375** MHz |
| Spreading factor | **7** |
| Bandwidth | **62.5** kHz |
| Coding rate | **5** |

Source: MeshCore radio presets documentation / API example (`New Zealand (Narrow)`).

Outside NZ, pick the preset that matches your region and local rules (for example
**Australia (Narrow)** on 916.575 MHz). Do not invent frequencies.

## Steps

!!! warning "Handset UI unverified"

    Exact app menu labels may differ by MeshCore app version. Confirm on your phone.

1. Power the board; antenna on.
2. Open the MeshCore app (or [app.meshcore.nz](https://app.meshcore.nz)) — see [Phone app](phone.md).
3. Connect to the Companion over Bluetooth.
4. Set a **node name** you recognise.
5. Apply **New Zealand (Narrow)** (or your local preset).
6. Save / apply so the radio uses the new settings.

Next: [Phone app](phone.md).
