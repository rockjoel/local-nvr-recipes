# Installazione generica (Linux + Docker)

## Requisiti

- Docker Engine + Docker Compose plugin
- Camera IP raggiungibile in LAN via RTSP
- Solo bassa esposizione di rete: nell’esempio Frigate ascolta su `127.0.0.1`

## Passi

1. Clona il repo
2. `cp .env.example .env` e compila host/user/password RTSP
3. `cp config/config.example.yaml config/config.yml`
4. Adatta `hwaccel_args` in `config.yml` al tuo hardware (o toglili)
5. `docker compose up -d`
6. Apri `http://127.0.0.1:8971` da quella macchina

## Note

- Su Windows/NVIDIA o mini-PC Intel servono overlay diversi: qui resta un compose **base** portabile
- Non avviare due Frigate contemporaneamente sulla stessa camera se non sai gestire lo stream
