---
id: Brute force attacks and OS hardening
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Brute Force Attacks

- **Brute force attack** adalah metode coba-coba untuk menebak informasi pribadi, seperti kata sandi, dengan mencoba kombinasi username dan password yang mungkin.
- Jenis-jenis brute force attack:

  - **Simple brute force attack**: Menebak kombinasi login dengan memasukkan berbagai username dan password.
  - **Dictionary attack**: Menggunakan daftar kata-kata umum atau kredensial yang dicuri dari pelanggaran sebelumnya.

- Brute force attacks bisa dilakukan secara manual atau menggunakan alat otomatis. Mereka bisa sangat memakan waktu dan sumber daya, namun alat otomatis mempercepat proses ini.

## Menggunakan Virtual Machines (VMs) dan Sandbox untuk Penilaian Kerentanannya

- **Virtual Machines (VMs)**:
  - Merupakan versi perangkat keras komputer secara perangkat lunak yang digunakan untuk mengisolasi kode dan menghindari dampak buruk pada sistem utama.
  - VMs digunakan untuk menjalankan kode berisiko, seperti malware, tanpa membahayakan sistem utama.
  - Meskipun aman, ada sedikit risiko malware bisa keluar dari VM dan mengakses mesin utama.
- **Sandbox**:
  - Merupakan lingkungan pengujian yang terisolasi, baik perangkat keras fisik atau berbasis perangkat lunak/cloud, untuk menguji perangkat lunak atau mengidentifikasi kerentanannya.
  - Sandboxes berguna untuk mendeteksi bug dan kerentanannya sebelum perangkat lunak dijalankan di jaringan utama.
  - Beberapa malware dapat mendeteksi jika mereka dijalankan dalam lingkungan sandbox atau VM, mengubah perilaku mereka menjadi tidak berbahaya.

## Langkah-langkah Pencegahan untuk Menghindari Brute Force Attacks

1. **Salting dan Hashing**:

   - **Hashing** mengubah informasi menjadi nilai unik yang tidak bisa dibalik untuk mendapatkan teks asli.
   - **Salting** menambahkan karakter acak pada password yang di-hash untuk meningkatkan kompleksitas dan keamanannya.

2. **Multi-Factor Authentication (MFA) dan Two-Factor Authentication (2FA)**:

   - **MFA**: Memerlukan lebih dari satu cara verifikasi untuk mengakses sistem (misalnya, password dan sidik jari).
   - **2FA**: Menggunakan dua faktor verifikasi (misalnya, password dan OTP yang dikirimkan).

3. **CAPTCHA dan reCAPTCHA**:

   - CAPTCHA digunakan untuk memastikan bahwa pengguna adalah manusia, mencegah otomatisasi oleh bot untuk mencoba login.

4. **Kebijakan Kata Sandi**:
   - Menetapkan kebijakan kata sandi yang mengatur kompleksitas, pembaruan berkala, dan penggunaan kata sandi yang sama.

## Kesimpulan

- **Brute force attacks** adalah metode trial-and-error untuk menebak password dan dapat diluncurkan baik secara manual maupun otomatis menggunakan perangkat lunak.
- Untuk melindungi sistem dari serangan ini, dapat digunakan alat seperti **sandboxes** dan **VMs** untuk menguji kerentanannya.
- **Langkah pencegahan** meliputi **hashing**, **salting**, **MFA/2FA**, **CAPTCHA**, dan kebijakan kata sandi yang kuat.
