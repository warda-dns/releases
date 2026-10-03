<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**Le filtre DNS qui apprend votre maison**

[![version](https://img.shields.io/github/v/release/warda-dns/Releases?label=version&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![publiée](https://img.shields.io/github/release-date/warda-dns/Releases?label=publi%C3%A9e&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![téléchargements](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=t%C3%A9l%C3%A9chargements&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licence](https://img.shields.io/badge/licence-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![site web](https://img.shields.io/badge/site%20web-warda--dns.com-6E46B7)](https://warda-dns.com/fr/)
[![documentation](https://img.shields.io/badge/documentation-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/fr/)

[English](README.md) · **Français** · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## Warda, c’est quoi ?

Warda bloque la publicité, le pistage et les sites dangereux pour tous les appareils de la maison — téléphones, ordinateurs, télévision, consoles — et apprend ce dont votre famille a vraiment besoin, sans avoir à gérer de listes vous-même : vous activez simplement les protections voulues. Warda observe les requêtes de votre réseau et propose quoi bloquer, avec son contexte : quel appareil, juste après quoi. Il ne bloque jamais de lui-même. Ce qu’il apprend reste chez vous, sur votre propre matériel.

<a name="download"></a>

## Télécharger

Dernière version : **0.7.10** · [notes de version](https://github.com/warda-dns/Releases/releases/tag/v0.7.10) · [toutes les versions](https://github.com/warda-dns/Releases/releases)

| Pour installer Warda sur | Fichier | Ce que c’est |
|---|---|---|
| **Raspberry Pi 4 ou plus récent** | [`warda_0.7.10_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_raspberrypi-arm64.img.xz) | Une image prête pour une carte microSD de 16 Go ou plus, écrite avec Raspberry Pi Imager. |
| **Debian et Ubuntu**<br>amd64 · arm64 | [`warda_0.7.10_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_amd64.deb)<br>[`warda_0.7.10_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_arm64.deb) | Un paquet Debian pour une machine virtuelle ou un serveur dédié. |
| **Un autre Linux**<br>amd64 · arm64 | [`warda_0.7.10_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_linux_amd64.tar.gz)<br>[`warda_0.7.10_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda_0.7.10_linux_arm64.tar.gz) | Une archive avec le programme seul. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.10`<br>Voir la [documentation](https://docs.warda-dns.com/fr/) | Un seul conteneur, pour un serveur ou un NAS qui fait déjà tourner Docker. |
| **Toutes les installations** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/SHA256SUMS.sig) | Les sommes de contrôle de chaque fichier, et leur signature. |

Avec Raspberry Pi Imager 2, vous pouvez aussi ouvrir [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.10/warda.rpi-imager-manifest) : Imager règle alors le Wi-Fi, l’utilisateur et SSH avant d’écrire la carte.

Sous Debian ou Ubuntu, dans un terminal :

```sh
sudo apt install ./warda_0.7.10_amd64.deb
```

Avec Docker, dans un terminal :

```sh
docker pull ghcr.io/warda-dns/warda:0.7.10
```

## Vérifier votre téléchargement

`SHA256SUMS` liste la somme de contrôle de chaque fichier d’une version, et `SHA256SUMS.sig` est sa signature Ed25519, faite avec la clé de publication de Warda. Téléchargez les deux à côté de votre fichier, puis :

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Enregistrez la clé publique ci-dessous sous le nom `warda-release.pub` (la seconde commande demande OpenSSL 3 ou plus récent). La même clé est intégrée à Warda : un boîtier n’installe que les versions signées avec elle.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Installer

La documentation vous guide pas à pas, pour le Raspberry Pi, Docker, Debian et Ubuntu : **[docs.warda-dns.com](https://docs.warda-dns.com/fr/)**. Une fois Warda démarré, ouvrez-le dans votre navigateur et suivez l’assistant.

## Mises à jour

Un boîtier déjà installé se met à jour tout seul depuis ce dépôt : rien à télécharger à la main. Il cherche une nouvelle version toutes les 6 heures et l’installe la nuit quand les mises à jour automatiques sont activées. Seule une version signée avec la clé de publication est acceptée, et la précédente est remise en place si la nouvelle ne démarre pas. Avec Docker, la nouvelle version est annoncée dans l’interface.

## Sécurité

Vous avez trouvé une faille ? Écrivez à [contact@warda-dns.com](mailto:contact@warda-dns.com) plutôt que d’ouvrir un ticket public ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Liens

- Site web : [warda-dns.com](https://warda-dns.com/fr/)
- Documentation : [docs.warda-dns.com](https://docs.warda-dns.com/fr/)
- Espace client : [account.warda-dns.com](https://account.warda-dns.com/)
- Assistance : bientôt

## Licence

Warda est un logiciel libre sous licence AGPLv3. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
