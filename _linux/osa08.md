---
title: "Linux-Opas osa8"
author: "Samuel Kriikkula"
tags: linux
---

Networking eli verkostoituminen mahdollistaa erinäköisten tietokoneiden kommunikaation.

## ifconfig
`ifconfig` on komentorivityökalu jolla voi tarkastella ja konfiguroida verkkoliitäntöjä.

```
$ ifconfig
enp4s0    Link encap:Ethernet  HWaddr A8:A1:59:F0:30:EA
          inet addr:192.168.1.107  Bcast:192.168.1.255  Mask:255.255.255.0
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:851208 errors:0 dropped:2 overruns:0 frame:0
          TX packets:468050 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:1080204129  TX bytes:49148261

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:164 errors:0 dropped:0 overruns:0 frame:0
          TX packets:164 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:17660  TX bytes:17660
```

'enp4s0' on meidän ethernet-liitäntä. Jos käytät WLAN-adapteria, liitäntä alkaa sanalla 'wlan'. `inet` sanan jälkeen näkyy liitännän "private" ip, tässä tapauksessa 192.168.1.107

## iptables