# Changelog

TurtleTAK Classic versions (the module in `modules/turtletak`). Newest first.

## Classic Edition 1.0.0
- First release for the original LAN Turtle and the LAN Turtle SD, as one Bash file in Hak5's module format (`configure`, `start`, `stop`, `status`), set up from the Turtle's own menu.
- Sensor on TAK: a position and status marker at the place you set, every 5 minutes by default. Marker type: sensor (`a-f-G-E-S`, the same as the Hub Edition), facility (`a-f-G-I`), team member (`a-f-G-U-C`) in any of ATAK's 14 team colors, or a custom CoT type.
- Network watch on the Turtle's LAN:
  - Learns the LAN on the first pass after a start, with no alerts.
  - New-device alerts.
  - Watched devices: missing after a set time, and back.
  - Ethernet link down and back up.
  - ARP spoofing: the gateway's IP claimed by another MAC, and the gateway restored when its real MAC is back.
- Alerts go to a TAK marker next to the Turtle (expires after an hour) and to All Chat Rooms, with quiet hours for GeoChat. Each alert type can be turned off. Alerts are queued while TAK is unreachable.
- TLS with a client certificate, like ATAK: with the `ncat` in the Hak5 firmware and `.pem` files (nothing to install), or with `openssl-util` and ATAK-style `.p12` files and their passwords. Plain TCP or UDP for servers that have those inputs. Warns 30 days before the client certificate expires.
- LAN Turtle SD: mounts the card's ext4 partition at `/sd` if needed (never formats), and keeps an alert log there for a set number of days.
- **Send test to TAK** in the menu.
