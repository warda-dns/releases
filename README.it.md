<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**Il filtro DNS che impara la tua casa**

[![versione](https://img.shields.io/github/v/release/warda-dns/Releases?label=versione&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![pubblicata](https://img.shields.io/github/release-date/warda-dns/Releases?label=pubblicata&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![download](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=download&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licenza](https://img.shields.io/badge/licenza-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![sito web](https://img.shields.io/badge/sito%20web-warda--dns.com-6E46B7)](https://warda-dns.com/it/)
[![documentazione](https://img.shields.io/badge/documentazione-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/it/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · **Italiano** · [Português](README.pt.md) · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## Che cos’è Warda?

Warda blocca pubblicità, tracciamento e siti pericolosi per tutti i dispositivi di casa — telefoni, computer, televisione, console — e impara di cosa ha davvero bisogno la tua famiglia, senza che tu debba gestire liste da solo: attivi semplicemente le protezioni che vuoi. Warda osserva le richieste della tua rete e suggerisce cosa bloccare, con il suo contesto: quale dispositivo, subito dopo cosa. Non blocca mai da solo. Ciò che impara resta a casa tua, sul tuo hardware.

<a name="download"></a>

## Scarica

Ultima versione: **0.7.11** · [note di rilascio](https://github.com/warda-dns/Releases/releases/tag/v0.7.11) · [tutte le versioni](https://github.com/warda-dns/Releases/releases)

| Per installare Warda su | File | Che cos’è |
|---|---|---|
| **Raspberry Pi 4 o successivo** | [`warda_0.7.11_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_raspberrypi-arm64.img.xz) | Un'immagine pronta per una scheda microSD da 16 GB o più, da scrivere con Raspberry Pi Imager. |
| **Debian e Ubuntu**<br>amd64 · arm64 | [`warda_0.7.11_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_amd64.deb)<br>[`warda_0.7.11_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_arm64.deb) | Un pacchetto Debian per una macchina virtuale o un server dedicato. |
| **Un altro Linux**<br>amd64 · arm64 | [`warda_0.7.11_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_linux_amd64.tar.gz)<br>[`warda_0.7.11_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_linux_arm64.tar.gz) | Un archivio con il solo programma. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.11`<br>Vedi la [documentazione](https://docs.warda-dns.com/it/) | Un solo container, per un server o un NAS che già esegue Docker. |
| **Tutte le installazioni** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/SHA256SUMS.sig) | Le somme di controllo di ogni file e la loro firma. |

Con Raspberry Pi Imager 2 puoi anche aprire [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda.rpi-imager-manifest): Imager imposta allora il Wi-Fi, l’utente e SSH prima di scrivere la scheda.

Su Debian o Ubuntu, in un terminale:

```sh
sudo apt install ./warda_0.7.11_amd64.deb
```

Con Docker, in un terminale:

```sh
docker pull ghcr.io/warda-dns/warda:0.7.11
```

## Verifica il download

`SHA256SUMS` elenca la somma di controllo di ogni file di una versione, e `SHA256SUMS.sig` è la sua firma Ed25519, creata con la chiave di rilascio di Warda. Scarica entrambi accanto al tuo file, poi:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Salva la chiave pubblica qui sotto come `warda-release.pub` (il secondo comando richiede OpenSSL 3 o successivo). La stessa chiave è integrata in Warda: una scatola installa solo le versioni firmate con essa.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Installazione

La documentazione ti guida passo dopo passo, per Raspberry Pi, Docker, Debian e Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/it/)**. Quando Warda è in funzione, aprilo nel browser e segui l’assistente.

## Aggiornamenti

Una scatola già installata si aggiorna da sola da questo repository: non c’è nulla da scaricare a mano. Cerca una nuova versione ogni 6 ore e la installa di notte quando gli aggiornamenti automatici sono attivi. Viene accettata solo una versione firmata con la chiave di rilascio, e la precedente viene ripristinata se la nuova non si avvia. Con Docker, la nuova versione viene annunciata nell’interfaccia.

## Sicurezza

Hai trovato una vulnerabilità? Scrivi a [contact@warda-dns.com](mailto:contact@warda-dns.com) invece di aprire una segnalazione pubblica ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Link

- Sito web: [warda-dns.com](https://warda-dns.com/it/)
- Documentazione: [docs.warda-dns.com](https://docs.warda-dns.com/it/)
- Area clienti: [account.warda-dns.com](https://account.warda-dns.com/)
- Assistenza: prossimamente

## Licenza

Warda è un software libero sotto licenza AGPLv3. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
