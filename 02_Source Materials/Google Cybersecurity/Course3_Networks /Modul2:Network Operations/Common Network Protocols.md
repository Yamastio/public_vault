---
id: Common Network Protocols
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Apa itu Protokol Jaringan?

- Protokol jaringan adalah seperangkat aturan yang digunakan oleh perangkat di jaringan untuk menentukan **urutan pengiriman** dan **struktur data**.
- Berfungsi seperti "bahasa bersama" yang memungkinkan perangkat di seluruh dunia saling berkomunikasi.

### Tiga Kategori Protokol Jaringan

1. **Protokol Komunikasi**
   Mengatur pengiriman data di jaringan, termasuk metode pemulihan data yang hilang.

   - **Transmission Control Protocol (TCP):**
     - Membentuk koneksi antar perangkat menggunakan proses _three-way handshake_.
     - Beroperasi di lapisan transport TCP/IP.
   - **User Datagram Protocol (UDP):**
     - Protokol tanpa koneksi yang cepat tetapi kurang andal dibanding TCP.
     - Digunakan untuk DNS dan streaming data.
     - Beroperasi di lapisan transport TCP/IP.
   - **Hypertext Transfer Protocol (HTTP):**
     - Mengatur komunikasi antara klien dan server web melalui port 80.
     - Digantikan oleh **HTTPS** karena lebih aman.
     - Beroperasi di lapisan aplikasi TCP/IP.
   - **Domain Name System (DNS):**
     - Menerjemahkan nama domain menjadi alamat IP.
     - Biasanya menggunakan UDP port 53, tetapi dapat menggunakan TCP untuk respons besar.
     - Beroperasi di lapisan aplikasi TCP/IP.

2. **Protokol Manajemen**
   Digunakan untuk **memantau** dan **mengelola aktivitas jaringan**.

   - **Simple Network Management Protocol (SNMP):**
     - Mengelola perangkat jaringan, seperti mengatur ulang kata sandi atau memantau penggunaan bandwidth.
     - Beroperasi di lapisan aplikasi TCP/IP.
   - **Internet Control Message Protocol (ICMP):**
     - Melaporkan kesalahan transmisi data, seperti dengan perintah "ping".
     - Beroperasi di lapisan internet TCP/IP.

3. **Protokol Keamanan**
   Melindungi data saat dikirim dan diterima di jaringan melalui **enkripsi**.
   - **Hypertext Transfer Protocol Secure (HTTPS):**
     - Versi aman dari HTTP yang menggunakan enkripsi SSL/TLS melalui port 443.
     - Beroperasi di lapisan aplikasi TCP/IP.
   - **Secure File Transfer Protocol (SFTP):**
     - Menggunakan SSH dan port TCP 22 untuk transfer file yang aman.
     - Umum digunakan untuk penyimpanan cloud.
     - Beroperasi di lapisan aplikasi TCP/IP.

## Catatan Penting

- Protokol keamanan (HTTPS, SFTP) **tidak menyembunyikan alamat IP sumber atau tujuan**, sehingga penyerang masih bisa mendapatkan informasi dasar.

## Takeaway

- Memahami protokol jaringan adalah **dasar penting** bagi analis keamanan siber pemula.
- Pengetahuan ini membantu menganalisis kerentanan jaringan, memitigasi risiko, dan mencegah serangan di masa depan.
