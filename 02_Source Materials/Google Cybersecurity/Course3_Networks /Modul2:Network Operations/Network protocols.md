---
id: Network protocols
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Definisi Protokol Jaringan (Network Protocols)

- Aturan yang memastikan data mencapai tujuan dengan benar.
- Digunakan oleh perangkat untuk mengatur **urutan pengiriman** dan **struktur data**.

## Contoh Penggunaan Protokol Jaringan: Mengakses Website

1. **Transmission Control Protocol (TCP):**

   - Membentuk koneksi antara perangkat (handshake).
   - Verifikasi sebelum komunikasi dilanjutkan.

2. **Address Resolution Protocol (ARP):**

   - Menentukan **MAC address** router atau perangkat berikutnya agar data sampai ke tujuan.

3. **Hypertext Transfer Protocol Secure (HTTPS):**

   - Mengamankan komunikasi antara browser dan server menggunakan **SSL/TLS**.
   - Contoh: Mengirim permintaan halaman web dan menerima respons secara aman.

4. **Domain Name System (DNS):**
   - Mengubah nama domain menjadi **IP address** untuk mengakses server tujuan.

## Keamanan dalam Protokol

- **HTTPS:**
  - Menggunakan **enkripsi SSL/TLS** untuk melindungi data dari pencurian oleh aktor jahat.

## Poin Penting untuk Analis Keamanan

- Protokol seperti **TCP**, **ARP**, **HTTPS**, dan **DNS** akan sering digunakan.
- HTTPS adalah contoh protokol penting yang menjaga komunikasi tetap aman.
- Dalam karier Anda, pemahaman dan penerapan protokol ini akan menjadi rutinitas sehari-hari.

## **Catatan Tambahan tentang TCP**

- **TCP (Transmission Control Protocol)** tidak terbatas hanya pada dua perangkat.
- TCP membangun **koneksi langsung** antara dua **endpoint** (pengirim dan penerima).
- Namun, infrastruktur jaringan di bawahnya (seperti router dan switch) bertugas untuk **merutekan data** melewati beberapa perangkat hingga mencapai tujuan.

### **Ilustrasi Singkat**

- Ketika Anda mengirimkan data ke server jauh:
  1. **Endpoint pengirim** memulai koneksi TCP.
  2. Data melewati jaringan dengan perangkat perantara (router).
  3. **Endpoint penerima** menyelesaikan koneksi TCP untuk menerima data.

### **Kesimpulan**

TCP mengatur komunikasi langsung antara dua endpoint, tetapi pengiriman data dilakukan oleh infrastruktur jaringan yang lebih luas.
