---
id: Access controls and authentication systems
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Rangkuman: Dasar-dasar Authentication dan Sistem Kontrol Akses

**Fitur Dasar Kontrol Akses:**
- **Tujuan:** Melindungi data dengan menjaga kerahasiaan, integritas, dan ketersediaan.
- **Fungsi Utama:** Authentication, Authorization, dan Accounting (AAA Framework).

## **Authentication:**
- **Definisi:** Sistem kontrol akses yang bertanya: *"Siapa Anda?"* untuk mengidentifikasi entitas yang mencoba mengakses informasi.
- **Tiga Faktor Authentication:**
  1. **Knowledge:** Sesuatu yang diketahui pengguna, seperti password atau jawaban pertanyaan keamanan.
  2. **Ownership:** Sesuatu yang dimiliki pengguna, seperti *One-Time Passcode (OTP)* yang dikirim melalui SMS atau email.
  3. **Characteristic:** Sesuatu yang menjadi ciri pengguna, seperti biometrik (sidik jari atau pemindaian wajah).

- **Syarat Authentication Berhasil:** Informasi yang diberikan harus cocok dengan data yang ada.

**Teknologi Pendukung Authentication:**
1. **Single Sign-On (SSO):**
   - **Fungsi:** Menggabungkan beberapa login menjadi satu proses autentikasi.
   - **Kelebihan:** Mempercepat akses ke sumber daya perusahaan.
   - **Kekurangan:** Rentan jika hanya menggunakan satu faktor autentikasi.

2. **Multi-Factor Authentication (MFA):**
   - **Fungsi:** Memerlukan lebih dari satu cara autentikasi untuk mengidentifikasi pengguna (contoh: kombinasi password dan OTP).
   - **Manfaat:** Menambahkan lapisan keamanan dan memperkuat sistem autentikasi.
   - **Penggunaan Bersama SSO:** Memberikan akses yang cepat sekaligus aman.

**Poin Utama:**
- SSO meningkatkan kenyamanan pengguna, tetapi harus dikombinasikan dengan MFA untuk menghindari risiko pemberian akses kepada pengguna yang salah.
- Authentication adalah langkah pertama dalam framework AAA; langkah berikutnya adalah Authorization untuk mengatur izin akses.
