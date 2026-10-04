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
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![site](https://img.shields.io/badge/site-warda--dns.com-6E46B7)](https://warda-dns.com/pt/)
[![documentação](https://img.shields.io/badge/documenta%C3%A7%C3%A3o-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/pt/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · **Português** · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · [Ελληνικά](README.el.md)

</div>

## O que é o Warda?

O Warda bloqueia publicidade, rastreamento e sites perigosos em todos os dispositivos da sua casa — telemóveis, computadores, televisão, consolas — e aprende o que a sua família realmente precisa, sem que tenha de gerir listas por si: basta ativar as proteções que pretende. O Warda observa os pedidos da sua rede e sugere o que bloquear, com o seu contexto: qual o dispositivo, logo a seguir a quê. Nunca bloqueia por conta própria. O que aprende fica em sua casa, no seu próprio equipamento.

<a name="download"></a>

## Transferir

Última versão: **0.7.11** · [notas da versão](https://github.com/warda-dns/Releases/releases/tag/v0.7.11) · [todas as versões](https://github.com/warda-dns/Releases/releases)

| Para instalar o Warda em | Ficheiro | O que é |
|---|---|---|
| **Raspberry Pi 4 ou posterior** | [`warda_0.7.11_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_raspberrypi-arm64.img.xz) | Uma imagem pronta para um cartão microSD de 16 GB ou mais, gravada com o Raspberry Pi Imager. |
| **Debian e Ubuntu**<br>amd64 · arm64 | [`warda_0.7.11_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_amd64.deb)<br>[`warda_0.7.11_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_arm64.deb) | Um pacote Debian para uma máquina virtual ou um servidor dedicado. |
| **Outro Linux**<br>amd64 · arm64 | [`warda_0.7.11_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_linux_amd64.tar.gz)<br>[`warda_0.7.11_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda_0.7.11_linux_arm64.tar.gz) | Um arquivo apenas com o programa. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.11`<br>Consulte a [documentação](https://docs.warda-dns.com/pt/) | Um único contentor, para um servidor ou uma NAS que já corra Docker. |
| **Todas as instalações** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/SHA256SUMS.sig) | As somas de verificação de cada ficheiro e a respetiva assinatura. |

Com o Raspberry Pi Imager 2, também pode abrir [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.11/warda.rpi-imager-manifest): o Imager configura então o Wi-Fi, o utilizador e o SSH antes de gravar o cartão.

Em Debian ou Ubuntu, num terminal:

```sh
sudo apt install ./warda_0.7.11_amd64.deb
```

Com Docker, num terminal:

```sh
docker pull ghcr.io/warda-dns/warda:0.7.11
```

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

A documentação guia-o passo a passo, para Raspberry Pi, Docker, Debian e Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/pt/)**. Quando o Warda estiver a funcionar, abra-o no seu navegador e siga o assistente.

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
