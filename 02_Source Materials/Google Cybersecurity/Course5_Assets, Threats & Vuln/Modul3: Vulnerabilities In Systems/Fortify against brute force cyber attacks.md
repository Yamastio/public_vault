---
id: Fortify against brute force cyber attacks
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan: Memperkuat Perlindungan dari Serangan Brute Force

### Apa Itu Brute Force Attack?
- **Brute Force Attack** adalah proses trial-and-error untuk menebak informasi sensitif, seperti username dan password, hingga menemukan kombinasi yang benar.
- Teknik-teknik serangan brute force meliputi:
  - **Simple Brute Force**: Menebak username dan password secara manual.
  - **Dictionary Attack**: Menggunakan daftar kata sandi umum.
  - **Reverse Brute Force**: Menggunakan satu kredensial untuk mencoba masuk ke banyak sistem.
  - **Credential Stuffing**: Memanfaatkan kredensial yang dicuri dari pelanggaran data lain.
  - **Pass the Hash**: Menggunakan hash kredensial yang dicuri untuk mengelabui sistem otentikasi.

### Alat yang Sering Digunakan Penyerang
- Alat-alat otomatis digunakan untuk mempercepat proses brute force, seperti:
  - **Aircrack-ng**: Menguji keamanan jaringan Wi-Fi.
  - **Hashcat**: Memecahkan hash kata sandi.
  - **John the Ripper**, **Ophcrack**, dan **THC Hydra**.

### Strategi Pencegahan
1. **Hashing dan Salting**:
   - **Hashing**: Mengonversi data menjadi nilai unik untuk menjaga integritas.
   - **Salting**: Menambahkan karakter acak untuk memperkuat hash.
2. **Multi-Factor Authentication (MFA)**:
   - Menambah lapisan verifikasi, seperti SMS atau aplikasi otentikasi, sehingga penyerang sulit melengkapi semua tahap otentikasi.
3. **CAPTCHA**:
   - Membatasi akses bot dengan meminta pengguna membuktikan bahwa mereka manusia (contoh: memasukkan teks atau mencocokkan gambar).
4. **Kebijakan Kata Sandi**:
   - Panjang minimal 8 karakter dengan kombinasi huruf, angka, dan simbol.
   - Kebijakan penguncian setelah beberapa percobaan gagal dan pembaruan kata sandi secara berkala.
   - Mengikuti pedoman **NIST SP 800-63B** untuk standar keamanan kata sandi.

### Kesimpulan
- **Serangan brute force sederhana tetapi efektif**, terutama jika perlindungan lemah.
- Kombinasi langkah teknis seperti **hashing, MFA, dan CAPTCHA** serta kebijakan manajerial yang ketat adalah kunci untuk melindungi sistem.
- Sebagai profesional keamanan, gunakan alat serupa untuk menguji dan memperkuat keamanan sistem organisasi Anda.
