---
id: Scanless
aliases: []
tags: []
---

## Deskripsi

What: Linux tool untuk network reconnaisance via external services
Who: Linux User & admin yang membutuhkan network reconnaissance
When: Ketika membutuhkan network info tanpa scan seecara langsung
Where: Linux terminal
Why: Mengelola privasi, mengurangi resiko deteksi di network reconnaisance
How: Menggunakan external service untuk scan target, masking identitas

## Praktik

### Install

1. Buka terminal
2. `sudo apt update`
3. `sudo apt install python3-pip`
4. `sudo pip install scanless`
5. `scanless -h`

### Observasi opsi dan kegunaan

1. -h, --help
2. -v, --version
3. scanless [-t TARGET] [-s SCANNER] [-l] [-a]
4. -t TARGET, --target: IP atau domain yang akan di scan
5. -s SCANNER, --scanner: scanner yang akan digunakan, default: youegetsignal
6. -r, --random: menggunakan random scanner
7. -l, --list: list scanner
8. -a, --all: menggunakan semua scanner
9. -d, --debug: menggunakan debug mode(cli mode off & melihatkan network error)

### List semuia proxy scanner

`scanless -l`

| Scanner Name  | Website                               |
| ------------- | ------------------------------------- |
| ipfingerprint | https://ipfingerprint.com/            |
| pingeu        | https://pingeu.eu/                    |
| spiderip      | https://spiderip.com/                 |
| standingtech  | https://portscanner.standingtech.com/ |
| viewdns       | https://viewdns.info/                 |
| youegetsignal | https://www.yougetsignal.com/         |

### Scan target

1. `scanless -t scanme.org`, secara default akan menggunakan `youegetsignal`
2. `scanless -t scanme.org -s viewdns`
3. `scanless -t scanme.org -r`(--random scanner)
4. `scanless -t scanme.org -a`(--all scanner)
5. `scanless -t scanme.org -a > anonymous.txt`

### Getting Help

1. https://pypi.org/project/scanless/
2. `scanless --help`
