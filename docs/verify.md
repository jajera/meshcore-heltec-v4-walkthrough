# Verify

Prove the Companion is alive end-to-end.

!!! warning "Unverified on this desk"

    Complete these checks on your handset after the live flash. Second-node chat needs another
    MeshCore device in range (or a known local repeater / room).

## Checks

| Check | Pass when |
| --- | --- |
| BLE link | MeshCore app stays connected to the Heltec Companion |
| Identity | Node name matches what you set under [Configure](configure.md) |
| Radio preset | **New Zealand (Narrow)** (or your local preset) is active |
| Mesh presence | App can send an **advert** / see the node on the local list when peers exist |
| Optional chat | Direct message or room traffic if another MeshCore node is in range |

## Solo desk

With only one board, treat **stable BLE connection + correct preset** as the minimum pass.
Air traffic needs another MeshCore node (Companion, repeater, or room server) — Meshtastic
nodes will not answer.

Next: keep [Troubleshoot](troubleshoot.md) handy, or skim [Reference](reference.md).
