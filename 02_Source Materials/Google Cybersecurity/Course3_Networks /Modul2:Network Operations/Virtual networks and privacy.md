---
id: Virtual networks and privacy
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Kategori Utama Protokol Jaringan

1. **Protokol Komunikasi**

   - Menghubungkan server dan perangkat.
   - Contoh: TCP, UDP, SMTP (untuk email).

2. **Protokol Manajemen**

   - Memecahkan masalah jaringan.
   - Contoh: ICMP.

3. **Protokol Keamanan**
   - Mengenkripsi data dalam transit.
   - Contoh: IPSec, SSL/TLS.

Protokol lain:

- **HTTP**: Komunikasi browser dan server.
- **DNS**: Menerjemahkan nama host ke IP.
- **ARP**: Memetakan IP ke MAC Address.

## Keamanan Wi-Fi

- **Protokol Keamanan Wi-Fi**: WEP, WPA, WPA2, dan WPA3.
- **WPA3**:
  - Menggunakan AES untuk enkripsi data.
  - Mode **Personal** untuk jaringan rumah dan **Enterprise** untuk bisnis.

## Alat dan Praktik Keamanan Jaringan

1. **Firewall**

   - Melindungi jaringan pribadi dengan memfilter lalu lintas berdasarkan aturan tertentu.
   - **Jenis-jenis Firewall**:
     - **Stateless**: Hanya berdasarkan aturan yang ditentukan.
     - **Stateful**: Melacak informasi koneksi, lebih efisien.
   - **Next-Generation Firewall (NGFW)**:
     - Inspeksi data mendalam (deep packet inspection).
     - Fitur tambahan: Malware sandboxing, Network Anti-Virus, URL/DNS filtering.

2. **Proxy Server**

   - Menambahkan keamanan dengan **Network Address Translation (NAT)**.
   - **Forward Proxy**: Mengelola permintaan internal ke sumber eksternal.
   - **Reverse Proxy**: Mengelola permintaan eksternal ke sumber internal.
   - Bisa dikonfigurasi seperti firewall untuk memblokir situs berbahaya.

3. **Virtual Private Network (VPN)**
   - Mengenkripsi data dalam transit dan menyembunyikan IP.
   - **Proses Encapsulation**: Membungkus data dalam paket terenkripsi.
   - Digunakan untuk melindungi komunikasi ke sumber daya internal perusahaan (server, aplikasi bisnis).
   - Kombinasi VPN dan **SD-WAN**:
     - SD-WAN: Jaringan virtual untuk menghubungkan lokasi secara aman di wilayah geografis luas.

## Poin Penting

- Protokol jaringan dibagi menjadi komunikasi, manajemen, dan keamanan.
- Alat keamanan seperti firewall, proxy server, dan VPN membantu menjaga privasi dan integritas data.
- Organisasi semakin mengadopsi pendekatan berbasis cloud dengan kombinasi VPN dan SD-WAN.
