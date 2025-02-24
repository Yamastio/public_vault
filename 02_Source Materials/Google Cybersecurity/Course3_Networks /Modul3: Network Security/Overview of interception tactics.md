---
id: Overview of interception tactics
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Pengantar Serangan Intersepsi

- **Definisi:**
  - Serangan yang melibatkan penyadapan data yang bergerak di jaringan, seperti **packet sniffing** dan **IP spoofing**.
- **Tujuan:**
  - Mencuri data, menyamar sebagai pengguna sah, atau menyebabkan gangguan layanan.

## Tinjauan Packet Sniffing

1. **Apa itu Packet Sniffing?**

   - Praktik menangkap dan menganalisis paket data yang melewati jaringan.
   - Pada operasi normal, perangkat hanya memproses paket yang ditujukan ke alamat MAC-nya.

2. **Promiscuous Mode pada NIC:**

   - NIC dapat diatur untuk menerima semua lalu lintas jaringan, termasuk yang tidak ditujukan padanya.
   - Alat seperti **Wireshark** sering digunakan untuk menyimpan data yang disadap.

3. **Risiko:**
   - Data sensitif (seperti IP dan alamat MAC) dapat dimanfaatkan untuk melakukan **IP spoofing** atau serangan lainnya.

## Jenis Serangan IP Spoofing

1. **On-Path Attack (Man-in-the-Middle):**

   - **Definisi:**
     - Penyerang menyusup di antara dua perangkat yang saling percaya untuk menyadap atau memanipulasi data.
   - **Risiko:**
     - Mengakses informasi sensitif seperti username dan password.
     - Memanipulasi lookup DNS untuk mengarahkan ke IP berbahaya.
   - **Perlindungan:**
     - Enkripsi data menggunakan **TLS**.

2. **Smurf Attack:**

   - **Definisi:**
     - Gabungan **IP spoofing** dan serangan DoS yang membanjiri jaringan dengan lalu lintas tidak diinginkan.
   - **Cara Kerja:**
     - Penyerang mengirimkan paket ICMP ping yang dipalsukan ke alamat broadcast, menyebabkan perangkat di jaringan mengirimkan balasan massal.
   - **Perlindungan:**
     - Gunakan **Next Generation Firewall (NGFW)** untuk mendeteksi lalu lintas anomali.

3. **Denial of Service (DoS):**
   - **Definisi:**
     - Serangan yang mencegah sistem berfungsi dengan membanjiri jaringan dengan IP palsu atau lalu lintas yang tidak sah.
   - **Risiko:**
     - Server menjadi tidak responsif atau crash.
   - **Perlindungan:**
     - Terapkan **Defense-in-Depth** dengan berbagai strategi seperti enkripsi dan firewall.

## Strategi Mitigasi Serangan Intersepsi

1. **Enkripsi Data:**
   - Pastikan semua data yang bergerak dienkripsi untuk mencegah akses tidak sah.
2. **Firewall Lanjutan:**
   - Gunakan firewall dengan kemampuan mendeteksi lalu lintas anomali dan membatasi penyalahgunaan.
3. **Pemantauan Jaringan:**
   - Identifikasi pola lalu lintas mencurigakan dengan alat pemantauan jaringan.
4. **Prinsip Defense-in-Depth:**
   - Gabungkan berbagai metode pertahanan untuk melindungi dari berbagai jenis serangan.

## Kesimpulan

- **Tantangan:**
  - Serangan seperti packet sniffing, IP spoofing, on-path attack, smurf attack, dan DoS memanfaatkan kelemahan jaringan.
- **Solusi:**
  - Terapkan lapisan keamanan seperti enkripsi, firewall, dan pemantauan untuk memitigasi risiko.
- **Pentingnya Analisis:**
  - Keamanan jaringan memerlukan pemahaman menyeluruh untuk memastikan mitigasi berhasil.
