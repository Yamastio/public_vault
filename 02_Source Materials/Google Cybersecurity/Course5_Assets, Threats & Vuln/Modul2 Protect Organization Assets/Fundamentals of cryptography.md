---
id: Fundamentals of cryptography
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan: Memahami PII dan Kriptografi

### Apa Itu PII?
- **PII (Personally Identifiable Information)**:
  - Informasi yang dapat mengidentifikasi individu, seperti:
    - Nama
    - Informasi medis dan keuangan
    - Foto, email, atau sidik jari
  - Menjaga privasi PII secara online memerlukan **kontrol keamanan** yang tepat.

### Peran Kriptografi dalam Keamanan Data
- **Kriptografi**:
  - Proses mengubah informasi menjadi bentuk yang tidak dapat dimengerti oleh pihak tak berwenang.
  - Dua langkah utama:
    1. **Enkripsi**: Mengubah data asli (*plaintext*) menjadi bentuk tak terbaca (*ciphertext*).
    2. **Dekripsi**: Mengembalikan *ciphertext* ke bentuk asli (*plaintext*).

### Caesar's Cipher: Metode Kriptografi Awal
- **Sejarah**:
  - Digunakan oleh Julius Caesar untuk menjaga kerahasiaan pesan militernya.
- **Cara Kerja**:
  - Huruf dalam alfabet digeser dengan jumlah tertentu (*shift*).
  - Contoh: "hello" dengan *shift* 3 menjadi "khoor".
- **Kunci Kriptografi**:
  - Elemen penting untuk mendekripsi *ciphertext*. Dalam contoh ini, kuncinya adalah *shift* 3.

### Kelemahan Caesar's Cipher
1. **Brute Force Attack**:
   - Pesan dapat dengan mudah dipecahkan hanya dengan mencoba semua kemungkinan *shift* (26 untuk alfabet Inggris).
2. **Ketergantungan pada Satu Kunci**:
   - Jika kunci hilang atau dicuri, data dapat diakses tanpa hambatan.

### Praktik Keamanan untuk Kriptografi
- Pastikan kunci kriptografi:
  - Tidak disimpan di tempat umum.
  - Dibagikan terpisah dari data yang akan didekripsi.

### Kesimpulan
- Caesar's cipher adalah awal dari metode enkripsi, tetapi memiliki banyak keterbatasan.
- Saat ini, digunakan algoritma yang lebih kompleks untuk menjaga privasi informasi secara online.
