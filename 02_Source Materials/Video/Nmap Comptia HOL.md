---
id: Nmap Comptia HOL
aliases: []
tags: []
---

## Deskripsi

What: Network scanner di linux untuk scanning
Who: Admin, security analyst, penetration tester
When: Selama audit keamanan, troubelshooting, penetration testing
Where: Linux terminal
Why: Identifikasi host, port, vulnerability
How: Enter nmap diikuti dengan target IP/host

## Praktik

1. Install nmap, `sudo apt install nmap`
2. Scan target yang diperbolehkan yaitu, `nmap scanme.org`, tekan panah atas di keyboard untuk melihat progressnya
3. Secara default, nmap akan scan 1000 port
4. Observasi output:

   - Host Status
   - Reverse DNS
   - not shown closed ports
   - port and services

5. Cek di https://www.speedguide.net/ports.php, untuk melihat semua port dan services nya
6. Cheat sheet nmap: https://stationx.net/nmap-cheat-sheet/

### Spesifik port tertentu

`nmap scanme.org -p 22`

### TCP scan

Secara default, akan TCP scan top 1000 port
`nmap scanme.org -p 1-1000`

### UDP Scan

`nmap 172.16.1.1 -sU`

### Service dan Version Detection

`nmap 172.16.1.1 -sV`

### Output Save

1. `nmap 172.16.1.1 -oN output.txt`
2. `nmap 172.16.1.1 > result.txt`, tapi tidak bisa arrow up untuk cek progress

### Ping scan

`nmap scanme.org -sn`

### Script Egnine:

Menggunakan NSE(Nmap Scripting Engine) untik advandce scanning dan automation

1. `nmap 172.16.1.1 --script=banner`, banner grabbing
2. `nmap 172.16.1.1 --script=http,banner`

### Timing and Perform

Nmap dianggap sebagai scanner yang banyak meninggalkan jejak, terlalu berisik, jadi ketika kita scan akan ada jejak yang tertinggal, apalagi jika ada IPS/IDS. Ada opsi -T, diikuti range tertentu dari 0-5, paranoid ke insane, setiap range berefek pada waktu dan agresivitas scan

`nmap scanme.org -T0`

### Help

`nmap --help`
`man nmap`
