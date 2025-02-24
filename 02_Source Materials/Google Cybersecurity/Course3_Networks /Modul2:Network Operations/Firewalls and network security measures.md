---
id: Firewalls and network security measures
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Definisi Firewall

- Firewall adalah perangkat keamanan jaringan yang memantau lalu lintas data masuk dan keluar jaringan.
- Firewall memungkinkan atau memblokir lalu lintas berdasarkan aturan keamanan yang telah ditentukan.
- **Fitur utama**:
  - Port Filtering: Membatasi komunikasi berdasarkan nomor port tertentu (contoh: hanya mengizinkan port 443 untuk HTTPS).

## Jenis-Jenis Firewall

1. **Hardware Firewall**

   - Perangkat fisik yang memeriksa setiap paket data sebelum masuk ke jaringan.
   - Cocok untuk melindungi jaringan secara keseluruhan.

2. **Software Firewall**

   - Program perangkat lunak yang diinstal pada komputer atau server.
   - Melindungi perangkat atau server tertentu.
   - **Kelebihan**: Biaya lebih rendah dibandingkan hardware firewall dan tidak memerlukan ruang fisik.
   - **Kekurangan**: Membebani pemrosesan perangkat yang menjalankannya.

3. **Cloud-Based Firewall (Firewall-as-a-Service/FaaS)**

   - Dikelola oleh penyedia layanan cloud.
   - Mengatur aturan firewall melalui antarmuka cloud.
   - **Fungsi**:
     - Melindungi lalu lintas masuk sebelum mencapai jaringan organisasi.
     - Melindungi aset dan proses yang berjalan di cloud.

---

## Klasifikasi Firewall: Stateless vs Stateful

1. **Stateless Firewall**

   - Bekerja berdasarkan aturan yang telah dikonfigurasi sebelumnya.
   - Tidak menyimpan informasi tentang paket data yang dianalisis.
   - **Kekurangan**: Kurang aman dibandingkan stateful firewall karena tidak mendeteksi tren mencurigakan.

2. **Stateful Firewall**

   - Menyimpan informasi tentang lalu lintas jaringan untuk memfilter ancaman secara proaktif.
   - **Keunggulan**: Menganalisis karakteristik dan perilaku lalu lintas untuk mendeteksi ancaman.

---

## Next-Generation Firewall (NGFW)

- Memberikan inspeksi lebih mendalam dibandingkan stateful firewall:
  - **Deep Packet Inspection**: Menganalisis isi data dalam paket.
  - **Intrusion Protection**: Melindungi dari ancaman masuk.
- Terhubung ke layanan intelijen ancaman berbasis cloud untuk memperbarui perlindungan terhadap ancaman baru.

---

## Poin Penting

- Firewall dapat berupa perangkat keras, perangkat lunak, atau berbasis cloud.
- **Stateful firewall** lebih aman dibandingkan stateless firewall.
- **Next-Generation Firewall (NGFW)** menawarkan keamanan tambahan dengan fitur canggih seperti deep packet inspection dan integrasi intelijen ancaman.
