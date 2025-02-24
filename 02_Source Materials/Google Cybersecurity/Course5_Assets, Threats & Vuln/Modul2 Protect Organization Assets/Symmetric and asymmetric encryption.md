---
id: Symmetric and asymmetric encryption
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan tentang Symmetric dan Asymmetric Encryption

### Istilah Penting
- **Encryption**: Proses mengubah data dari format yang dapat dibaca menjadi format yang terenkripsi.
- **Public Key Infrastructure (PKI)**: Framework enkripsi yang mengamankan pertukaran informasi online.
- **Cipher**: Algoritma untuk mengenkripsi informasi.

### Jenis Enkripsi
1. **Symmetric Encryption**
   - Menggunakan satu **secret key** untuk mengenkripsi dan mendekripsi data.
   - Kelebihan: Proses lebih cepat.
   - Kekurangan: Keamanan lebih rendah karena berbagi key rentan terhadap pencurian.

2. **Asymmetric Encryption**
   - Menggunakan **public key** untuk enkripsi dan **private key** untuk dekripsi.
   - Kelebihan: Keamanan lebih tinggi karena hanya private key yang dirahasiakan.
   - Kekurangan: Proses lebih lambat.

### Panjang Key
- **Panjang key** sangat penting untuk melawan brute force attacks.
- Key yang lebih panjang lebih aman, tetapi memperlambat proses enkripsi.
- Contoh: **AES-128** dianggap sangat aman karena butuh miliaran tahun untuk brute force.

### Algoritma Enkripsi Umum
1. **Symmetric Algorithms**:
   - **Triple DES (3DES)**: Menggunakan key sepanjang 192 bit.
     Mulai ditinggalkan karena keterbatasan jumlah data yang bisa dienkripsi.
   - **Advanced Encryption Standard (AES)**: Mendukung key 128, 192, atau 256 bit.
     Salah satu algoritma paling aman saat ini.

2. **Asymmetric Algorithms**:
   - **RSA**: Menghasilkan key sepanjang 1,024 hingga 4,096 bit.
     Digunakan untuk melindungi data sangat sensitif.
   - **Digital Signature Algorithm (DSA)**: Digunakan bersamaan dengan RSA dalam PKI.

### Implementasi dan Alat
- **OpenSSL**: Tool open-source untuk menghasilkan public dan private key.
  *Contoh*: OpenSSL digunakan untuk memverifikasi digital certificates.
- Penting untuk menggunakan versi perangkat lunak yang aman karena bug seperti **Heartbleed**.

### Prinsip Keamanan
- **Kerckhoff's Principle**: Algoritma enkripsi tetap aman meskipun semua detail algoritma diketahui, kecuali private key.
- Algoritma custom sering kali mudah diretas jika tidak diuji secara publik.

### Contoh Penggunaan
- Website sering menggunakan **asymmetric encryption** untuk login (username/password).
- Setelah login, sesi web biasanya beralih ke **symmetric encryption** untuk mempercepat komunikasi.

### Regulasi Terkait
- **FIPS 140-3** dan **GDPR**: Menentukan standar enkripsi untuk melindungi data pengguna dan memastikan kepatuhan hukum.

### Kesimpulan
- **Symmetric encryption**: Cepat, tetapi kurang aman.
- **Asymmetric encryption**: Aman, tetapi lebih lambat.
- Kombinasi keduanya sering digunakan untuk menyeimbangkan keamanan dan pengalaman pengguna.
- Memahami dasar-dasar enkripsi penting untuk memenuhi regulasi dan melindungi data online.
