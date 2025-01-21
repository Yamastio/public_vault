Tags: [[hacking_intermediate]] [[hacking_tools]]

## Apa itu Burp Suite
Burp Suite adalah alat yang digunakan secara luas untuk penetration testing (pengujian penetrasi) di aplikasi web. Burp Suite memungkinkan pengguna untuk mengintercept dan menganalisis lalu lintas web yang dikirimkan antara browser dan server, termasuk permintaan (request) dan respons (response). Cara kerjanya adalah dengan mengkonfigurasi proxy di browser atau perangkat mobile (Android/iOS) agar lalu lintas web dapat dialihkan ke Burp Suite untuk dianalisis.

## Instalasi Burp Suite
1. **Download Burp Suite** melalui halaman resmi [PortSwigger.net](https://portswigger.net/burp).
2. Login menggunakan email Anda.
3. Pilih dan download **Community Edition** (versi gratis).

## Konfigurasi Burp Suite dengan Firefox
1. **Buka Pengaturan Firefox**:
   - Klik menu (tiga garis horizontal) di pojok kanan atas.
   - Pilih **Settings** dan scroll ke bawah untuk menemukan bagian **Network Settings**.
2. **Atur Proxy**:
   - Cari keyword **Network Settings** dan klik **Settings**.
   - Pilih **Manual proxy configuration**.
   - Masukkan **127.0.0.1** sebagai **HTTP Proxy** dan **8080** sebagai port.
   - Centang **Use this proxy server for all protocols**.
3. **Konfigurasi Burp Suite**:
   - Buka Burp Suite dan pergi ke tab **Proxy**.
   - Pilih **Options** dan pastikan **Proxy Listener** terpasang di **127.0.0.1:8080** (default).
4. **Install Burp Suite CA Certificate di Firefox**:
   - Akses Burp Suite di browser Anda dengan menuju ke `http://burpsuite/`.
   - Download **CA Certificate** yang tersedia di bagian kanan atas.
   - Di Firefox, pergi ke **Settings > Privacy & Security > Certificates**, kemudian klik **View Certificates**.
   - Klik **Import**, pilih dan impor certificate yang sudah diunduh dari Burp Suite.
   - Setelah sertifikat terpasang, restart Firefox.

Sekarang Anda dapat mengintercept permintaan HTTP dan HTTPS melalui Burp Suite di Firefox.

## Fitur-Fitur Burp Suite
1. **Dashboard**:
   - **Issue Activity**: Menampilkan informasi tentang kerentanannya, seperti SQL Injection, XSS, dll. Detail kerentanannya akan ditampilkan di sini.
   - **Target**: Menyusun target pengujian, memungkinkan Anda untuk fokus pada objek yang relevan.
     - **HTTP History**: Menampilkan daftar permintaan yang sudah dilakukan.
     - **Issue Definitions**: Penjelasan tentang jenis kerentanannya.

2. **Proxy**:
   - **Intercept**: Menangkap permintaan dan respons yang dikirimkan antara browser dan server. Anda dapat melihat dan memodifikasi data ini sebelum mengirimnya ke server.
   - **Repeater**: Setelah menangkap permintaan, Anda dapat mengirim ulang permintaan yang sama beberapa kali untuk menguji respons server, contohnya untuk eksploitasi kerentanannya.
   
3. **Repeater**:
   - Mengirim permintaan HTTP secara berulang. Ini sangat membantu dalam eksploitasi kerentanannya seperti SQL Injection.

4. **Intruder**:
   - Digunakan untuk melakukan serangan **bruteforce** atau untuk menguji apakah aplikasi rentan terhadap teknik tertentu seperti **Rate Limiting**.
     - **Payload**: Tentukan payload seperti **Simple List** untuk mengganti parameter di request.
     - **Start Attack**: Mulai proses serangan untuk mengirimkan data sesuai dengan payload yang telah ditentukan.

5. **Logger**:
   - Mencatat log semua aktivitas yang terjadi pada Burp Suite, seperti **HTTP History**, yang berfungsi sebagai arsip permintaan dan respons.

6. **Extensions (BApp Store)**:
   - **BApp Store**: Menyediakan berbagai ekstensi untuk menambah fungsionalitas Burp Suite. Beberapa ekstensi gratis dan beberapa lainnya berbayar. Ekstensi ini bisa memperluas kemampuan Burp Suite untuk analisis lebih lanjut.

## Kegunaan Burp Suite
1. **Intruder**:
   - Untuk **bruteforce** pada form login, password, atau menguji kerentanannya terhadap **Rate Limiting**.
2. **Repeater**:
   - Untuk mengirimkan ulang permintaan berulang kali, sangat berguna untuk eksploitasi seperti **SQL Injection**.
3. **Extensions**:
   - Menambah kemampuan Burp Suite dengan berbagai ekstensi, baik yang gratis maupun berbayar.

## Burp Suite Academy
Untuk belajar menggunakan Burp Suite lebih dalam, Anda dapat mengakses **Burp Suite Academy** secara gratis. Di sana, Anda dapat menemukan materi tentang **web security**, dan **ethical hacking**:
- **Website**: [Burp Suite Academy](https://portswigger.net/web-security)
