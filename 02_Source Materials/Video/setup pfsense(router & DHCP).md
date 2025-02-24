---
id: setup pfSense(router & dhcp)
aliases: []
tags: []
---

tags: [[hacking_fundamentals]]

## Description

What: Open Source Firewall dan router
Who: Dibuat oleh netgate, pfsense.org
When: Rilis pertama 2004
Where: Di komputer atau VM dan router lalu lintas jaringan
Why: Meningkatkan network security & traffic management
How: Berdasarkan FreeBSD, GUI untuk mudah dikonfigurasikan

## Practice

### Download pfsense dan konfigurasi di Virtual Box

1. Kunjungi web pfsense.org
2. Download pfsense for your OS, pastikan download file ISO, karena kita akan install di Virtual Box
3. Ekstrak file sehingga akan muncul file .iso
4. Klik new di VM, pilih ISO nya lalu set Processor minimal 1 gb dan hard drive 16 gb, 1 core cpu sudah cukup
5. Klik finish
6. Pergi ke setting, lalu pilih network, ubah adapter 1 dari NAT ke Bridge, adapter 1 ini akan menjadi WAN kita
7. Enable adapter 2, yang akan menjadi LAN kita nantinya, ubah dari NAT ke Internal Network, lalu aktifkan `Promiscuous Mode` ke `Allow VMs`
8. Klik Ok, lalu start

### Install pfsense

1. Setelah boot, tekan enter untuk `accept` copyright
2. Akan muncul Menu welcome, pilih `install pfsense`
3. Ketika muncul network installation, klik `OK`. Pastikan pilih adapter 1, yang jadi WAN kita yang bisa connect ke internet
4. Ingat hanya atur WAN saja, biasanya namanya `vtnet0`, lalu pilih continue
5. Untuk LAN kita skip, lalu pilih continue
6. Pilih `install CE`
7. Pilih Ok, Yes, Ok, dan proses install selesai, nanti akan muncul popup install sukses, dan pilih reboot

### Setelah sukses install

1. Setelah reboot akan balik lagi ke menu install, ini karena kita belum copot bootable OS nya
2. Pergi ke virtual box, pilih setting di machine pfsense, lalu pilih storage, lalu remove file ISO nya
3. Powef OFF lalu start lagi, pfsense sudah berhasil di install

### Konfigurasi Network Interface

1. Setelah start pfsense machine, akan terlihat IP address dari WAN dan LAN kita
2. Pilih menu 2, untuk `Set interface IP address`
3. Pilih 2 lagi, untuk konfigurasi LAN pilih statis di em1
4. Tulis `n`, untuk konfigurasi IPv4 address interface lewat DHCP
5. Masukan ip: 172.16.1.1 dan tekan enter
6. Masukan 16 untuk Class B subnet mask
7. Enter, kita tidak akan konfigurasi WAN IPv4 address nya
8. Tulis `n` lalu enter, kita tidak akan konfigurasi LAN interface vai DHCPv6
9. Enter(Kita tidak akan konfigurasi LAN IPv6 address)
10. Tulis `y`, kita akan enable DHCP server di LAN kita
11. Masukan 172.16.1.100 untuk start IP Address dan enter lagi
12. Tulis 172.16.1.200 untuk end dari IP Address lalu enter
13. Tulis `n` lalu enter, kita tidk akan revert ke http, kita akan gunakan https
14. Enter untuk continue
15. IP berhasil diubah, bisa cek dengan pilih menui 7, lalu masukan DNS google, `8.8.8.8`
16. Pastikan ping request berjalan dengan baik

### Verifikasi di machine yang lain

1. Buka virtual box, pastikan pfsense machine sudah aktif
2. Buka setting, lalu pilih network, ubah adapter 1 dari NAT ke Internal Network, aktifkan juga `Promiscuous Mode` ke `Allow VMs`
3. Klik Ok, lalu start
4. Buka terminal di kali linux atau OS yang disetting ke Internal Network tadi, lalu cek ip addressnya
5. Pastikan IP addressnya sama dengan yang di set di pfsense di rentang 100 sampai 200
6. `ip addr show`, akan terlihat IP Addressnya jika dhcp berhasil maka ip akan ada direntang 172.16.1.100/200
7. Coba ping ke pfsense kita, ip nya tadi 127.16.1.1, pastikan ping berjalan
8. Coba ping ke dns google, 8.8.8.8, pastikan ping berjalan juga
9. Jika semua berjalan, bisa dipastikan setup pfsense router dan dhcp berhasil

- 10. Untuk mematikan dhcp service bisa masukan command `dhclient -r`, untuk menghidupkan kembali `dhclient`.

### Enable DNS

1. Beberapa ISP atau jaringan upstream tidak mendukung DNSSSEC(Domain Name System Security Extensions), yang menyebabkan tidak bisa melakukan `ping google.com` atau domain lainya
2. Silakan Bisa Matikan Enable DNSSEC di Services > DNS Resolver, matikan centang pada opsi `Enable DNSSEC Support`
3. Aktifkan juga opsi `Enable Forwarding Mode`
4. Klik save dan Apply
