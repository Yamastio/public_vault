Tags: [[hacking_fundamentals]] [[blue_team]]

**Reconnaissance** adalah fase pengumpulan informasi yang penting dalam **cybersecurity** dan **penetration testing (pentest)**. Tujuannya adalah untuk mengumpulkan sebanyak mungkin data tentang target, sehingga dapat memahami struktur, potensi titik lemah, dan arsitektur sistem target sebelum eksploitasi diluncurkan. Proses ini biasanya dibagi menjadi dua jenis utama:

---

## 1. Passive Reconnaissance

Passive reconnaissance adalah metode mengumpulkan informasi tentang target tanpa melakukan interaksi langsung dengan sistemnya. Teknik ini melibatkan pengumpulan data dari sumber terbuka dan publik, sehingga aktivitas ini sulit terdeteksi oleh target. Karena tidak ada interaksi langsung, metode ini sangat berguna untuk memahami target secara awal tanpa meninggalkan jejak yang mencolok.

### Tujuan Passive Reconnaissance

- Memahami infrastruktur, jaringan, dan sumber daya target.
- Mengidentifikasi potensi titik lemah atau celah keamanan.
- Menyusun strategi serangan lebih lanjut atau untuk analisis keamanan.

### Metode yang Digunakan dalam Passive Reconnaissance

1. **Open Source Intelligence (OSINT)**: Menggunakan sumber daya terbuka seperti:
    - _Website resmi_: Mengumpulkan informasi dari situs web target.
    - _Media sosial_: Melacak aktivitas atau profil perusahaan dan karyawan.
    - _Forum dan komunitas online_: Mengamati diskusi yang relevan.
2. **Pencarian DNS (Domain Name System)**:
    - _WHOIS Lookup_: Menemukan detail terkait domain, pemilik, dan server.
    - _Reverse DNS Lookup_: Mengidentifikasi alamat IP yang terkait.
    - _Zone Transfer_: Jika DNS dikonfigurasi dengan buruk, memungkinkan transfer zona data.
3. **Browsing Cache Mesin Pencari**: Menggunakan cache dari mesin pencari untuk mengakses konten situs yang mungkin telah diubah atau dihapus.
4. **Analisis Metadata**: Mengekstrak metadata dari file yang tersedia di internet.
5. **Monitoring Jaringan Sosial**: Memantau aktivitas media sosial yang terkait dengan target.
6. **Footprinting dengan Pemetaan IP**: Menggunakan database publik untuk informasi terkait IP target.

### Kelebihan Passive Reconnaissance

- **Tidak Terdeteksi**: Sulit dideteksi karena tidak berinteraksi dengan sistem target.
- **Legal**: Selama informasi yang diperoleh adalah publik, tidak melanggar hukum.

### Keterbatasan Passive Reconnaissance

- **Keterbatasan Data**: Hanya bergantung pada informasi yang tersedia di publik.
- **Tidak Mendalam**: Memberikan gambaran umum tanpa detail teknis mendalam.

---

## 2. Active Reconnaissance

Active reconnaissance melibatkan interaksi langsung dengan sistem target untuk mendapatkan data lebih rinci. Karena melibatkan komunikasi langsung, teknik ini lebih berisiko untuk dideteksi oleh perangkat keamanan, namun dapat memberikan informasi yang jauh lebih mendalam.

### Tujuan Active Reconnaissance

- Memperoleh pemahaman yang lebih rinci tentang sistem target.
- Mengidentifikasi titik masuk untuk eksploitasi.
- Menyempitkan fokus pengujian pada area berisiko tinggi.

### Teknik Reconnaissance Aktif

1. **Scanning Jaringan**:
    - _Port Scanning_: Memindai port terbuka untuk layanan yang aktif.
    - _Vulnerability Scanning_: Mencari kerentanan dalam sistem.
    - _Service Fingerprinting_: Mengidentifikasi layanan spesifik yang berjalan.
2. **Social Engineering**:
    - _Phishing_: Memancing target untuk mengungkapkan informasi sensitif.
    - _Pretexting_: Membuat skenario palsu untuk memanipulasi target.
    - _Baiting_: Menggunakan perangkat fisik yang terinfeksi.
3. **Interaksi Langsung**:
    - _Panggilan Telepon_: Menggunakan identitas palsu untuk mendapatkan informasi.
    - _Mengunjungi Situs Web_: Mengeksplorasi celah keamanan.
    - _Formulir Kontak_: Menguji respons dari input tertentu.

### Tool yang Digunakan dalam Active Reconnaissance

- _Nmap_: Untuk pemindaian port dan layanan.
- _Nessus, OpenVAS_: Untuk pencarian kerentanan.
- _Metasploit_: Framework eksploitasi.
- _Burp Suite_: Untuk pengujian aplikasi web.
- _Wireshark_: Untuk analisis lalu lintas jaringan.

### Contoh Skenario Active Reconnaissance

Misalnya, seorang pentester dapat memindai port terbuka untuk melihat layanan yang berjalan, memeriksa kerentanan umum, atau menggunakan taktik rekayasa sosial untuk mendapatkan informasi tambahan.

## Penting untuk Diingat

- **Izin**: Dapatkan izin tertulis sebelum melakukan pengujian.
- **Etika**: Hindari tindakan merusak atau membahayakan sistem.
- **Hukum**: Patuh terhadap aturan yang berlaku.

---

Dengan kombinasi **passive dan active reconnaissance**, penguji keamanan atau penyerang dapat membangun gambaran lengkap tentang target, yang berguna untuk pengujian keamanan mendalam atau serangan.