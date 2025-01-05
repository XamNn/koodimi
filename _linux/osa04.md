---
title: "Linux-Opas osa4"
author: "Samuel Kriikkula"
tags: linux
---

# Tiedostonhallinta
Tiedostoja ja hakemistoja voi operoida Linuxilla näppärästi terminaalissa

## ls
`ls` komeneto tulostaa tämänhetkisen hakemiston sisältämät tiedostot ja hakemistot.
 
![img](/linux/ls.png)

Sinisellä värjätyt tiedostot ovat hakemistoja (kyllä, Linuxissa hakemistotkin ovat tiedostoja).

### -la
`ls -la` antaa isomman listauksen. Lisää tästä myöhemmin.

## cd
`cd` vaihtaa työhakemiston, eli sen missä tällä hetkellä oleskelemme.
Voit esimerkiksi ajaa `cd Videos` avataksesi Videos hakemiston.

`..` tarkoittaa ylähakemistoa.
```
cd ..
```

## touch
Luo tiedostoja! 
```
touch testi.txt
```

## cp
Kopioi tiedostoja. Jos haluat kopioida hakemiston, lisää `-r` komennon nimen jälkeen.
```
cp testi.txt kopio.txt
```

## mv
Siirrä tiedostoja.
`mv testi.txt uusi-nimi.txt`

## rm
Poista tiedostoja! VARO: tiedostot poistetaan pysyvästi! Jos haluat poistaa hakemiston, lisää `-r` komennon nimen jälkeen.
```
rm uusi-nimi.txt
```

## cat
Kissalla voit tulostaa tiedoston sisällön terminaaliin.
```
cat /etc/fstab
```

## Nano
Nano voi olla hyvä ensimmäinen terminaalieditori. Se on melko helppokäyttöinen. Muita vaihtoehtoja ovat esimerkiksi Vim, Emacs, ja NeoVim.

```
nano editoi-nanolla.txt
```

![img](/linux/nano.png)

Nanossa on sisäänrakennettuna monia näppäinkomentoja. Näistä lisää myöhemmin.
Poistu nanosta Ctrl+X, Ctrl+Y, Enter

## Oikeudet ja ls -la

Suorita `ls -la`
```
$ ls -la
total 8
drwxr-xr-x  2 samuel users 4096 24. 3. 17:21 .
drwx------ 45 samuel users 4096 24. 3. 17:20 ..
-rwxrw-r--  1 samuel users    0 24. 3. 17:20 tiedosto
```

`-` merkki rivin alussa merkkaa tiedostoa, kun taas `d` merkkaa hakemistoa.

Oikeudet näyttää merkkijono `rwxrw-r--`

r = lukuoikeudet
w = kirjoitusoikeudet
x = suoritusoikeudet

Ensimmäiset kolme merkkiä määrittää tiedoston omistajan oikeudet, seuraavat kolme taas omistajan ryhmän oikeudet, ja viimeiset kolme kaikkien käyttäjien oikeudet.
Tämä tarkoittaa sitä, että tiedostoa voi lukea, kirjoittaa ja suorittaa tiedoston omistaja, tiedostoa voi lukea ja kijroittaa omistajan ryhmän jäsenet ja kaikki voivat lukea tiedostoa.
