<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**DNS filtr, který se učí váš domov**

[![verze](https://img.shields.io/github/v/release/warda-dns/Releases?label=verze&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![vydáno](https://img.shields.io/github/release-date/warda-dns/Releases?label=vyd%C3%A1no&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![stažení](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=sta%C5%BEen%C3%AD&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licence](https://img.shields.io/badge/licence-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![web](https://img.shields.io/badge/web-warda--dns.com-6E46B7)](https://warda-dns.com/cs/)
[![dokumentace](https://img.shields.io/badge/dokumentace-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/en/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [Polski](README.pl.md) · [Română](README.ro.md) · **Čeština** · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## Co je Warda?

Warda blokuje reklamu, sledování a nebezpečné weby pro všechna zařízení ve vaší domácnosti — telefony, počítače, televizi, herní konzole — a učí se, co vaše rodina opravdu potřebuje, aniž byste museli sami spravovat seznamy: jednoduše zapnete ochrany, které chcete. Warda sleduje dotazy ve vaší síti a navrhuje, co blokovat, i s kontextem: které zařízení a hned po čem. Nikdy neblokuje sama od sebe. Co se naučí, zůstává u vás doma, na vašem vlastním hardwaru.

<a name="download"></a>

## Stáhnout

Nejnovější verze: **0.7.8** · [poznámky k vydání](https://github.com/warda-dns/Releases/releases/tag/v0.7.8) · [všechny verze](https://github.com/warda-dns/Releases/releases)

| Instalace Wardy na | Soubor | Co to je |
|---|---|---|
| **Raspberry Pi 4 nebo novější** | [`warda_0.7.8_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.8/warda_0.7.8_raspberrypi-arm64.img.xz) | Hotový obraz pro kartu microSD s kapacitou 16 GB nebo více, zapsaný pomocí Raspberry Pi Imager. |
| **Debian a Ubuntu**<br>amd64 · arm64 | [`warda_0.7.8_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.8/warda_0.7.8_amd64.deb)<br>[`warda_0.7.8_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.8/warda_0.7.8_arm64.deb) | Balíček pro Debian pro virtuální stroj nebo dedikovaný server. |
| **Jiný Linux**<br>amd64 · arm64 | [`warda_0.7.8_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.8/warda_0.7.8_linux_amd64.tar.gz)<br>[`warda_0.7.8_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.8/warda_0.7.8_linux_arm64.tar.gz) | Archiv se samotným programem. |
| **Docker**<br>amd64 · arm64 | Viz [dokumentace](https://docs.warda-dns.com/en/) | Jeden kontejner pro server nebo NAS, na kterém už Docker běží. |
| **Všechny instalace** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.8/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.8/SHA256SUMS.sig) | Kontrolní součty všech souborů a jejich podpis. |

V Raspberry Pi Imager 2 můžete také otevřít soubor [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.8/warda.rpi-imager-manifest): Imager pak před zápisem karty nastaví Wi-Fi, uživatele a SSH.

V Debianu nebo Ubuntu, v terminálu:

```sh
sudo apt install ./warda_0.7.8_amd64.deb
```

## Ověřte stažený soubor

`SHA256SUMS` obsahuje kontrolní součet každého souboru vydání a `SHA256SUMS.sig` je jeho podpis Ed25519 vytvořený vydavatelským klíčem Wardy. Stáhněte si oba soubory vedle svého souboru a potom:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Níže uvedený veřejný klíč uložte jako `warda-release.pub` (druhý příkaz vyžaduje OpenSSL 3 nebo novější). Stejný klíč je zabudován ve Wardě: krabička nainstaluje jen verze, které jsou jím podepsané.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Instalace

Dokumentace vás provede krok za krokem, pro Raspberry Pi, Docker, Debian a Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/en/)**. Jakmile Warda běží, otevřete ji v prohlížeči a postupujte podle průvodce.

## Aktualizace

Již nainstalovaná krabička se aktualizuje sama z tohoto repozitáře: nic není třeba stahovat ručně. Každých 6 hodin zjišťuje, zda je k dispozici nová verze, a nainstaluje ji v noci, pokud jsou zapnuté automatické aktualizace. Přijata je jen verze podepsaná vydavatelským klíčem, a pokud se nová verze nespustí, vrátí se předchozí. U Dockeru je nová verze oznámena v rozhraní.

## Zabezpečení

Našli jste zranitelnost? Napište prosím na [contact@warda-dns.com](mailto:contact@warda-dns.com), místo abyste zakládali veřejné hlášení ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Odkazy

- Web: [warda-dns.com](https://warda-dns.com/cs/)
- Dokumentace: [docs.warda-dns.com](https://docs.warda-dns.com/en/)
- Zákaznická zóna: [account.warda-dns.com](https://account.warda-dns.com/)
- Podpora: již brzy

## Licence

Warda je svobodný software pod licencí AGPLv3. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
