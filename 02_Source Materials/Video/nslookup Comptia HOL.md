---
id: nslookup Comptia HOL
aliases: []
tags: []
---

## Description

What: Linux tool untuk DNS Queries
Who: Admin dan pengguna yang ingin troubleshooting network isu
Where: di CLI linux
When: Resolve domain names, and debug DNS Isu
Why: Mendiagnosa masalah jaringan, verfikasi DNS
How: run dengan `nslookup` dengan domain/ip ke queri DNS

## Praktik

nslookup ada dua mode, interaktif(lebih lengkap) dan non interaktif

1. Buka terminal

### Interaktif mode

2. Masuk ke interaktif mode, `nslookup`

   - facebook.com
   - amazon.com
   - apple.com
   - exit

3. Observasi hasil output:
   - Server: domain server di mesin kita
   - Non-Authoritative Answer
   - Name
   - Address
4. Find MX(mail exchange) record of a server:

   - nslookup
   - set q=mx
   - facebook.com

5. Find TXT(text) record of a server:
   - nslookup
   - set q=txt
   - facebook.com
6. Find NS(name server)

   - nslookup
   - set q=ns
   - facebook.com

7. Ubah DNS:
   - nslookup
   - server 1.1.1.1
   - amazon.com

### Non Interaktif Mode

8. Gunakan:
   - nslookup -type=A facebook.com
   - nslookup -type=AAAA facebook.com
   - nslookup -type=mx facebook.com
   - nslookup -type=txt facebook.com

### Debug Mode

`nslookup -debug facebook.com`

### Menggunakan mxtoolbox: https://mxtoolbox.com

    - mx
    - AAAA
    - TXT

### Getting Help

- `man nslookup`
