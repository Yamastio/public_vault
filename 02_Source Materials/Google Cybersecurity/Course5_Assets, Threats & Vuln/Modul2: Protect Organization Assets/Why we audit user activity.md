---
id: Why we audit user activity
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Rangkuman: Akuntansi dalam Sistem Keamanan Akses

**Pentingnya Akuntansi:**
- Akuntansi adalah praktik pemantauan **access logs**, yang merekam siapa yang mengakses sistem, kapan akses dilakukan, dan sumber daya apa yang digunakan.
- Log akses sangat penting untuk mendeteksi kejadian keamanan seperti upaya login yang gagal atau serangan peretasan, serta untuk mengidentifikasi kebocoran data.

**Cara Kerja Akuntansi:**
- **Session** adalah urutan permintaan dan respons HTTP Basic Auth yang terkait dengan pengguna yang sama.
- Log akses adalah catatan sesi yang merekam seluruh perjalanan pengguna dalam sistem, dimulai dari login hingga logout.

**Proses Pengumpulan Data:**
1. **Session ID:**
   - Setiap kali sesi dimulai, ID sesi yang unik dibuat. ID ini mengidentifikasi pengguna dan perangkat mereka.
   - ID sesi ini melekat pada pengguna selama sesi, hingga mereka keluar atau sesi berakhir secara otomatis.

2. **Session Cookies:**
   - Cookies bertindak sebagai token untuk memvalidasi sesi. Mereka menentukan berapa lama sesi akan berlangsung dan informasi apa yang akan ditampilkan kepada pengguna.
   - Cookies meningkatkan keamanan dan efisiensi sesi web, karena tidak ada informasi sensitif yang dibagikan, seperti username atau password.

**Ancaman Keamanan:**
- **Session Hijacking:**
   - Ketika seorang penyerang mendapatkan **session ID** yang sah, mereka dapat menyamar sebagai pengguna yang sah dan melakukan tindakan yang merugikan, seperti mencuri data atau uang.
   - Jika token Single Sign-On (SSO) dicuri melalui cookies, penyerang bahkan dapat mengakses sistem lain yang tampaknya aman.

**Pentingnya Pemantauan Log Akses:**
- Aktivitas yang tidak biasa dalam **access logs** bisa menunjukkan bahwa informasi telah diakses atau dicuri secara tidak sah.
- Akuntansi memberikan wawasan berharga yang meningkatkan keamanan data dan membantu mengidentifikasi potensi ancaman.

**Poin Utama:**
- Akuntansi adalah tentang memantau dan menganalisis log akses untuk meningkatkan keamanan.
- Pemantauan sesi dan penggunaan cookies penting untuk mengidentifikasi dan mencegah serangan seperti **session hijacking**.
