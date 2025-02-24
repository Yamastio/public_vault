---
id: Hand On Lab ARP Comptia
aliases: []
tags: []
---

## Step

1. Open Terminal
2. Ketikan `arp` atau `arp -n`
3. Ping pfSense router dan Ubuntu IP address dari kali linux

### Manual arp Request

1. `sudo arping 172.16.1.1`
2. `arp -a` untuk lihat arp cache

### Menambahkan static arp entry

1. `sudo arp -s 172.16.1.120 08:00:27:6e:13:8e`

### Menghapus arp entry

1. `sudo arp -d 172.16.1.120`

### MiTM Arp Spoofing

`sudo arpspoof -i eth0 -t 172.16.1.101 172.16.1.1 -r`

### Mencegah ARP spoofing

[ ] Static ARP Entry
[ ] ARP Spoofing Detection Software
[ ] Dynamic ARP Inspection (DAI)
[ ] Port Security

### Getting Help

[ ]`arp --help`
[ ]`man arp`
