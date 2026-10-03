<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**The DNS filter that learns your home**

[![release](https://img.shields.io/github/v/release/warda-dns/Releases?label=release&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![released](https://img.shields.io/github/release-date/warda-dns/Releases?label=released&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![downloads](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=downloads&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licence](https://img.shields.io/badge/licence-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![website](https://img.shields.io/badge/website-warda--dns.com-6E46B7)](https://warda-dns.com/en/)
[![documentation](https://img.shields.io/badge/documentation-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/en/)

**English** · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## What is Warda?

Warda blocks advertising, tracking and dangerous sites for every device of your home — phones, computers, television, game consoles — and learns what your family really needs, without you having to manage lists yourself: you simply switch on the protections you want. Warda watches the requests of your network and suggests what to block, with its context: which device, just after what. It never blocks on its own. What it learns stays at home, on your own hardware.

<a name="download"></a>

## Download

Latest version: **0.7.10** · [release notes](https://github.com/warda-dns/Releases/releases/tag/v0.7.10) · [all versions](https://github.com/warda-dns/Releases/releases)

| To install Warda on | File | What it is |
|---|---|---|
| **Raspberry Pi 4 or later** | [`warda_0.7.10_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_raspberrypi-arm64.img.xz) | A ready image for a microSD card of 16 GB or more, written with Raspberry Pi Imager. |
| **Debian and Ubuntu**<br>amd64 · arm64 | [`warda_0.7.10_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_amd64.deb)<br>[`warda_0.7.10_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_arm64.deb) | A Debian package for a virtual machine or a dedicated server. |
| **Another Linux**<br>amd64 · arm64 | [`warda_0.7.10_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_linux_amd64.tar.gz)<br>[`warda_0.7.10_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_linux_arm64.tar.gz) | An archive with the program alone. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.10`<br>See the [documentation](https://docs.warda-dns.com/en/) | One container, for a server or a NAS that already runs Docker. |
| **Every installation** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/SHA256SUMS.sig) | The checksums of every file, and their signature. |

With Raspberry Pi Imager 2, you can also open [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda.rpi-imager-manifest): Imager then sets the Wi-Fi, the user and SSH before writing the card.

On Debian or Ubuntu, in a terminal:

```sh
sudo apt install ./warda_0.7.10_amd64.deb
```

With Docker, in a terminal:

```sh
docker pull ghcr.io/warda-dns/warda:0.7.10
```

## Verify your download

`SHA256SUMS` lists the checksum of every file of a version, and `SHA256SUMS.sig` is its Ed25519 signature, made with the release key of Warda. Download both next to your file, then:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Save the public key below as `warda-release.pub` (the second command needs OpenSSL 3 or later). The same key is built into Warda: a box only installs the versions signed with it.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Install

The documentation guides you step by step, for the Raspberry Pi, Docker, Debian and Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/en/)**. Once Warda is running, open it in your browser and follow the assistant.

## Updates

A box already installed updates itself from this repository: there is nothing to download by hand. It looks for a new version every 6 hours and installs it at night when automatic updates are on. Only a version signed with the release key is accepted, and the previous one is put back if the new one does not start. With Docker, the new version is announced in the interface.

## Security

Have you found a vulnerability? Please write to [contact@warda-dns.com](mailto:contact@warda-dns.com) rather than opening a public issue ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Links

- Website: [warda-dns.com](https://warda-dns.com/en/)
- Documentation: [docs.warda-dns.com](https://docs.warda-dns.com/en/)
- Customer area: [account.warda-dns.com](https://account.warda-dns.com/)
- Support: coming soon

## Licence

Warda is free software under the AGPLv3 licence. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
