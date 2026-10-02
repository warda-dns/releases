<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**Filtr DNS, który poznaje Twój dom**

[![wersja](https://img.shields.io/github/v/release/warda-dns/Releases?label=wersja&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![wydano](https://img.shields.io/github/release-date/warda-dns/Releases?label=wydano&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![pobrania](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=pobrania&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licencja](https://img.shields.io/badge/licencja-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![strona](https://img.shields.io/badge/strona-warda--dns.com-6E46B7)](https://warda-dns.com/pl/)
[![dokumentacja](https://img.shields.io/badge/dokumentacja-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/en/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · [Português](README.pt.md) · **Polski** · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## Czym jest Warda?

Warda blokuje reklamy, śledzenie i niebezpieczne strony na wszystkich urządzeniach w Twoim domu — telefonach, komputerach, telewizorze, konsolach — i uczy się, czego naprawdę potrzebuje Twoja rodzina, bez samodzielnego zarządzania listami: po prostu włączasz ochronę, której chcesz. Warda obserwuje zapytania w Twojej sieci i podpowiada, co zablokować, wraz z kontekstem: które urządzenie, zaraz po czym. Nigdy nie blokuje niczego sama. To, czego się nauczy, zostaje u Ciebie w domu, na Twoim własnym sprzęcie.

<a name="download"></a>

## Pobierz

Najnowsza wersja: **0.7.9** · [informacje o wydaniu](https://github.com/warda-dns/Releases/releases/tag/v0.7.9) · [wszystkie wersje](https://github.com/warda-dns/Releases/releases)

| Aby zainstalować Wardę na | Plik | Co to jest |
|---|---|---|
| **Raspberry Pi 4 lub nowszy** | [`warda_0.7.9_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_raspberrypi-arm64.img.xz) | Gotowy obraz na kartę microSD o pojemności co najmniej 16 GB, zapisywany za pomocą Raspberry Pi Imager. |
| **Debian i Ubuntu**<br>amd64 · arm64 | [`warda_0.7.9_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_amd64.deb)<br>[`warda_0.7.9_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_arm64.deb) | Pakiet Debiana dla maszyny wirtualnej lub serwera dedykowanego. |
| **Inny Linux**<br>amd64 · arm64 | [`warda_0.7.9_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_linux_amd64.tar.gz)<br>[`warda_0.7.9_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda_0.7.9_linux_arm64.tar.gz) | Archiwum z samym programem. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.9`<br>Zobacz [dokumentację](https://docs.warda-dns.com/en/) | Jeden kontener dla serwera lub NAS-a, na którym już działa Docker. |
| **Wszystkie instalacje** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/SHA256SUMS.sig) | Sumy kontrolne wszystkich plików i ich podpis. |

W programie Raspberry Pi Imager 2 możesz też otworzyć plik [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.9/warda.rpi-imager-manifest): Imager ustawi wtedy Wi-Fi, użytkownika i SSH przed zapisaniem karty.

W Debianie lub Ubuntu, w terminalu:

```sh
sudo apt install ./warda_0.7.9_amd64.deb
```

Z Dockerem, w terminalu:

```sh
docker pull ghcr.io/warda-dns/warda:0.7.9
```

## Sprawdź pobrany plik

`SHA256SUMS` zawiera sumę kontrolną każdego pliku wydania, a `SHA256SUMS.sig` to jego podpis Ed25519, złożony kluczem wydań Wardy. Pobierz oba pliki obok swojego pliku, a następnie:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Zapisz poniższy klucz publiczny jako `warda-release.pub` (drugie polecenie wymaga OpenSSL 3 lub nowszego). Ten sam klucz jest wbudowany w Wardę: urządzenie instaluje tylko wersje nim podpisane.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Instalacja

Dokumentacja prowadzi krok po kroku, dla Raspberry Pi, Dockera, Debiana i Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/en/)**. Gdy Warda już działa, otwórz ją w przeglądarce i postępuj zgodnie z kreatorem.

## Aktualizacje

Zainstalowane już urządzenie aktualizuje się samo z tego repozytorium: niczego nie trzeba pobierać ręcznie. Co 6 godzin sprawdza, czy jest nowa wersja, i instaluje ją w nocy, gdy automatyczne aktualizacje są włączone. Przyjmowana jest tylko wersja podpisana kluczem wydań, a jeśli nowa wersja się nie uruchomi, przywracana jest poprzednia. W przypadku Dockera nowa wersja jest zapowiadana w interfejsie.

## Bezpieczeństwo

Masz informację o luce w zabezpieczeniach? Napisz na [contact@warda-dns.com](mailto:contact@warda-dns.com) zamiast otwierać publiczne zgłoszenie ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Linki

- Strona: [warda-dns.com](https://warda-dns.com/pl/)
- Dokumentacja: [docs.warda-dns.com](https://docs.warda-dns.com/en/)
- Strefa klienta: [account.warda-dns.com](https://account.warda-dns.com/)
- Pomoc: wkrótce

## Licencja

Warda to wolne oprogramowanie na licencji AGPLv3. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
