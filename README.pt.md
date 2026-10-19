<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**O filtro DNS que aprende a sua casa**

[![versão](https://img.shields.io/github/v/release/warda-dns/Releases?label=vers%C3%A3o&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![publicada](https://img.shields.io/github/release-date/warda-dns/Releases?label=publicada&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![transferências](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=transfer%C3%AAncias&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![licença](https://img.shields.io/badge/licen%C3%A7a-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Fedora · RHEL](https://img.shields.io/badge/Fedora%20%C2%B7%20RHEL-amd64%20%C2%B7%20arm64-294172?logo=fedora&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#docker)
[![site](https://img.shields.io/badge/site-warda--dns.com-6E46B7)](https://warda-dns.com/pt/)
[![documentação](https://img.shields.io/badge/documenta%C3%A7%C3%A3o-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/pt/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · **Português** · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## O que é o Warda?

O Warda bloqueia publicidade, rastreamento e sites perigosos em todos os dispositivos da sua casa — telemóveis, computadores, televisão, consolas — e aprende o que a sua família realmente precisa, sem que tenha de gerir listas por si: basta ativar as proteções que pretende. O Warda observa os pedidos da sua rede e sugere o que bloquear, com o seu contexto: qual o dispositivo, logo a seguir a quê. Nunca bloqueia por conta própria. O que aprende fica em sua casa, no seu próprio equipamento.

<a name="download"></a>

## Transferir

Última versão: **0.9.3** · [notas da versão](https://github.com/warda-dns/Releases/releases/tag/v0.9.3) · [todas as versões](https://github.com/warda-dns/Releases/releases)

| Para instalar o Warda em | Ficheiro | O que é |
|---|---|---|
| **Raspberry Pi 4 ou posterior** | [`warda_0.9.3_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/warda_0.9.3_raspberrypi-arm64.img.xz) | Uma imagem pronta para um cartão microSD de 16 GB ou mais, gravada com o Raspberry Pi Imager. |
| **Debian e Ubuntu**<br>amd64 · arm64 | [`warda_0.9.3_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/warda_0.9.3_amd64.deb)<br>[`warda_0.9.3_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/warda_0.9.3_arm64.deb) | Um pacote Debian para uma máquina virtual ou um servidor dedicado. |
| **Fedora, RHEL, Rocky Linux, AlmaLinux**<br>amd64 · arm64 | [`warda-0.9.3-1.x86_64.rpm`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/warda-0.9.3-1.x86_64.rpm)<br>[`warda-0.9.3-1.aarch64.rpm`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/warda-0.9.3-1.aarch64.rpm) | Um pacote rpm para uma máquina virtual ou um servidor dedicado. |
| **Outro Linux**<br>amd64 · arm64 | [`warda_0.9.3_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/warda_0.9.3_linux_amd64.tar.gz)<br>[`warda_0.9.3_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/warda_0.9.3_linux_arm64.tar.gz) | Um arquivo apenas com o programa. |
| **Docker**<br>amd64 · arm64 | [`docker-compose.yml`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/docker-compose.yml)<br>`ghcr.io/warda-dns/warda:0.9.3` | Um único contentor, para um servidor ou uma NAS que já corra Docker. Consulte [Instalar com Docker](#docker). |
| **Todas as instalações** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/SHA256SUMS.sig) | As somas de verificação de cada ficheiro e a respetiva assinatura. |

Com o Raspberry Pi Imager 2, também pode abrir [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.9.3/warda.rpi-imager-manifest): o Imager configura então o Wi-Fi, o utilizador e o SSH antes de gravar o cartão.

Em Debian ou Ubuntu, num terminal:

```sh
sudo apt install ./warda_0.9.3_amd64.deb
```

Em Fedora, RHEL, Rocky Linux ou AlmaLinux, num terminal:

```sh
sudo dnf install ./warda-0.9.3-1.x86_64.rpm
```

O pacote abre no firewalld as portas de que o Warda precisa (serviço `warda`).

<a name="docker"></a>

## Instalar com Docker

Num Raspberry Pi 4 ou mais recente com um sistema de 64 bits, ou num servidor, numa pasta vazia:

```sh
curl -fsSLO https://github.com/warda-dns/Releases/releases/latest/download/docker-compose.yml
docker compose up -d
```

O mesmo ficheiro está também na raiz deste repositório, [`docker-compose.yml`](docker-compose.yml): sempre o da versão mais recente.

O Warda usa diretamente a rede da máquina: as portas 53 (DNS), 80 e 443 (interface web) têm de estar livres. Se um proxy inverso como o Traefik já usa as portas 80 e 443, defina `WARDA_HTTP_LISTEN: ":8080"` e `WARDA_HTTPS_LISTEN: ":8443"` no ficheiro antes de iniciar o Warda. Se o systemd-resolved ocupa a porta 53, o ficheiro explica como a libertar.

Depois abra `http://<endereço da máquina>` no seu navegador (seguido de `:8080` se mudou a porta) e siga o assistente. `docker logs warda` indica o endereço exato e a definição a alterar quando uma porta já está em uso.

Para atualizar, escreva a nova versão na linha `image:` do ficheiro e depois execute `docker compose pull && docker compose up -d`.

## Verificar a sua transferência

`SHA256SUMS` lista a soma de verificação de cada ficheiro de uma versão, e `SHA256SUMS.sig` é a sua assinatura Ed25519, feita com a chave de publicação do Warda. Transfira ambos para junto do seu ficheiro e, depois:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Guarde a chave pública abaixo como `warda-release.pub` (o segundo comando requer o OpenSSL 3 ou posterior). A mesma chave está integrada no Warda: uma caixa só instala as versões assinadas com ela.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Instalar

A documentação guia-o passo a passo, para Raspberry Pi, Docker, Debian, Ubuntu, Fedora e RHEL: **[docs.warda-dns.com](https://docs.warda-dns.com/pt/)**. Quando o Warda estiver a funcionar, abra-o no seu navegador e siga o assistente.

## Atualizações

Uma caixa já instalada atualiza-se sozinha a partir deste repositório: não há nada para transferir à mão. Procura uma nova versão a cada 6 horas e instala-a durante a noite quando as atualizações automáticas estão ativadas. Só é aceite uma versão assinada com a chave de publicação, e a anterior é reposta se a nova não arrancar. Com o Docker, a nova versão é anunciada na interface.

## Segurança

Encontrou uma vulnerabilidade? Escreva para [contact@warda-dns.com](mailto:contact@warda-dns.com) em vez de abrir um pedido público ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Ligações

- Site: [warda-dns.com](https://warda-dns.com/pt/)
- Documentação: [docs.warda-dns.com](https://docs.warda-dns.com/pt/)
- Área de cliente: [account.warda-dns.com](https://account.warda-dns.com/)
- Suporte: em breve

## Licença

Warda é software livre sob a licença AGPLv3. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
