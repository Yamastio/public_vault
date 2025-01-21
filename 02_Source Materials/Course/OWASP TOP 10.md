Tags: [[hacking_fundamentals]]

Berikut revisi dan tambahan untuk memperluas serta memperbaiki catatan Anda:

---

## OWASP
**Open Web Application Security Project (OWASP)** adalah organisasi nirlaba yang berfokus pada meningkatkan keamanan aplikasi web.  
- **Didirikan oleh:** Mark Curphey.  
- **Tujuan:** Memberikan panduan, informasi, tools, dan teknik untuk mengidentifikasi serta mengatasi kerentanan keamanan web secara gratis.  
- **Sumber daya:** OWASP menyediakan berbagai tools seperti **OWASP ZAP (Zed Attack Proxy)**, cheat sheets, dan dokumentasi best practice.

---

## OWASP Top 10
OWASP Top 10 adalah daftar prioritas kerentanan keamanan aplikasi web yang sering terjadi.  
- **Fungsi:** Panduan untuk mengidentifikasi dan mengurangi risiko keamanan dalam aplikasi web.  
- **Update berkala:** Daftar diperbarui secara teratur untuk mencerminkan ancaman keamanan terkini.  
- **Penting:** Ini tidak hanya panduan teknis, tetapi juga membantu organisasi dalam membangun kebijakan keamanan aplikasi.

---

## OWASP Top 10 (2017)
Berikut daftar OWASP Top 10 tahun 2017 dengan penjelasan yang lebih detail:

### 1. Injection (A01:2017)
- **Definisi:** Serangan yang terjadi ketika penyerang menyisipkan **malicious payloads** ke input aplikasi yang kemudian diproses tanpa validasi.
- **Contoh:** SQL Injection, Command Injection, LDAP Injection.
- **Mitigasi:**  
  - Gunakan prepared statements (parameterized queries).  
  - Validasi dan sanitasi input pengguna.  

### 2. Broken Authentication (A02:2017)
- **Definisi:** Kelemahan dalam mekanisme autentikasi yang memungkinkan hacker mengambil alih akun atau sistem.  
- **Contoh:**  
  - Penggunaan credential default.  
  - Pengelolaan session yang tidak aman.  
- **Mitigasi:**  
  - Implementasi autentikasi multifaktor (MFA).  
  - Jangan menyimpan password secara plaintext; gunakan hashing seperti bcrypt.  

### 3. Sensitive Data Exposure (A03:2017)
- **Definisi:** Data sensitif seperti informasi pribadi atau kredensial bocor karena kurangnya enkripsi atau konfigurasi keamanan.  
- **Contoh:** Data pengguna dikirim melalui HTTP, bukan HTTPS.  
- **Mitigasi:**  
  - Gunakan protokol HTTPS untuk semua data yang dikirim.  
  - Enkripsi data sensitif dalam penyimpanan dan transfer.  

### 4. XML External Entities (XXE) (A04:2017)
- **Definisi:** Kerentanan saat parser XML memproses entitas eksternal yang berbahaya.  
- **Contoh:** Server membaca file sistem seperti `/etc/passwd`.  
- **Mitigasi:**  
  - Nonaktifkan entitas eksternal di parser XML.  
  - Gunakan parser XML modern yang aman.  

### 5. Broken Access Control (A05:2017)
- **Definisi:** Kontrol akses yang tidak efektif memungkinkan pengguna melakukan tindakan yang tidak diotorisasi.  
- **Contoh:** Akses admin oleh user biasa.  
- **Mitigasi:**  
  - Terapkan model kontrol akses berbasis peran (RBAC).  
  - Validasi semua akses di sisi server.  

### 6. Security Misconfiguration (A06:2017)
- **Definisi:** Kelemahan akibat konfigurasi keamanan yang salah, seperti penggunaan default settings atau debug mode aktif di produksi.  
- **Contoh:** Direktori aplikasi yang terekspos publik.  
- **Mitigasi:**  
  - Terapkan prinsip "minimal configuration".  
  - Gunakan alat seperti OWASP ASVS untuk audit.  

### 7. Cross-Site Scripting (XSS) (A07:2017)
- **Definisi:** Penyerang menyisipkan kode berbahaya (biasanya JavaScript) ke dalam aplikasi untuk dieksekusi oleh browser pengguna lain.  
- **Contoh:** Popup yang mencuri cookie pengguna.  
- **Mitigasi:**  
  - Gunakan encoding karakter untuk input/output.  
  - Gunakan Content Security Policy (CSP).  

### 8. Insecure Deserialization (A08:2017)
- **Definisi:** Kerentanan yang terjadi ketika data deserialisasi berasal dari sumber tidak terpercaya.  
- **Contoh:** Penyerang mengirim objek berbahaya ke API untuk eksekusi kode.  
- **Mitigasi:**  
  - Hindari deserialisasi data tidak terpercaya.  
  - Gunakan format data yang aman seperti JSON.  

### 9. Using Components with Known Vulnerabilities (A09:2017)
- **Definisi:** Aplikasi menggunakan komponen pihak ketiga yang memiliki kerentanan yang diketahui.  
- **Contoh:** Library usang yang memiliki exploit terkenal.  
- **Mitigasi:**  
  - Perbarui dependency secara rutin.  
  - Gunakan tools seperti Dependabot atau Snyk.  

### 10. Insufficient Logging & Monitoring (A10:2017)
- **Definisi:** Kurangnya logging dan monitoring membuat organisasi tidak sadar akan serangan yang sedang berlangsung atau sebelumnya.  
- **Contoh:** Tidak ada log untuk percobaan login yang gagal.  
- **Mitigasi:**  
  - Implementasi logging yang komprehensif.  
  - Gunakan SIEM untuk analisis log.  

---

## Perbandingan OWASP 2017 dan 2021
- **Penambahan di 2021:**  
  - **Insecure Design:** Fokus pada masalah keamanan sejak tahap desain aplikasi.  
  - **Shift Prioritas:** Broken Access Control naik menjadi nomor 1 karena risiko tinggi yang sering terjadi.

---

## Rekomendasi untuk Belajar
- **Praktik Langsung:** Gunakan tools seperti **OWASP ZAP** atau **Burp Suite** untuk memahami eksploitasi kerentanan.  
- **Simulasi:** Coba platform seperti **Hack The Box**, **TryHackMe**, atau aplikasi yang dirancang untuk latihan seperti **DVWA** (Damn Vulnerable Web Application).  
- **Langganan Newsletter:** Ikuti perkembangan OWASP dan update keamanan melalui situs resmi mereka.