<div align="center">

<img src="https://warda-dns.com/assets/apple-touch-icon.png" alt="Warda" width="96" height="96">

# Warda

**Το φίλτρο DNS που μαθαίνει το σπίτι σας**

[![έκδοση](https://img.shields.io/github/v/release/warda-dns/Releases?label=%CE%AD%CE%BA%CE%B4%CE%BF%CF%83%CE%B7&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![κυκλοφόρησε](https://img.shields.io/github/release-date/warda-dns/Releases?label=%CE%BA%CF%85%CE%BA%CE%BB%CE%BF%CF%86%CF%8C%CF%81%CE%B7%CF%83%CE%B5&color=6E46B7)](https://github.com/warda-dns/Releases/releases/latest)
[![λήψεις](https://img.shields.io/github/downloads/warda-dns/Releases/total?label=%CE%BB%CE%AE%CF%88%CE%B5%CE%B9%CF%82&color=6E46B7)](https://github.com/warda-dns/Releases/releases)
[![άδεια](https://img.shields.io/badge/%CE%AC%CE%B4%CE%B5%CE%B9%CE%B1-AGPL--3.0-6E46B7)](https://www.gnu.org/licenses/agpl-3.0.html)

[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-arm64-C51A4A?logo=raspberrypi&logoColor=white)](#download)
[![Debian · Ubuntu](https://img.shields.io/badge/Debian%20%C2%B7%20Ubuntu-amd64%20%C2%B7%20arm64-A81D33?logo=debian&logoColor=white)](#download)
[![Docker](https://img.shields.io/badge/Docker-amd64%20%C2%B7%20arm64-2496ED?logo=docker&logoColor=white)](#download)
[![ιστότοπος](https://img.shields.io/badge/%CE%B9%CF%83%CF%84%CF%8C%CF%84%CE%BF%CF%80%CE%BF%CF%82-warda--dns.com-6E46B7)](https://warda-dns.com/el/)
[![τεκμηρίωση](https://img.shields.io/badge/%CF%84%CE%B5%CE%BA%CE%BC%CE%B7%CF%81%CE%AF%CF%89%CF%83%CE%B7-docs.warda--dns.com-6E46B7)](https://docs.warda-dns.com/en/)

[English](README.md) · [Français](README.fr.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Nederlands](README.nl.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [Polski](README.pl.md) · [Română](README.ro.md) · [Čeština](README.cs.md) · [Magyar](README.hu.md) · **Ελληνικά**

</div>

## Τι είναι το Warda;

Το Warda μπλοκάρει τις διαφημίσεις, την παρακολούθηση και τους επικίνδυνους ιστότοπους σε κάθε συσκευή του σπιτιού σας — κινητά, υπολογιστές, τηλεόραση, κονσόλες παιχνιδιών — και μαθαίνει τι πραγματικά χρειάζεται η οικογένειά σας, χωρίς να χρειάζεται να διαχειρίζεστε λίστες μόνοι σας: απλώς ενεργοποιείτε τις προστασίες που θέλετε. Το Warda παρατηρεί τα ερωτήματα του δικτύου σας και προτείνει τι να μπλοκάρετε, με το πλαίσιό του: ποια συσκευή, αμέσως μετά από τι. Δεν μπλοκάρει ποτέ τίποτα από μόνο του. Ό,τι μαθαίνει μένει στο σπίτι σας, στον δικό σας εξοπλισμό.

<a name="download"></a>

## Λήψη

Τελευταία έκδοση: **0.7.13** · [σημειώσεις έκδοσης](https://github.com/warda-dns/Releases/releases/tag/v0.7.13) · [όλες οι εκδόσεις](https://github.com/warda-dns/Releases/releases)

| Για εγκατάσταση του Warda σε | Αρχείο | Τι είναι |
|---|---|---|
| **Raspberry Pi 4 ή νεότερο** | [`warda_0.7.13_raspberrypi-arm64.img.xz`](https://github.com/warda-dns/Releases/releases/download/v0.7.13/warda_0.7.13_raspberrypi-arm64.img.xz) | Έτοιμη εικόνα για κάρτα microSD 16 GB ή μεγαλύτερη, που γράφεται με το Raspberry Pi Imager. |
| **Debian και Ubuntu**<br>amd64 · arm64 | [`warda_0.7.13_amd64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.13/warda_0.7.13_amd64.deb)<br>[`warda_0.7.13_arm64.deb`](https://github.com/warda-dns/Releases/releases/download/v0.7.13/warda_0.7.13_arm64.deb) | Ένα πακέτο Debian για εικονική μηχανή ή αποκλειστικό διακομιστή. |
| **Άλλο Linux**<br>amd64 · arm64 | [`warda_0.7.13_linux_amd64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.13/warda_0.7.13_linux_amd64.tar.gz)<br>[`warda_0.7.13_linux_arm64.tar.gz`](https://github.com/warda-dns/Releases/releases/download/v0.7.13/warda_0.7.13_linux_arm64.tar.gz) | Ένα συμπιεσμένο αρχείο μόνο με το πρόγραμμα. |
| **Docker**<br>amd64 · arm64 | `ghcr.io/warda-dns/warda:0.7.13`<br>Δείτε την [τεκμηρίωση](https://docs.warda-dns.com/en/) | Ένα container, για διακομιστή ή NAS που ήδη τρέχει Docker. |
| **Όλες οι εγκαταστάσεις** | [`SHA256SUMS`](https://github.com/warda-dns/Releases/releases/download/v0.7.13/SHA256SUMS)<br>[`SHA256SUMS.sig`](https://github.com/warda-dns/Releases/releases/download/v0.7.13/SHA256SUMS.sig) | Τα checksums κάθε αρχείου και η υπογραφή τους. |

Με το Raspberry Pi Imager 2 μπορείτε επίσης να ανοίξετε το [`warda.rpi-imager-manifest`](https://github.com/warda-dns/Releases/releases/download/v0.7.13/warda.rpi-imager-manifest): το Imager ρυθμίζει τότε το Wi-Fi, τον χρήστη και το SSH πριν γράψει την κάρτα.

Σε Debian ή Ubuntu, σε ένα τερματικό:

```sh
sudo apt install ./warda_0.7.13_amd64.deb
```

Με Docker, σε ένα τερματικό:

```sh
docker pull ghcr.io/warda-dns/warda:0.7.13
```

## Επαληθεύστε τη λήψη σας

Το `SHA256SUMS` περιέχει το checksum κάθε αρχείου μιας έκδοσης, και το `SHA256SUMS.sig` είναι η υπογραφή του Ed25519, που έγινε με το κλειδί δημοσίευσης του Warda. Κατεβάστε και τα δύο δίπλα στο αρχείο σας και, στη συνέχεια:

```sh
sha256sum --check --ignore-missing SHA256SUMS
openssl pkeyutl -verify -pubin -inkey warda-release.pub -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

Αποθηκεύστε το παρακάτω δημόσιο κλειδί ως `warda-release.pub` (η δεύτερη εντολή απαιτεί OpenSSL 3 ή νεότερο). Το ίδιο κλειδί είναι ενσωματωμένο στο Warda: ένα κουτί εγκαθιστά μόνο τις εκδόσεις που έχουν υπογραφεί με αυτό.

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAnDKR0w4ktuxZVIezyPwGx8EMLfZhgf21R5P4efLjMXY=
-----END PUBLIC KEY-----
```

## Εγκατάσταση

Η τεκμηρίωση σας καθοδηγεί βήμα προς βήμα, για Raspberry Pi, Docker, Debian και Ubuntu: **[docs.warda-dns.com](https://docs.warda-dns.com/en/)**. Μόλις το Warda ξεκινήσει, ανοίξτε το στον περιηγητή σας και ακολουθήστε τον οδηγό.

## Ενημερώσεις

Ένα κουτί που είναι ήδη εγκατεστημένο ενημερώνεται μόνο του από αυτό το αποθετήριο: δεν χρειάζεται να κατεβάσετε τίποτα με το χέρι. Αναζητά νέα έκδοση κάθε 6 ώρες και την εγκαθιστά τη νύχτα, όταν οι αυτόματες ενημερώσεις είναι ενεργές. Γίνεται δεκτή μόνο έκδοση υπογεγραμμένη με το κλειδί δημοσίευσης, και η προηγούμενη επαναφέρεται αν η νέα δεν ξεκινήσει. Με το Docker, η νέα έκδοση ανακοινώνεται στο περιβάλλον διαχείρισης.

## Ασφάλεια

Βρήκατε κάποια ευπάθεια; Γράψτε στο [contact@warda-dns.com](mailto:contact@warda-dns.com) αντί να ανοίξετε δημόσια αναφορά ([security.txt](https://warda-dns.com/.well-known/security.txt)).

## Σύνδεσμοι

- Ιστότοπος: [warda-dns.com](https://warda-dns.com/el/)
- Τεκμηρίωση: [docs.warda-dns.com](https://docs.warda-dns.com/en/)
- Περιοχή πελάτη: [account.warda-dns.com](https://account.warda-dns.com/)
- Υποστήριξη: σύντομα

## Άδεια χρήσης

Το Warda είναι ελεύθερο λογισμικό με άδεια AGPLv3. [GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)
