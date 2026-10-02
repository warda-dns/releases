<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**De DNS-filter die jouw huis leert kennen**

[![versie](https://img.shields.io/github/v/release/warda-dns/Releases?label=versie&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![uitgebracht](https://img.shields.io/github/release-date/warda-dns/Releases?label=uitgebracht&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![downloads](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=downloads&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licentie](https://img.shields.io/badge/licentie-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![website](https://img.shields.io/badge/website-warda--dns.com-6E46B7)](https://warda-dns.com/nl/)
[![documentatie](https://img.shields.io/badge/documentatie-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/nl/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · **Nederlands** · [Italiano](README.it.md) · [Português](README.pt.md) · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## Wat is Warda?

Warda blokkeert reclame, tracking en gevaarlijke sites voor elk apparaat in huis — telefoons, computers, televisie, spelcomputers — en leert wat jouw gezin echt nodig heeft, zonder dat je zelf lijsten hoeft te beheren: je zet gewoon de beschermingen aan die je wilt. Warda kijkt mee met de verzoeken van je netwerk en stelt voor wat te blokkeren, met context: welk apparaat, vlak na wat. Hij blokkeert nooit zelf. Wat hij leert, blijft bij jou thuis, op je eigen hardware.

<a name="download"></a>

## Downloaden

Nieuwste versie: **0.7.9** · [release-opmerkingen](https://github.com/warda-dns/Releases/releases/tag/v0.7.9) · [alle versies](https://github.com/warda-dns/Releases/releases)

| Warda installeren op | Bestand | Wat het is |
|---|---|---|
| **Raspberry Pi 4 of nieuwer** | [`warda_0.7.9_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_raspberrypi-arm64.img.xz) | Een kant-en-klare image voor een microSD-kaart van 16 GB of meer, te schrijven met Raspberry Pi Imager. |
| **Debian en Ubuntu**<br>amd64 · arm64 | [`warda_0.7.9_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_amd64.deb)<br>[`warda_0.7.9_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_arm64.deb) | Een Debian-pakket voor een virtuele machine of een dedicated server. |
| **Een andere Linux**<br>amd64 · arm64 | [`warda_0.7.9_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_linux_amd64.tar.gz)<br>[`warda_0.7.9_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_linux_arm64.tar.gz) | Een archief met alleen het programma. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.9`<br>Zie de [documentatie](https://docs.warda-dns.com/nl/) | Eén container, voor een server of een NAS die al Docker draait. |
| **Alle installaties** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/SHA256SUMS.sig) | De controlesommen van elk bestand, en hun handtekening. |

Met Raspberry Pi Imager 2 kun je ook [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda.rpi-imager-manifest) openen: Imager stelt dan de wifi, de gebruiker en SSH in voordat de kaart wordt geschreven.

Op Debian of Ubuntu, in een terminal:

```sh
sudo apt install ./warda_0.7.9_amd64.deb
```

Met Docker, in een terminal:

```sh
docker pull ghcr.io/warda-dns/warda:0.7.9
```

## Je download controleren

`SHA256SUMS` bevat de controlesom van elk bestand van een versie, en `SHA256SUMS.sig` is de Ed25519-handtekening ervan, gemaakt met de releasesleutel van Warda. Download beide naast je bestand, en daarna:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Sla de publieke sleutel hieronder op als `warda-release.pub` (het tweede commando vereist OpenSSL 3 of nieuwer). Dezelfde sleutel is in Warda ingebouwd: een kastje installeert alleen versies die ermee zijn ondertekend.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Installeren

De documentatie begeleidt je stap voor stap, voor de Raspberry Pi, Docker, Debian en Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/nl/)**. Zodra Warda draait, open je hem in je browser en volg je de assistent.

## Updates

Een kastje dat al is geïnstalleerd, werkt zichzelf bij vanuit deze repository: je hoeft niets met de hand te downloaden. Het zoekt elke 6 uur naar een nieuwe versie en installeert die ’s nachts wanneer automatische updates aanstaan. Alleen een versie die met de releasesleutel is ondertekend wordt aanvaard, en de vorige wordt teruggezet als de nieuwe niet start. Met Docker wordt de nieuwe versie in de interface aangekondigd.

## Beveiliging

Heb je een kwetsbaarheid gevonden? Schrijf naar [contact@warda-dns.com](mailto:contact@warda-dns.com) in plaats van een openbare issue te openen ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Links

- Website: [warda-dns.com](https://warda-dns.com/nl/)
- Documentatie: [docs.warda-dns.com](https://docs.warda-dns.com/nl/)
- Klantenzone: [account.warda-dns.com](https://account.warda-dns.com/)
- Ondersteuning: binnenkort

## Licentie

Warda is vrije software onder de AGPLv3-licentie. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
