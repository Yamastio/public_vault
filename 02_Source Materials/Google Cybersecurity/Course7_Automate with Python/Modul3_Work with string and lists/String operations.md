---
id: String operations
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Pemahaman String di Python untuk Security Analyst

Sebagai **security analyst**, memahami cara kerja string sangat penting, terutama untuk menganalisis data seperti **username** atau pola dalam informasi login. Berikut adalah ringkasan materi mengenai **string** di Python:

### Pengertian String

1. **String** adalah data yang terdiri dari **urutan karakter berurutan**.

   - Ditulis di antara **tanda kutip** (bisa tunggal `'` atau ganda `"`).
   - Contoh: `"Hello"`, `"123"`, dan `"Number 1!"`.

2. **Variabel** dapat digunakan untuk menyimpan string, misalnya:

   ```python
   my_string = "security"
   ```

3. String juga dapat dibuat dari tipe data lain, seperti **integer** atau **float**, menggunakan fungsi bawaan `str()`.
   - Contoh:
     ```python
     new_string = str(123)  # Mengubah integer 123 menjadi string "123"
     ```

### Operasi Dasar pada String

1. **Fungsi `len()`**

   - Digunakan untuk menghitung **jumlah karakter** dalam string.
   - Contoh:
     ```python
     print(len("Hello"))  # Output: 5
     ```
   - Aplikasi: Memvalidasi **IPv4 address**, yang panjang maksimalnya 15 karakter.

2. **String Concatenation (Penggabungan String)**
   - Menggabungkan dua string menggunakan operator `+`.
   - Contoh:
     ```python
     print("Hello" + "world")  # Output: "Helloworld"
     ```
   - Catatan: Operator seperti `-` tidak berlaku untuk string.

### String Methods

**Method** adalah fungsi yang khusus untuk tipe data tertentu. Pada string, beberapa method umum meliputi:

1. **`upper()`**

   - Mengubah semua huruf dalam string menjadi **huruf besar**.
   - Contoh:
     ```python
     print("Hello".upper())  # Output: "HELLO"
     ```

2. **`lower()`**
   - Mengubah semua huruf dalam string menjadi **huruf kecil**.
   - Contoh:
     ```python
     print("Hello".lower())  # Output: "hello"
     ```

### Kesimpulan

- String adalah salah satu tipe data penting di Python, terutama untuk analisis keamanan.
- Anda telah belajar:
  - Membuat string.
  - Operasi dasar seperti `len()` dan concatenation.
  - Menggunakan **method** seperti `upper()` dan `lower()`.
- Materi berikutnya akan membahas **indexing** dan **splitting strings** untuk manipulasi yang lebih lanjut.

Mari terus eksplorasi Python untuk menjadi security analyst yang lebih efektif! 🎉
