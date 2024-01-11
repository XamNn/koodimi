---
title: "Linux-Opas osa3"
author: "Samuel Kriikkula"
tags: linux
---

## Paketinhallinta

### Graafinen
![img](/linux/soft.png)

Voit asentaa paketteja graaffisesta käyttöliittymästä. Mutta on toinenkin (parempi) tapa!

### APT
Debian-pohjaisissa jakeluissa paketit asennetaan apt-ohjelmistolla.

Päivitä aptin indeksi
```
sudo apt update
```

Koitetaan ajaa htop
```
htop
```

Antaa virheen.

Asenna paketti `htop`.
```
sudo apt install htop
```

Ajetaan htop.
![img](/linux/htop.png)

:)