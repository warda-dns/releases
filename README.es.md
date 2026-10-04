<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**El filtro DNS que aprende de tu casa**

[![versión](https://img.shields.io/github/v/release/warda-dns/Releases?label=versi%C3%B3n&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![publicada](https://img.shields.io/github/release-date/warda-dns/Releases?label=publicada&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![descargas](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=descargas&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licencia](https://img.shields.io/badge/licencia-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![sitio web](https://img.shields.io/badge/sitio%20web-warda--dns.com-6E46B7)](https://warda-dns.com/es/)
[![documentación](https://img.shields.io/badge/documentaci%C3%B3n-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/es/)

[English](README.md) · [Français](README.fr.md) · **Español** · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## ¿Qué es Warda?

Warda bloquea la publicidad, el rastreo y los sitios peligrosos para todos los dispositivos de tu casa — teléfonos, ordenadores, televisión, videoconsolas — y aprende lo que tu familia realmente necesita, sin que tengas que gestionar listas tú mismo: simplemente activas las protecciones que quieres. Warda observa las peticiones de tu red y sugiere qué bloquear, con su contexto: qué dispositivo, justo después de qué. Nunca bloquea por su cuenta. Lo que aprende se queda en casa, en tu propio hardware.

<a name="download"></a>

## Descargar

Última versión: **0.7.11** · [notas de la versión](https://github.com/warda-dns/Releases/releases/tag/v0.7.11) · [todas las versiones](https://github.com/warda-dns/Releases/releases)

| Para instalar Warda en | Archivo | Qué es |
|---|---|---|
| **Raspberry Pi 4 o posterior** | [`warda_0.7.11_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_raspberrypi-arm64.img.xz) | Una imagen lista para una tarjeta microSD de 16 GB o más, escrita con Raspberry Pi Imager. |
| **Debian y Ubuntu**<br>amd64 · arm64 | [`warda_0.7.11_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_amd64.deb)<br>[`warda_0.7.11_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_arm64.deb) | Un paquete Debian para una máquina virtual o un servidor dedicado. |
| **Otro Linux**<br>amd64 · arm64 | [`warda_0.7.11_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_linux_amd64.tar.gz)<br>[`warda_0.7.11_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_linux_arm64.tar.gz) | Un archivo comprimido con solo el programa. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.11`<br>Consulta la [documentación](https://docs.warda-dns.com/es/) | Un único contenedor, para un servidor o un NAS que ya tenga Docker. |
| **Todas las instalaciones** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/SHA256SUMS.sig) | Las sumas de comprobación de cada archivo y su firma. |

Con Raspberry Pi Imager 2 también puedes abrir [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda.rpi-imager-manifest): Imager configura entonces el wifi, el usuario y SSH antes de grabar la tarjeta.

En Debian o Ubuntu, en un terminal:

```sh
sudo apt install ./warda_0.7.11_amd64.deb
```

Con Docker, en un terminal:

```sh
docker pull ghcr.io/warda-dns/warda:0.7.11
```

## Verifica tu descarga

`SHA256SUMS` contiene la suma de comprobación de cada archivo de una versión, y `SHA256SUMS.sig` es su firma Ed25519, hecha con la clave de publicación de Warda. Descarga ambos junto a tu archivo y, después:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Guarda la clave pública de abajo como `warda-release.pub` (el segundo comando necesita OpenSSL 3 o posterior). La misma clave está integrada en Warda: una caja solo instala las versiones firmadas con ella.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Instalar

La documentación te guía paso a paso, para Raspberry Pi, Docker, Debian y Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/es/)**. Cuando Warda esté en marcha, ábrelo en tu navegador y sigue al asistente.

## Actualizaciones

Una caja ya instalada se actualiza sola desde este repositorio: no hay nada que descargar a mano. Busca una versión nueva cada 6 horas y la instala por la noche cuando las actualizaciones automáticas están activadas. Solo se acepta una versión firmada con la clave de publicación, y se restaura la anterior si la nueva no arranca. Con Docker, la nueva versión se anuncia en la interfaz.

## Seguridad

¿Has encontrado una vulnerabilidad? Escribe a [contact@warda-dns.com](mailto:contact@warda-dns.com) en lugar de abrir una incidencia pública ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Enlaces

- Sitio web: [warda-dns.com](https://warda-dns.com/es/)
- Documentación: [docs.warda-dns.com](https://docs.warda-dns.com/es/)
- Área de cliente: [account.warda-dns.com](https://account.warda-dns.com/)
- Soporte: próximamente

## Licencia

Warda es software libre bajo licencia AGPLv3. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
