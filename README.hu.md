<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**A DNS-szűrő, amely megtanulja az otthonát**

[![verzió](https://img.shields.io/github/v/release/warda-dns/Releases?label=verzi%C3%B3&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![kiadva](https://img.shields.io/github/release-date/warda-dns/Releases?label=kiadva&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![letöltések](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=let%C3%B6lt%C3%A9sek&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licenc](https://img.shields.io/badge/licenc-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#docker)
[![webhely](https://img.shields.io/badge/webhely-warda--dns.com-6E46B7)](https://warda-dns.com/hu/)
[![dokumentáció](https://img.shields.io/badge/dokument%C3%A1ci%C3%B3-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/en/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · **Magyar** · [Ελληνικά](README.el.md)

</div>

## Mi az a Warda?

A Warda letiltja a reklámokat, a követést és a veszélyes oldalakat az otthon minden eszközén — telefonokon, számítógépeken, tévén, játékkonzolokon —, és megtanulja, mire van valóban szüksége a családjának, anélkül hogy Önnek listákat kellene kezelnie: egyszerűen bekapcsolja a kívánt védelmeket. A Warda figyeli a hálózat kéréseit, és javasolja, mit érdemes letiltani, a körülményekkel együtt: melyik eszköz, közvetlenül mi után. Magától soha nem tilt le semmit. Amit megtanul, az Önnél marad, a saját hardverén.

<a name="download"></a>

## Letöltés

Legújabb verzió: **0.8.8** · [kiadási megjegyzések](https://github.com/warda-dns/Releases/releases/tag/v0.8.8) · [minden verzió](https://github.com/warda-dns/Releases/releases)

| A Warda telepítése ide | Fájl | Mi ez |
|---|---|---|
| **Raspberry Pi 4 vagy újabb** | [`warda_0.8.8_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.8.8/warda_0.8.8_raspberrypi-arm64.img.xz) | Kész lemezkép legalább 16 GB-os microSD-kártyára, a Raspberry Pi Imager programmal felírva. |
| **Debian és Ubuntu**<br>amd64 · arm64 | [`warda_0.8.8_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.8.8/warda_0.8.8_amd64.deb)<br>[`warda_0.8.8_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.8.8/warda_0.8.8_arm64.deb) | Debian-csomag virtuális gépre vagy dedikált szerverre. |
| **Más Linux**<br>amd64 · arm64 | [`warda_0.8.8_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.8.8/warda_0.8.8_linux_amd64.tar.gz)<br>[`warda_0.8.8_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.8.8/warda_0.8.8_linux_arm64.tar.gz) | Archívum, amely csak a programot tartalmazza. |
| **Docker**<br>amd64 · arm64 | [`docker-compose.yml`](https://github.com/warda-dns/Releases/releases/download/v0.8.8/docker-compose.yml)<br>`ghcr.io/warda-dns/warda:0.8.8` | Egyetlen konténer olyan szerverre vagy NAS-ra, amelyen már fut a Docker. Lásd: [Telepítés Dockerrel](#docker). |
| **Minden telepítés** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.8.8/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.8.8/SHA256SUMS.sig) | Az összes fájl ellenőrzőösszege és azok aláírása. |

A Raspberry Pi Imager 2 programban megnyithatja a [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.8.8/warda.rpi-imager-manifest) fájlt is: az Imager ekkor a kártya írása előtt beállítja a Wi-Fi-t, a felhasználót és az SSH-t.

Debian vagy Ubuntu rendszeren, terminálban:

```sh
sudo apt install ./warda_0.8.8_amd64.deb
```

<a name="docker"></a>

## Telepítés Dockerrel

64 bites rendszert futtató Raspberry Pi 4-en vagy újabbon, illetve szerveren, egy üres könyvtárban:

```sh
curl -fsSLO https://github.com/warda-dns/Releases/releases/latest/download/docker-compose.yml
docker compose up -d
```

A Warda közvetlenül a gép hálózatát használja: az 53-as (DNS), a 80-as és a 443-as (webes felület) portnak szabadnak kell lennie. Ha a 80-as és a 443-as portot már egy reverse proxy, például a Traefik használja, a Warda indítása előtt állítsa be a fájlban a `WARDA_HTTP_LISTEN: ":8080"` és a `WARDA_HTTPS_LISTEN: ":8443"` értéket. Ha az 53-as portot a systemd-resolved foglalja, a fájl leírja, hogyan szabadíthatja fel.

Ezután nyissa meg a böngészőben a `http://<a gép címe>` címet (a végén `:8080`-nal, ha áthelyezte a portot), és kövesse a varázslót. A `docker logs warda` megadja a pontos címet, és foglalt port esetén megnevezi a módosítandó beállítást.

Frissítéshez írja be az új verziót a fájl `image:` sorába, majd futtassa a `docker compose pull && docker compose up -d` parancsot.

## A letöltés ellenőrzése

A `SHA256SUMS` egy kiadás minden fájljának ellenőrzőösszegét tartalmazza, a `SHA256SUMS.sig` pedig ennek Ed25519-aláírása, amely a Warda kiadási kulcsával készült. Töltse le mindkettőt a fájlja mellé, majd:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Mentse az alábbi nyilvános kulcsot `warda-release.pub` néven (a második parancshoz OpenSSL 3 vagy újabb szükséges). Ugyanez a kulcs be van építve a Wardába: egy doboz csak az ezzel aláírt verziókat telepíti.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Telepítés

A dokumentáció lépésről lépésre végigvezeti a telepítésen Raspberry Pi, Docker, Debian és Ubuntu esetén: **[docs.warda-dns.com](https://docs.warda-dns.com/en/)**. Amint a Warda fut, nyissa meg a böngészőjében, és kövesse a varázslót.

## Frissítések

A már telepített doboz ebből a tárolóból frissíti magát: semmit sem kell kézzel letölteni. 6 óránként keres új verziót, és éjszaka telepíti, ha az automatikus frissítések be vannak kapcsolva. Csak a kiadási kulccsal aláírt verziót fogadja el, és ha az új verzió nem indul el, visszaáll az előző. Docker esetén az új verziót a felület jelzi.

## Biztonság

Sebezhetőséget talált? Kérjük, nyilvános hibajegy nyitása helyett írjon a [contact@warda-dns.com](mailto:contact@warda-dns.com) címre ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Hivatkozások

- Webhely: [warda-dns.com](https://warda-dns.com/hu/)
- Dokumentáció: [docs.warda-dns.com](https://docs.warda-dns.com/en/)
- Ügyfélterület: [account.warda-dns.com](https://account.warda-dns.com/)
- Támogatás: hamarosan

## Licenc

A Warda szabad szoftver, AGPLv3 licenc alatt. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
