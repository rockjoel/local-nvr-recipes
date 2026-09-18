# local-nvr-recipes

Public, **sanitized recipes** for a local NVR with [Frigate](https://frigate.video/) + Docker.

Goal: show a **privacy-first** approach (local, credentials out of Git, no port-forward to cameras).

> This repo is **not** a home system. It has no real IPs, network inventories, tokens, video, or trained models.

## What’s included

| Path | Content |
|---|---|
| [`docker-compose.yml`](docker-compose.yml) | Example Frigate + Mosquitto (MQTT) |
| [`config/config.example.yaml`](config/config.example.yaml) | Frigate config with placeholders |
| [`.env.example`](.env.example) | RTSP variables (copy to `.env`, do not commit) |
| [`mqtt/mosquitto.conf`](mqtt/mosquitto.conf) | MQTT broker on the internal Compose network only |
| [`SECURITY.md`](SECURITY.md) | Minimum security/privacy rules |
| [`INSTALL.md`](INSTALL.md) | Generic Linux startup |

## Quick start (Linux)

```bash
cp .env.example .env
# edit .env with YOUR camera host/user/password (LAN)
cp config/config.example.yaml config/config.yml
docker compose up -d
```

Typical UI (localhost only in the example): `http://127.0.0.1:8971`

## Limits

- Not a professional / certified video-surveillance guide
- Hardware accel (NVIDIA / VAAPI) must be adapted to your machine
- Telegram, face-train, VPN, and network inventories are **intentionally** left out

## License

[MIT](LICENSE)
