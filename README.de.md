<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**Der DNS-Filter, der Ihr Zuhause lernt**

[![Version](https://img.shields.io/github/v/release/warda-dns/Releases?label=Version&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![veröffentlicht](https://img.shields.io/github/release-date/warda-dns/Releases?label=ver%C3%B6ffentlicht&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=Downloads&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![Lizenz](https://img.shields.io/badge/Lizenz-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![Website](https://img.shields.io/badge/Website-warda--dns.com-6E46B7)](https://warda-dns.com/de/)
[![Dokumentation](https://img.shields.io/badge/Dokumentation-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/de/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · **Deutsch** · [Nederlands](README.nl.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## Was ist Warda?

Warda blockiert Werbung, Tracking und gefährliche Seiten für alle Geräte in Ihrem Zuhause — Handys, Computer, Fernseher, Spielkonsolen — und lernt, was Ihre Familie wirklich braucht, ohne dass Sie selbst Listen verwalten müssen: Sie schalten einfach die gewünschten Schutzfunktionen ein. Warda beobachtet die Anfragen Ihres Netzwerks und schlägt vor, was blockiert werden könnte, mit Kontext: welches Gerät, kurz nach was. Es blockiert nie von sich aus. Was es lernt, bleibt bei Ihnen zu Hause, auf Ihrer eigenen Hardware.

<a name="download"></a>

## Download

Neueste Version: **0.7.10** · [Versionshinweise](https://github.com/warda-dns/Releases/releases/tag/v0.7.10) · [alle Versionen](https://github.com/warda-dns/Releases/releases)

| Warda installieren auf | Datei | Was es ist |
|---|---|---|
| **Raspberry Pi 4 oder neuer** | [`warda_0.7.10_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_raspberrypi-arm64.img.xz) | Ein fertiges Image für eine microSD-Karte ab 16 GB, geschrieben mit Raspberry Pi Imager. |
| **Debian und Ubuntu**<br>amd64 · arm64 | [`warda_0.7.10_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_amd64.deb)<br>[`warda_0.7.10_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_arm64.deb) | Ein Debian-Paket für eine virtuelle Maschine oder einen dedizierten Server. |
| **Ein anderes Linux**<br>amd64 · arm64 | [`warda_0.7.10_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_linux_amd64.tar.gz)<br>[`warda_0.7.10_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_linux_arm64.tar.gz) | Ein Archiv, das nur das Programm enthält. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.10`<br>Siehe [Dokumentation](https://docs.warda-dns.com/de/) | Ein einziger Container, für einen Server oder ein NAS, auf dem bereits Docker läuft. |
| **Alle Installationen** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/SHA256SUMS.sig) | Die Prüfsummen aller Dateien und ihre Signatur. |

Mit Raspberry Pi Imager 2 können Sie auch [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda.rpi-imager-manifest) öffnen: Imager richtet dann WLAN, Benutzer und SSH ein, bevor die Karte beschrieben wird.

Unter Debian oder Ubuntu, in einem Terminal:

```sh
sudo apt install ./warda_0.7.10_amd64.deb
```

Mit Docker, in einem Terminal:

```sh
docker pull ghcr.io/warda-dns/warda:0.7.10
```

## Download überprüfen

`SHA256SUMS` enthält die Prüfsumme jeder Datei einer Version, und `SHA256SUMS.sig` ist ihre Ed25519-Signatur, erstellt mit dem Veröffentlichungsschlüssel von Warda. Laden Sie beide neben Ihre Datei herunter, dann:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Speichern Sie den öffentlichen Schlüssel unten als `warda-release.pub` (der zweite Befehl benötigt OpenSSL 3 oder neuer). Derselbe Schlüssel ist in Warda eingebaut: Eine Box installiert nur Versionen, die damit signiert sind.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Installieren

Die Dokumentation führt Sie Schritt für Schritt durch die Installation, für Raspberry Pi, Docker, Debian und Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/de/)**. Sobald Warda läuft, öffnen Sie es im Browser und folgen Sie dem Assistenten.

## Updates

Eine bereits installierte Box aktualisiert sich selbst aus diesem Repository: Es muss nichts von Hand heruntergeladen werden. Sie sucht alle 6 Stunden nach einer neuen Version und installiert sie nachts, wenn die automatischen Updates eingeschaltet sind. Nur eine mit dem Veröffentlichungsschlüssel signierte Version wird angenommen, und die vorherige wird wiederhergestellt, falls die neue nicht startet. Mit Docker wird die neue Version in der Oberfläche angekündigt.

## Sicherheit

Sie haben eine Sicherheitslücke gefunden? Schreiben Sie bitte an [contact@warda-dns.com](mailto:contact@warda-dns.com), statt ein öffentliches Issue zu eröffnen ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Links

- Website: [warda-dns.com](https://warda-dns.com/de/)
- Dokumentation: [docs.warda-dns.com](https://docs.warda-dns.com/de/)
- Kundenbereich: [account.warda-dns.com](https://account.warda-dns.com/)
- Support: demnächst

## Lizenz

Warda ist freie Software unter der AGPLv3-Lizenz. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
