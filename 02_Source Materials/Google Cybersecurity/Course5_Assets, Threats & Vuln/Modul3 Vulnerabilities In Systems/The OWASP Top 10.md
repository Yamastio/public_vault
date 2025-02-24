---
id: The OWASP Top 10
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Rangkuman: OWASP Top 10 dan Peranannya dalam Keamanan Aplikasi Web

**Apa itu OWASP?**
- **OWASP (Open Web Application Security Project)** adalah organisasi nirlaba yang fokus pada meningkatkan keamanan perangkat lunak, khususnya aplikasi web.
- OWASP menyediakan platform terbuka untuk berbagi informasi, alat, dan acara yang berfokus pada keamanan aplikasi web.

**OWASP Top 10:**
- **OWASP Top 10** adalah daftar sepuluh kerentanannya paling umum yang telah dipublikasikan sejak 2003 untuk meningkatkan kesadaran tentang kerentanannya yang paling banyak diserang di web.
- Organisasi besar sering merujuk pada OWASP Top 10 selama pengembangan aplikasi untuk memastikan program mereka mengatasi kesalahan keamanan yang umum.

**Kerentanannya yang Paling Umum di OWASP Top 10:**
1. **Broken Access Control (Kontrol Akses Rusak):**
   - Mengacu pada kegagalan dalam mekanisme kontrol akses yang dapat memberi akses tidak sah ke aplikasi atau informasi.

2. **Cryptographic Failures (Kegagalan Kriptografi):**
   - Terjadi saat data sensitif, seperti PII, tidak dienkripsi dengan metode yang cukup kuat, meningkatkan risiko kebocoran data.

3. **Injection (Injeksi):**
   - Terjadi ketika kode berbahaya disisipkan ke dalam aplikasi yang rentan, seperti melalui form login, yang memungkinkan peretas mencuri atau mengubah kredensial.

4. **Insecure Design (Desain Tidak Aman):**
   - Aplikasi yang tidak didesain untuk menghadapi serangan dan tidak memiliki kontrol keamanan yang memadai.

5. **Security Misconfiguration (Misconfigurasi Keamanan):**
   - Terjadi saat pengaturan keamanan tidak tepat atau tidak diperbarui dengan benar, seperti penggunaan pengaturan default pada server.

6. **Vulnerable and Outdated Components (Komponen Rentan dan Kadaluarsa):**
   - Penggunaan komponen perangkat lunak yang sudah rentan atau usang yang dapat dieksploitasi oleh penyerang.

7. **Identification and Authentication Failures (Kegagalan Identifikasi dan Autentikasi):**
   - Gagal mengidentifikasi dan memverifikasi pengguna yang sah, yang memungkinkan akses tidak sah ke aplikasi.

8. **Software and Data Integrity Failures (Kegagalan Integritas Perangkat Lunak dan Data):**
   - Terjadi ketika pembaruan atau patch tidak diperiksa dengan cermat sebelum diterapkan, yang dapat mengekspos aplikasi pada serangan, seperti serangan rantai pasokan.

9. **Security Logging and Monitoring Failures (Kegagalan Pencatatan dan Pemantauan Keamanan):**
   - Kegagalan untuk mencatat atau memantau peristiwa keamanan, yang penting untuk mendeteksi dan memperbaiki masalah keamanan.

10. **Server-Side Request Forgery (SSRF - Pemalsuan Permintaan Server):**
![SSRF](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/DT6Hkom1RcugsbS_BFgoLw_7e1de97a7fdc4e00b7c9b14a0ad5fcf1_Pfjezx6XbwJ_TAJbWmCtLMpwLX4YD2xP4Se2IJeQF4uTD6BtqNXlcpObbGHeJuzWlxr5A3WqWQzZ2K6E6kFLsX3JiI0bxbFtWFjNUCxZTgs7ftpEgVEcI87zvBxN2flvGXs37nW_RJF0QVLY7798FCXB9pAH_uUI3zYLbXOiOpGcdhti00aMTwl7xbMFpg?expiry=1736121600000&hmac=frdJ8Y8ZYQacFk6sdKe6Hc49zmhXv72lmPjMZEl8aks)
    - Penyerang memanipulasi permintaan server untuk mengakses data yang tidak sah dari server yang rentan.

**Poin Penting:**
- **OWASP Top 10** adalah referensi yang berguna bagi perusahaan untuk merancang aplikasi yang lebih aman dan menghindari kesalahan desain atau pengaturan yang dapat mengarah pada kerentanannya.
- Daftar ini juga digunakan oleh auditor untuk mengevaluasi kepatuhan terhadap peraturan keamanan.

