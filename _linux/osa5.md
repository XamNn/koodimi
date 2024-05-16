---
title: "Linux-Opas osa5"
author: "Samuel Kriikkula"
tags: linux
---

# Käyttäjät
Yhdessä Linux-järejstelmässä voi olla, ja aina onkin, usampi käyttäjä.

## Root
`root` käyttäjällä on oikeus tehdä mitä vaan Linux-järjestelmässä.
Jotkin operaatiot vaativatkin root-kättäjää.
Voit suorittaa komennon root-käyttäjällä kirjoittamalla komennon alkuun `sudo`.
Tee tämä kuitenkin harkiten!

## Luo uusi käytäjä
Käyttäjä luodaan `adduser` komennolla. Harjoitellaan samalla sudon käyttöä.
```
sudo adduser paulus
```

Voit halutessasi antaa sudo-oikeudet uudelle käyttäjälle:
```
sudo usermod -a -G sudo paulus
```

## Vaihda salasana
Salasana vaihdetaan `passwd` komennolla
```
passwd
```

## /etc/passwd
Kissataan */etc/passwd*.
Tämä tiedosto sisältää tietoa eri käyttäjistä.
```
cat /etc/passwd
```
