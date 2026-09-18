# Sicurezza e privacy (minimo sindacale)

## Principi

- Telecamera e NVR restano sulla **LAN** (o VLAN IoT isolata)
- **Niente port-forward** verso camera, Frigate o MQTT
- Credenziali e token **solo** in `.env` / secret file locali, mai in Git
- Accesso remoto solo via **VPN** (mesh/privata), senza esporre porte
- Registrazioni e eventuali dati biometrici restano **locali** e fuori repo

## Prima di usarlo “per davvero”

- [ ] Password uniche su camera e servizi
- [ ] UPnP disabilitato se il router lo permette
- [ ] Nessuna porta NVR/camera aperta su Internet
- [ ] Retention registrazioni limitata al necessario
- [ ] Notifiche esterne (se le aggiungi) senza mandare frame completi a caso

## Cosa questo esempio evita di proposito

Inventari host di casa, IP reali, bot Telegram, whitelist persone, script di rete personali.
