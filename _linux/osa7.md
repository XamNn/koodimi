---
title: "Linux-Opas osa7"
author: "Samuel Kriikkula"
tags: linux
---

Tässä osassa perehdymme Systemd serviceihin ja daemoneihin. Servicet on ohjelmistoja, jotka ajaa taustalla huomaamatta.
Servicet tarjoaa erinäisiä funktionaalisuuksia kuten äänen, kuvan, internetyhteyden, tietokantoja, bluetooth-yhteyden, tai vaikkapa peliserverin.

*Varo:* **Kaikki Linux-jakelut eivät käytä Systemd:tä**

## systemctl
Komentoa `systemctl` käytetään servicien aloittamiseen ja lopettamiseen

Komennolla `systemctl ls-units --type=service` voit listata tämänhetkiset servicet.

Katsellaan serviceä *NetworkManager*. Se tarjoaa meille internet-yhteyden. Katso servicen tila komennolla:
```
systemctl status NetworkManager
```

Tässä toisia komentoja
```
sudo systemctl start ServiceTähän   # Aloita
sudo systemctl stop ServiceTähän    # Lopeta
sudo systemctl restart ServiceTähän # Uudelleenkäynnistä
sudo systemctl enable ServiceTähän  # Konfiguroi serviceä aloittamaan kun käynnistät Linuxin
sudo systemctl enable ServiceTähän  # Konfiguroi serviceä olla aloittamatta kun käynnistät Linuxin
```

Oman servicen teko on melko helppoa, mutta sitä ei tämä kurssi kata.