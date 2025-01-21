---
id: Malicious packet sniffing
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Apa itu Packet Sniffing?

- **Definisi:**
  - Praktik menggunakan perangkat lunak atau perangkat keras untuk mengamati dan menganalisis data yang bergerak di jaringan.
- **Komponen Data yang Diamati:**
  - **Header:** Berisi alamat IP pengirim dan penerima.
  - **Body:** Dapat memuat informasi sensitif, seperti nama, tanggal lahir, pesan pribadi, informasi keuangan, dan nomor kartu kredit.
- **Tujuan:**
  - **Analis Keamanan:** Menggunakan packet sniffing untuk menyelidiki insiden atau debugging jaringan.
  - **Aktor Jahat:** Memata-matai atau memanipulasi data untuk keuntungan pribadi.

## Tipe Serangan Packet Sniffing

1. **Passive Packet Sniffing:**

   - **Definisi:** Data dibaca selama transit tanpa mengubahnya.
   - **Contoh:** Seperti kurir surat yang membaca isi surat tanpa sepengetahuan pengirim atau penerima.
   - **Tipe Serangan:**
     - Memantau semua lalu lintas di jaringan untuk mencuri informasi.

2. **Active Packet Sniffing:**
   - **Definisi:** Data dimanipulasi selama transit.
   - **Contoh:** Seperti tetangga yang mengaku akan mengantarkan surat, tetapi membaca atau mengubah isi surat sebelum menyerahkannya.
   - **Tipe Serangan:**
     - Mengarahkan paket ke port yang tidak dimaksudkan.
     - Mengubah informasi di dalam paket (misalnya, mengganti nomor rekening bank penerima).

## Cara Mencegah Packet Sniffing

1. **Menggunakan VPN:**

   - **Manfaat:**
     - Mengenskripsi data saat melintas di jaringan, sehingga meskipun lalu lintas terganggu, data tetap tidak dapat dibaca.
   - **Penerapan:**
     - Gunakan layanan VPN terpercaya saat terhubung ke jaringan yang tidak aman.

2. **Menggunakan HTTPS:**

   - **Manfaat:**
     - Memastikan bahwa data antara browser dan server terenkripsi menggunakan **SSL/TLS**.
   - **Tanda:**
     - URL memiliki **“https://”** di awal alamat domain.

3. **Hindari WiFi Publik Tanpa Perlindungan:**
   - **Risiko:**
     - Jaringan tanpa enkripsi (seperti di kafe atau bandara) memungkinkan siapa pun di jaringan yang sama mengakses data Anda.
   - **Solusi:**
     - Jangan gunakan WiFi publik tanpa VPN.

## Kesimpulan

- **Bahaya Packet Sniffing:**
  - Dapat menyebabkan pencurian data sensitif atau manipulasi data.
- **Langkah Perlindungan:**
  - Enkripsi data melalui VPN atau HTTPS.
  - Hindari jaringan WiFi publik yang tidak aman.
