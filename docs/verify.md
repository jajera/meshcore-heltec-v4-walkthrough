# Verify

Prove the Companion is alive end-to-end.

**Verified on this desk** after Companion BLE **v1.17.1** + iPhone: BLE stayed up, node
identity and **New Zealand (Narrow)** set in the app, and a local repeater advert appeared
(**WR Windy Peak**). Direct-message ACK to a distant companion is path-dependent — treat a
**Failed** send as “no route yet”, not a bad flash.

## Checks

| Check | Pass when |
| --- | --- |
| BLE link | MeshCore app stays connected to the Heltec Companion |
| Identity | Node name matches what you set under [Configure](configure.md) / device setup |
| Radio preset | **New Zealand (Narrow)** active — **917.375** MHz / SF7 / BW62.5 / CR5 |
| Mesh presence | Contacts / discovery shows MeshCore peers (for example a local repeater) after an advert |
| Optional DM | Message to a Companion contact gets an ACK when RF path exists; else Flood Advert + Reset path — [Phone app](phone.md) |

## Minimum pass (one board)

Stable **BLE + correct preset** is enough to call the flash and phone path done.

Hearing a **repeater** proves RX on the local mesh. A successful **DM ACK** needs the other
Companion (or a path through repeaters) on the same preset — Meshtastic nodes will not answer.

Antennas on before intentional TX. Stuck? [Troubleshoot](troubleshoot.md).

Next: [Troubleshoot](troubleshoot.md) or [Reference](reference.md).
