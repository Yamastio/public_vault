---
id: Ensure proper syntax and readability in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Panduan Menulis Kode Python yang Rapi dan Mudah Dibaca

### PEP 8 Style Guide

- **PEP 8** adalah panduan gaya yang memberikan rekomendasi penulisan kode Python agar mudah dipahami oleh programmer lain.
- Fokus PEP 8 meliputi **komentar**, **indentasi**, dan memperhatikan **syntax** agar kode berjalan dengan benar.

---

### Komentar (Comments)

- **Komentar** adalah catatan yang menjelaskan maksud kode untuk membantu pembaca memahami kode.
- Tambahkan komentar di awal program untuk menjelaskan tujuan umum, serta di bagian spesifik kode untuk memberikan konteks tambahan.

#### Jenis Komentar

1. **Single-line Comment**

   - Dimulai dengan simbol `#`.
   - Panjang maksimal satu baris disarankan di bawah **79 karakter**.
   - Contoh:
     ```python
     # Menampilkan elemen dalam daftar 'computer_assets'
     computer_assets = ["laptop1", "desktop20", "smartphone03"]
     for asset in computer_assets:
         print(asset)
     ```
   - Cocok untuk penjelasan bagian kode sederhana.

2. **Multi-line Comment**
   - Digunakan untuk penjelasan lebih panjang (lebih dari 79 karakter).
   - Dua metode:
     - Menggunakan beberapa baris `#`:
       ```python
       # Fungsi remaining_login_attempts() menerima dua parameter integer:
       # jumlah maksimum login yang diperbolehkan dan total login yang dilakukan.
       # Fungsi ini mengembalikan sisa jumlah percobaan login.
       def remaining_login_attempts(maximum_attempts, total_attempts):
           return maximum_attempts - total_attempts
       ```
     - Menggunakan **docstring** dengan tanda kutip tiga (`"""`):
       ```python
       """
       Fungsi remaining_login_attempts() menerima dua parameter integer:
       jumlah maksimum login yang diperbolehkan dan total login yang dilakukan.
       Fungsi ini mengembalikan sisa jumlah percobaan login.
       """
       ```

---

### Indentasi (Indentation)

- **Indentasi** adalah penambahan spasi di awal baris kode untuk menunjukkan hubungan antar baris.
- Penting untuk:
  1. Membuat kode lebih mudah dibaca.
  2. Memastikan Python mengeksekusi kode dengan benar.
- PEP 8 merekomendasikan **4 spasi** untuk setiap level indentasi.
- Contoh:
  ```python
  count = 0
  login_status = True
  while login_status:
      print("Coba lagi.")
      count += 1
      if count == 4:
          login_status = False
  ```

---

### Memastikan Syntax yang Benar

- **Error syntax** adalah kesalahan umum dalam Python. Memahami aturan berikut membantu menghindari error:

#### Tipe Data

- String: gunakan tanda kutip.
  ```python
  username = "bmoreno"
  ```
- Integer, Float, dan Boolean: **jangan gunakan tanda kutip**.
  ```python
  login_attempts = 5
  percentage_successful = 0.8
  login_status = True
  ```
- List: gunakan kurung siku `[]` dan pisahkan elemen dengan koma.
  ```python
  username_list = ["bmoreno", "tshah"]
  ```

#### Kolon (Colon) pada Header

- Tambahkan **colon (`:`)** di akhir header pernyataan kondisional, iteratif, atau definisi fungsi.
  ```python
  def remaining_login_attempts(maximum_attempts, total_attempts):
      return maximum_attempts - total_attempts
  ```

---

### Kesimpulan

- **PEP 8** membantu memastikan kode Python mudah dibaca dan dimengerti oleh programmer lain.
- Tambahkan **komentar** untuk menjelaskan maksud kode.
- Gunakan **indentasi** yang benar agar kode dapat dieksekusi sesuai rencana.
- Perhatikan **syntax umum** seperti tipe data dan penggunaan colon.

---

### Sumber Tambahan

- **PEP 8 - Style Guide for Python Code**
  Panduan lengkap PEP 8 untuk belajar praktik terbaik penulisan kode Python. Gunakan tabel isi untuk navigasi.
