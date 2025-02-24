---
id: Network hardening practices
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Network Hardening

- **Network hardening** berfokus pada keamanan yang berhubungan dengan jaringan, termasuk **filtering port**, **hak akses jaringan**, dan **enkripsi komunikasi**.
- Beberapa tugas dilakukan secara rutin, seperti pemeliharaan aturan firewall, analisis log jaringan, pembaruan patch, dan pencadangan server.
- Tugas lain dilakukan sekali dan diperbarui sesuai kebutuhan, seperti filter port di firewall dan pengaturan hak akses jaringan.

## Tugas Rutin

- **Pemeliharaan Aturan Firewall**: Aturan firewall yang terjaga dengan baik membatasi akses jaringan yang tidak sah dan hanya mengizinkan komunikasi yang diperlukan.
- **Analisis Log Jaringan**: Proses memeriksa log jaringan untuk mendeteksi kejadian penting. Alat seperti **SIEM (Security Information and Event Management)** digunakan untuk menganalisis log dan memberikan gambaran umum tentang kerentanannya, serta memberikan prioritas mitigasi.
- **Pembaruan Patch**: Sama seperti pada OS, pembaruan patch dilakukan untuk mengatasi kerentanannya dan memastikan bahwa perangkat lunak jaringan selalu diperbarui.
- **Pencadangan Server**: Backup server secara teratur untuk melindungi data penting dan memastikan pemulihan sistem setelah insiden.

## Tugas Sekali Lakukan dan Pembaruan Sesuai Kebutuhan

1. **Filter Port**:

   - **Port filtering** adalah fungsi firewall yang membatasi port mana yang diizinkan atau diblokir untuk komunikasi. Hanya port yang diperlukan untuk operasi jaringan yang diperbolehkan, sementara port yang tidak digunakan harus diblokir untuk menghindari kerentanannya.

2. **Hak Akses Jaringan**:

   - Membatasi akses jaringan hanya kepada pengguna yang berwenang. Akses harus berdasarkan peran yang diperlukan untuk setiap individu di organisasi.

3. **Segmentasi Jaringan**:

   - **Network segmentation** membagi jaringan menjadi subnet yang terisolasi untuk departemen yang berbeda (misalnya, departemen pemasaran dan keuangan) agar masalah di satu bagian jaringan tidak menyebar ke seluruh organisasi.
   - Segmentasi juga digunakan untuk memisahkan zona keamanan yang lebih sensitif, seperti data yang sangat terjamin.

4. **Enkripsi Komunikasi**:
   - Semua komunikasi jaringan harus dienkripsi menggunakan **standar enkripsi terbaru** untuk melindungi data yang dikirim melalui jaringan.
   - Zona yang membatasi akses data sensitif atau terbatas harus menggunakan enkripsi yang lebih kuat agar lebih sulit diakses.

## Kesimpulan

- **Network hardening** melibatkan langkah-langkah penting untuk melindungi infrastruktur jaringan, seperti pemeliharaan aturan firewall, analisis log, pembaruan patch, filter port, segmentasi jaringan, dan enkripsi.
- Pengamanan jaringan ini membantu memastikan bahwa hanya pengguna berwenang yang dapat mengakses informasi penting dan melindungi data dari ancaman eksternal.

Pemahaman tentang keamanan hardening pada jaringan ini sangat berguna bagi karier Anda sebagai analis keamanan siber.
