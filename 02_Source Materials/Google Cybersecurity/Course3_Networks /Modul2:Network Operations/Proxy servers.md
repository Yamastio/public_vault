---
id: Proxy servers
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Apa Itu Proxy Server?

- **Proxy server** adalah server yang memenuhi permintaan klien dengan meneruskan permintaan tersebut ke server lain.
- Proxy server bertindak sebagai perantara antara internet dan jaringan internal.
- Ketika permintaan untuk terhubung ke jaringan datang dari internet, proxy server akan memeriksa apakah permintaan tersebut aman.

## Fungsi Proxy Server dalam Keamanan Jaringan

- **Menyembunyikan Alamat IP Privat**: Proxy server menggunakan alamat IP publik yang berbeda dari jaringan privat, menyembunyikan alamat IP asli jaringan internal dan menambah lapisan keamanan.
- **Blokir Website Berbahaya**: Proxy server bisa digunakan untuk memblokir situs web yang tidak aman dan tidak boleh diakses oleh pengguna jaringan.
- **Meningkatkan Efisiensi**: Proxy server menyimpan data yang sering diminta dalam **memory sementara** untuk mengurangi kebutuhan akses langsung ke server internal, meningkatkan keamanan dengan mengurangi interaksi langsung.

## Jenis-jenis Proxy Server

1. **Forward Proxy Server**

   - Mengatur dan membatasi akses pengguna ke internet.
   - Menyembunyikan alamat IP pengguna dan menyetujui semua permintaan keluar.
   - Dalam organisasi, proxy ini menerima lalu lintas keluar dari karyawan, menyetujui, dan meneruskannya ke tujuan di internet.

2. **Reverse Proxy Server**

   - Mengatur dan membatasi akses ke server internal dari internet.
   - Menerima lalu lintas dari pihak eksternal, menyetujui, dan meneruskannya ke server internal.
   - Berguna untuk melindungi server web internal yang mengandung data sensitif agar tidak mengekspos alamat IP mereka ke pihak luar.

3. **Email Proxy Server**
   - Memfilter email spam dengan memverifikasi apakah alamat pengirim palsu.
   - Mengurangi risiko serangan phishing yang meniru orang yang dikenal di organisasi.
   - Sebagai contoh, proxy server dapat digunakan untuk menyaring spam dengan beberapa lapisan filtrasi sebelum email diterima, seperti yang dilakukan oleh ISP besar di masa lalu.

### **Keamanan Tambahan dengan Proxy Server**

- Proxy server memainkan peran penting dalam **menyaring lalu lintas masuk dan keluar** serta **mendeteksi serangan jaringan**.
- Mereka menambahkan lapisan perlindungan dari **jaringan publik yang tidak aman** (internet), sehingga meningkatkan keamanan jaringan internal.
