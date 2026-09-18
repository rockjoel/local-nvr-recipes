# Security and privacy (baseline)

## Principles

- Camera and NVR stay on the **LAN** (or an isolated IoT VLAN)
- **No port-forward** to the camera, Frigate, or MQTT
- Credentials and tokens **only** in `.env` / local secret files — never in Git
- Remote access only via **VPN** (private mesh) — do not expose ports
- Recordings and any biometric data stay **local** and out of the repo

## Before using this “for real”

- [ ] Unique passwords on camera and services
- [ ] UPnP disabled if the router allows it
- [ ] No NVR/camera ports open to the Internet
- [ ] Recording retention limited to what you need
- [ ] External notifications (if you add any) without casually sending full frames

## What this example deliberately avoids

Home host inventories, real IPs, Telegram bots, person whitelists, personal network scripts.
