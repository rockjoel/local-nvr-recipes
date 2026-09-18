# Generic install (Linux + Docker)

## Requirements

- Docker Engine + Docker Compose plugin
- IP camera reachable on the LAN via RTSP
- Low network exposure: in the example, Frigate listens on `127.0.0.1`

## Steps

1. Clone the repo
2. `cp .env.example .env` and fill RTSP host/user/password
3. `cp config/config.example.yaml config/config.yml`
4. Adapt `hwaccel_args` in `config.yml` to your hardware (or remove them)
5. `docker compose up -d`
6. Open `http://127.0.0.1:8971` from that machine

## Notes

- Windows / NVIDIA or Intel mini-PCs need different overlays: this stays a portable **base** compose
- Do not run two Frigate instances on the same camera unless you know how to share the stream
