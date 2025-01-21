Tags: [[hacking_fundamentals]] [[blue_team]]

Penetration testing atau uji penetrasi merupakan simulasi serangan siber yang bertujuan untuk mengidentifikasi dan memperbaiki kelemahan keamanan dalam sistem komputer. Penetration testing dilakukan secara etis dan dengan izin pemilik sistem agar kerentanan yang ditemukan dapat ditangani sebelum dieksploitasi oleh pihak tidak bertanggung jawab. Berikut adalah penjelasan mengenai **fase-fase utama dalam penetration testing**:

---

### **1. Reconnaissance (Pengumpulan Informasi)**

- **Tujuan**: Mengumpulkan sebanyak mungkin informasi tentang target sebelum melancarkan serangan.
- **Metode**:
    - **Passive Reconnaissance**: Mengamati target tanpa melakukan kontak langsung, seperti mengakses informasi yang tersedia secara publik (website, media sosial, DNS).
    - **Active Reconnaissance**: Melibatkan interaksi langsung dengan sistem target seperti ping atau scanning port.
- **Tools Umum**:
    - **Whois** untuk mendapatkan informasi registrasi domain.
    - **Shodan** untuk memindai perangkat yang terhubung ke internet.
    - **Google Hacking** untuk mengungkap data atau dokumen sensitif.

### **2. Scanning (Pemindaian)**

- **Tujuan**: Mengidentifikasi layanan, port yang terbuka, dan potensi kerentanan di sistem target.
- **Jenis Pemindaian**:
    - **Port Scanning**: Mengidentifikasi port terbuka dan layanan yang berjalan di atasnya.
    - **Vulnerability Scanning**: Memindai sistem untuk menemukan kerentanan yang diketahui menggunakan database keamanan.
- **Tools Umum**:
    - **Nmap** untuk pemindaian port.
    - **Nessus** dan **OpenVAS** untuk pemindaian kerentanan.

### **3. Gaining Access (Mendapatkan Akses)**

- **Tujuan**: Mengeksploitasi kerentanan yang ditemukan dalam fase sebelumnya untuk mendapatkan akses ke sistem target.
- **Teknik Umum**:
    - **SQL Injection**: Mengeksploitasi input yang tidak tervalidasi dalam query database.
    - **Cross-Site Scripting (XSS)**: Menyuntikkan skrip berbahaya ke halaman web.
    - **Buffer Overflow**: Mengeksploitasi batas buffer dalam memori aplikasi.
- **Tools Umum**:
    - **Metasploit Framework** untuk eksploitasi otomatis.

### **4. Maintaining Access (Menjaga Akses)**

- **Tujuan**: Setelah mendapatkan akses, penyerang akan berusaha untuk mempertahankan akses tersebut agar dapat mengakses sistem target di masa depan.
- **Teknik Umum**:
    - **Backdoors**: Menyisipkan pintu belakang yang memungkinkan akses ulang di kemudian hari.
    - **Rootkits**: Mengubah kernel sistem untuk menyembunyikan aktivitas penyerang.
    - **Persistence Mechanisms**: Menggunakan layanan yang terus berjalan atau modifikasi file sistem.

### **5. Covering Tracks (Menyembunyikan Jejak)**

- **Tujuan**: Menghapus atau menyamarkan jejak aktivitas agar tidak terdeteksi.
- **Teknik Umum**:
    - **Log Wiping**: Menghapus atau memodifikasi log aktivitas di sistem target.
    - **Timestamp Modification**: Mengubah waktu modifikasi file agar tidak terlihat mencurigakan.
    - **File Hiding**: Menyembunyikan file penting yang berkaitan dengan serangan.

---

Dengan memahami setiap fase penetration testing ini, tim keamanan dapat mengambil langkah-langkah pencegahan yang sesuai, seperti memperkuat jaringan, melakukan pemantauan aktif, serta meningkatkan kesadaran tentang ancaman siber. Langkah ini akan membantu mencegah dan meminimalkan dampak dari potensi serangan.