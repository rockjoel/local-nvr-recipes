# local-nvr-recipes

Ricette **pubbliche e sanitizzate** per un NVR locale con [Frigate](https://frigate.video/) + Docker.

Obiettivo: mostrare un approccio **privacy-first** (locale, credenziali fuori da Git, niente port-forward alle telecamere).

> Questo repo **non** è il sistema di casa. Non contiene IP reali, inventari rete, token, video o modelli addestrati.

## Cosa c’è

| Percorso | Contenuto |
|---|---|
| [`docker-compose.yml`](docker-compose.yml) | Frigate + Mosquitto (MQTT) di esempio |
| [`config/config.example.yaml`](config/config.example.yaml) | Config Frigate con placeholder |
| [`.env.example`](.env.example) | Variabili RTSP (da copiare in `.env`, non commitare) |
| [`mqtt/mosquitto.conf`](mqtt/mosquitto.conf) | Broker MQTT solo rete interna Compose |
| [`SECURITY.md`](SECURITY.md) | Regole minime di sicurezza/privacy |
| [`INSTALL.md`](INSTALL.md) | Avvio generico su Linux |

## Avvio rapido (Linux)

```bash
cp .env.example .env
# modifica .env con host/user/password della TUA camera (LAN)
cp config/config.example.yaml config/config.yml
docker compose up -d
```

UI tipica (solo localhost nell’esempio): `http://127.0.0.1:8971`

## Limiti

- Non è una guida di videosorveglianza professionale / certificata
- Hardware accel (NVIDIA / VAAPI) va adattato alla tua macchina
- Telegram, face-train, VPN e inventari rete **non** sono inclusi qui di proposito

## Licenza

[MIT](LICENSE)
