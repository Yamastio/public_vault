---
id: Security zones
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Apa Itu Security Zones?

- **Security Zones** adalah segmen jaringan yang memproteksi jaringan internal dari internet, bagian dari teknik **network segmentation** yang membagi jaringan menjadi beberapa segmen.
- Setiap segmen jaringan memiliki **izin akses** dan aturan keamanan sendiri, yang mengatur siapa yang dapat mengakses bagian tertentu dari jaringan.

## Fungsi dan Manfaat Security Zones

- **Mencegah Penyebaran Masalah**: Segmen-segmen ini mencegah masalah, seperti serangan, menyebar ke seluruh jaringan.
- **Menjaga Privasi**: Memastikan privasi di dalam kelompok perusahaan atau departemen.
- **Membatasi Akses**: Mengatur akses dan memperketat kontrol antara segmen-segmen berbeda dalam jaringan.

## Contoh Penggunaan Security Zones

- **Wi-Fi Hotel**: Wi-Fi tamu yang tidak terenkripsi dipisahkan dari jaringan staf yang terenkripsi, menjaga keamanan data.
- **Subnets pada Universitas**: Misalnya, jaringan fakultas dan jaringan siswa dipisahkan untuk mencegah kontaminasi dari satu segmen ke segmen lainnya.

## Jenis-Jenis Security Zones

1. **Uncontrolled Zone**:

   - Jaringan di luar kontrol organisasi, seperti **internet**.

2. **Controlled Zone**:
   - Subnet yang melindungi jaringan internal dari **uncontrolled zone**.
   - Ada beberapa lapisan di dalam controlled zone:
     - **DMZ (Demilitarized Zone)**:
       - Menampung layanan publik yang dapat mengakses internet, seperti web server, proxy server, DNS server, dan email server.
     - **Internal Network**:
       - Menangani server dan data pribadi organisasi.
     - **Restricted Zone**:
       - Melindungi informasi sensitif yang hanya dapat diakses oleh karyawan dengan hak istimewa tertentu.

## Diagram Keamanan

- **DMZ** ditempatkan di antara **dua firewall** untuk memfilter trafik yang masuk dan keluar, memberikan perlindungan bertingkat untuk jaringan internal.
- Jika ada **restricted zone**, maka akan dilindungi oleh **firewall tambahan** untuk mencegah akses ke data sensitif.

## Tugas Seorang Security Analysis

- **Mengelola Kebijakan Akses**:
  - Menentukan aturan akses ke DMZ dan jaringan internal, seperti membatasi akses hanya untuk trafik HTTPS ke web server di DMZ.

## Pentingnya Security Zones

- **Keamanan Jaringan**:
  - Memahami dan mengelola security zones sangat penting untuk mencegah serangan dan menjaga kerahasiaan data, terutama di organisasi besar.
