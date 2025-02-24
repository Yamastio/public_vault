---
id: setup firewall dan rules di pfsense
aliases: []
tags:
  - pfSense
  - Firewall
  - Router
  - VirtualBox
author: Nama Anda
categories:
  - Jaringan Komputer
  - Keamanan Siber
date: "2023-10-15"
title: Setup firewall dan rules di pfsense
---

## Misi

1. Membatasi jaringan router kita(172.16.1.0/16) agar tidak bisa ping ke 8.8.8.8, tapi mengizinkan lalu lintas dari icmp lainya masuk dan keluar

## Praktik

### Verifikasi Virtual Machine Environment

1. Verifikasi pfsense memiliki dua interface, satu bridge adapter, satunya internal network
2. Start pfsense machine, start juga kali linux machine, begitu juga di ubuntu(pastikan network sudah diatur ke internal network dan allow Vms)
3. Verifikasi koneksi internet, di kali linux dan ubuntu juga
4. Cek dengan `ping 8.8.8.8` dan `ip addr`

### Selesaikan installasi pfsense

1. Buka ubuntu dan pergi ke browser firefox, kunjungi https://172.16.1.1 yang merupakan IP dari LAN pfsense machine kita
2. Login dengan username `admin` dan password `pfsense`
3. Klik next, next, lalu atur primary DNS server ke `8.8.8.8`, next, next, lalu next lagi
4. Ubah password Admin, jangan gunakan password default
5. Reload web nya, lalu klik `check for updates`
6. Lalu ke menu system, lalu logout, login kembali untuk cek apakah password sudah benar
7. Accept copyright, lalu pilih close
8. Dan Instalasi pfsense berhasil

### Konfigurasi pfsense untuk block ICMP

1. Pilih menu `Firewall` lalu ke `Rules`
2. Klik `Add Rule`
3. Action: `Block`
4. Interface: LAN
5. Address Family: IPv4
6. Protocol: ICMP
7. Source: `Any`
8. Destination: `address alias` > 8.8.8.8
9. Enable log packets
10. Deskripsi: `No more ping to Google's DNS`
11. Klik Apply Changes
