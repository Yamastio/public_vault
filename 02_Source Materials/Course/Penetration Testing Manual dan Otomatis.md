Tags: [[hacking_fundamentals]]

## Penetration Testing Manual

**Penetration Testing Manual** dilakukan secara langsung oleh pentester untuk mengevaluasi keamanan sistem dengan cara yang menyerupai metode serangan hacker.  
- **Keunggulan utama:**  
  - Lebih fleksibel karena memahami sudut pandang penyerang.  
  - Dapat menemukan kerentanan yang tidak terdeteksi oleh alat otomatis.  

---

### Tahapan Penetrasi Manual

1. **Data Collection (Pengumpulan Data):**  
   - Langkah awal untuk mengumpulkan informasi sebanyak mungkin tentang target.  
   - Informasi yang dicari mencakup:  
     - Plugin yang digunakan.  
     - Versi sistem atau software.  
     - Teknologi backend (server, database, dll).  
     - Rekayasa sosial (jika diperlukan).  
   - Tools pendukung: **Whois, Recon-ng, Nmap, Nikto, Burp Suite.**

2. **Vulnerability Assessment (Penilaian Kerentanan):**  
   - Mengidentifikasi kelemahan dalam sistem yang dapat dieksploitasi.  
   - Hasilnya memberikan daftar kerentanan untuk dievaluasi lebih lanjut.  
   - Tools pendukung: **Nessus, OpenVAS, Qualys.**

3. **Actual Exploitation (Eksploitasi Kerentanan):**  
   - Melakukan serangan terhadap kerentanan yang ditemukan untuk memahami dampaknya.  
   - Contoh: **SQL Injection, XSS, RCE** (Remote Code Execution).  
   - Pentester sering menggunakan framework seperti **Metasploit**.  

4. **Report Preparation (Penyusunan Laporan):**  
   - Mengorganisasikan hasil pengujian dan memberikan rekomendasi perbaikan.  
   - Struktur laporan mencakup:  
     - Ringkasan eksekutif (executive summary).  
     - Deskripsi kerentanan.  
     - Dampak potensial.  
     - Saran mitigasi dan pencegahan.  

---

### Kategori Penetrasi Manual

1. **Focused Manual Penetration Testing (Pengujian Terfokus):**  
   - Hanya menguji kerentanan tertentu atau komponen spesifik dari sistem.  
   - Contoh: Menguji kekuatan autentikasi pada aplikasi login.  

2. **Comprehensive Manual Penetration Testing (Pengujian Komprehensif):**  
   - Menguji seluruh sistem termasuk jaringan, aplikasi, dan perangkat yang saling terhubung.  
   - Mengidentifikasi kombinasi kerentanan kecil yang mungkin memiliki dampak besar.  
   - Cocok untuk pengujian tingkat enterprise.  

---

## Penetration Testing Otomatis

**Penetration Testing Otomatis** dilakukan dengan menggunakan alat otomatis untuk memindai dan mengeksploitasi sistem secara cepat.  
- **Keunggulan utama:**  
  - Cepat, efisien, dan hemat biaya.  
  - Tidak membutuhkan keahlian mendalam untuk mengoperasikan alat.  

---

### Tools Populer untuk Penetrasi Otomatis
1. **SQLMAP:**  
   - Alat untuk mendeteksi dan mengeksploitasi kerentanan SQL Injection.  

2. **Burp Suite:**  
   - Platform untuk pengujian keamanan aplikasi web.  
   - Mampu melakukan scanning otomatis, intercept traffic, dan banyak lagi.  

3. **Shodan:**  
   - Mesin pencari untuk perangkat IoT atau server yang terekspos ke internet.  

4. **Nikto:**  
   - Alat untuk menganalisis kelemahan pada web server.  

5. **OWASP ZAP (Zed Attack Proxy):**  
   - Framework untuk memindai kerentanan aplikasi web.  

---

## Perbedaan Penetrasi Manual dan Otomatis

| **Aspek**             | **Penetrasi Manual**                                      | **Penetrasi Otomatis**                                        |
| --------------------- | --------------------------------------------------------- | ------------------------------------------------------------- |
| **Keahlian**          | Membutuhkan praktisi ahli.                                | Tidak memerlukan keahlian mendalam, hanya pengoperasian alat. |
| **Alat**              | Menggunakan berbagai tools terpisah sesuai kebutuhan.     | Menggunakan alat otomatis yang terintegrasi.                  |
| **Fleksibilitas**     | Sangat fleksibel, mampu menyesuaikan metode serangan.     | Kurang fleksibel, tergantung algoritma alat.                  |
| **Kecepatan**         | Lambat, membutuhkan waktu lama untuk analisis mendalam.   | Cepat, memindai sistem dalam waktu singkat.                   |
| **Hasil**             | Bervariasi tergantung metode dan pengalaman pentester.    | Konsisten sesuai kemampuan alat.                              |
| **Analisis Mendalam** | Mampu mengidentifikasi kerentanan kompleks.               | Tidak dapat melakukan analisis situasional yang mendalam.     |
| **Skalabilitas**      | Kurang efisien untuk sistem besar dengan banyak endpoint. | Efisien untuk memindai jaringan besar.                        |

---

## Kapan Menggunakan Metode Manual atau Otomatis?

- **Manual:**
  - Ketika membutuhkan analisis mendalam.
  - Menghadapi sistem yang kompleks atau unik.
  - Membutuhkan pendekatan khusus yang tidak dapat ditangani alat otomatis.

- **Otomatis:**
  - Untuk pengujian awal atau identifikasi kerentanan umum.
  - Ketika waktu atau sumber daya terbatas.
  - Untuk pengujian sistem dengan arsitektur standar.  
