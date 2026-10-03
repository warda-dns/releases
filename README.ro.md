<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**Filtrul DNS care învață casa dumneavoastră**

[![versiune](https://img.shields.io/github/v/release/warda-dns/Releases?label=versiune&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![publicată](https://img.shields.io/github/release-date/warda-dns/Releases?label=publicat%C4%83&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![descărcări](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=desc%C4%83rc%C4%83ri&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licență](https://img.shields.io/badge/licen%C8%9B%C4%83-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![site](https://img.shields.io/badge/site-warda--dns.com-6E46B7)](https://warda-dns.com/ro/)
[![documentație](https://img.shields.io/badge/documenta%C8%9Bie-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/en/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [Polski](README.pl.md) · **Română** · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## Ce este Warda?

Warda blochează reclamele, urmărirea și site-urile periculoase pe toate dispozitivele din casă — telefoane, calculatoare, televizor, console de jocuri — și învață de ce are cu adevărat nevoie familia dumneavoastră, fără să mai gestionați liste: activați pur și simplu protecțiile pe care le doriți. Warda observă cererile din rețea și vă sugerează ce să blocați, împreună cu contextul: ce dispozitiv, imediat după ce. Nu blochează niciodată nimic de unul singur. Ceea ce învață rămâne la dumneavoastră acasă, pe propriul echipament.

<a name="download"></a>

## Descărcare

Ultima versiune: **0.7.10** · [note de versiune](https://github.com/warda-dns/Releases/releases/tag/v0.7.10) · [toate versiunile](https://github.com/warda-dns/Releases/releases)

| Pentru a instala Warda pe | Fișier | Ce este |
|---|---|---|
| **Raspberry Pi 4 sau mai nou** | [`warda_0.7.10_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_raspberrypi-arm64.img.xz) | O imagine gata făcută pentru un card microSD de 16 GB sau mai mare, scrisă cu Raspberry Pi Imager. |
| **Debian și Ubuntu**<br>amd64 · arm64 | [`warda_0.7.10_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_amd64.deb)<br>[`warda_0.7.10_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_arm64.deb) | Un pachet Debian pentru o mașină virtuală sau un server dedicat. |
| **Alt Linux**<br>amd64 · arm64 | [`warda_0.7.10_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_linux_amd64.tar.gz)<br>[`warda_0.7.10_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_linux_arm64.tar.gz) | O arhivă care conține doar programul. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.10`<br>Consultați [documentația](https://docs.warda-dns.com/en/) | Un singur container, pentru un server sau un NAS care rulează deja Docker. |
| **Toate instalările** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/SHA256SUMS.sig) | Sumele de control ale fiecărui fișier și semnătura lor. |

Cu Raspberry Pi Imager 2 puteți deschide și [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda.rpi-imager-manifest): Imager configurează atunci Wi-Fi-ul, utilizatorul și SSH înainte de a scrie cardul.

Pe Debian sau Ubuntu, într-un terminal:

```sh
sudo apt install ./warda_0.7.10_amd64.deb
```

Cu Docker, într-un terminal:

```sh
docker pull ghcr.io/warda-dns/warda:0.7.10
```

## Verificați descărcarea

`SHA256SUMS` conține suma de control a fiecărui fișier al unei versiuni, iar `SHA256SUMS.sig` este semnătura sa Ed25519, făcută cu cheia de publicare Warda. Descărcați-le pe amândouă lângă fișierul dumneavoastră, apoi:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Salvați cheia publică de mai jos ca `warda-release.pub` (a doua comandă necesită OpenSSL 3 sau mai nou). Aceeași cheie este integrată în Warda: o cutie instalează doar versiunile semnate cu ea.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Instalare

Documentația vă ghidează pas cu pas, pentru Raspberry Pi, Docker, Debian și Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/en/)**. După ce Warda pornește, deschideți-l în browser și urmați asistentul.

## Actualizări

O cutie deja instalată se actualizează singură din acest depozit: nu trebuie descărcat nimic manual. Caută o versiune nouă la fiecare 6 ore și o instalează noaptea, când actualizările automate sunt activate. Este acceptată doar o versiune semnată cu cheia de publicare, iar cea anterioară este restabilită dacă cea nouă nu pornește. Cu Docker, noua versiune este anunțată în interfață.

## Securitate

Ați găsit o vulnerabilitate? Scrieți la [contact@warda-dns.com](mailto:contact@warda-dns.com) în loc să deschideți o sesizare publică ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Linkuri

- Site: [warda-dns.com](https://warda-dns.com/ro/)
- Documentație: [docs.warda-dns.com](https://docs.warda-dns.com/en/)
- Zona de client: [account.warda-dns.com](https://account.warda-dns.com/)
- Asistență: în curând

## Licență

Warda este software liber, sub licența AGPLv3. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
