---
id: The mechanisms of authorization
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Rangkuman: Mekanisme Otorisasi dalam Sistem Kontrol Akses

**Pentingnya Otorisasi:**
- Otorisasi berfungsi untuk menentukan apa yang dapat dilakukan oleh pengguna setelah autentikasi mereka diverifikasi.
- Otorisasi terkait erat dengan prinsip **least privilege**, yaitu memberikan akses hanya selama yang diperlukan.
- **Separation of duties** juga menjadi prinsip penting dalam otorisasi untuk mencegah penyalahgunaan sistem. Misalnya, seseorang yang bertanggung jawab memberi layanan pelanggan seharusnya tidak dapat memberikan nilai tinggi untuk dirinya sendiri tanpa pengawasan.

**Prinsip Keamanan yang Relevan:**
- **Least privilege** dan **separation of duties** tidak hanya berlaku untuk orang, tetapi juga untuk sistem, jaringan, basis data, dan proses lainnya dalam organisasi.

**Kontrol Akses yang Digunakan dalam Otorisasi:**
1. **HTTP Basic Auth:**
   - Digunakan untuk autentikasi pengguna ketika berkomunikasi dengan server.
   - Mengirimkan username dan password setiap kali pengguna mengakses situs.
   - Rentan terhadap serangan karena data dikirimkan secara terbuka, yang membuatnya tidak aman. Kini, banyak situs menggunakan **HTTPS** untuk menggantikan HTTP guna mengamankan data yang dikirim.

2. **OAuth:**
   - Merupakan protokol otorisasi standar terbuka yang memungkinkan berbagi akses antara aplikasi.
   - OAuth menggunakan **API tokens** untuk mengotentikasi pengguna tanpa mengirimkan username dan password yang sensitif.
   - API tokens mengandung informasi mengenai identitas pengguna, izin situs, dan lainnya. Pengguna tetap dapat menikmati keamanan seperti **multi-factor authentication** (MFA) yang aktif pada akun mereka.

**Keuntungan OAuth:**
- Mengurangi risiko penyalahgunaan kredensial karena API token yang terenkripsi mengurangi paparan informasi sensitif.

**Pentingnya Pemantauan Akses:**
- Selain mengontrol akses, pemantauan akses juga sangat penting untuk menjaga keamanan informasi.

**Poin Utama:**
- Otorisasi mengatur apa yang dapat dilakukan pengguna setelah mereka diautentikasi.
- HTTP Basic Auth dan OAuth adalah dua contoh protokol otorisasi yang mendukung prinsip-prinsip keamanan seperti **least privilege** dan **separation of duties**.
