---
id: Data types in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Tipe Data dalam Python

### Apa Itu Tipe Data?

- **Tipe data** adalah kategori untuk jenis data tertentu.
- Dalam Python, tipe data digunakan untuk mengatur cara penanganan data.
- Contoh:
  - **String**: Data teks (karakter, huruf, simbol).
  - **Integer**: Angka bulat tanpa desimal.
  - **Float**: Angka dengan desimal.
  - **Boolean**: Hanya bernilai **True** atau **False**.
  - **List**: Kumpulan data dalam urutan tertentu.

---

### Penjelasan Tipe Data

#### 1. String

- **String** adalah data yang terdiri dari urutan karakter (huruf, simbol, spasi, angka).
- Ciri: Semua karakter dalam string harus diapit oleh tanda kutip (`"` atau `'`).
- **Catatan**: Angka dalam string **tidak bisa digunakan untuk perhitungan**.
- **Contoh**:
  ```python
  print("Hello Python!")  # Output: Hello Python!
  ```
- **Kesalahan umum**: Jika tanda kutip terlewat, Python akan memberikan pesan error.

---

#### 2. Numeric Data: Integer dan Float

- **Integer**: Angka bulat tanpa desimal (contoh: `0`, `-9`, `5000`).
- **Float**: Angka dengan desimal (contoh: `2.1`, `10.5`, `2.0`).
- Angka **tidak perlu tanda kutip**.
- Python dapat melakukan operasi matematika seperti:
  - Penjumlahan (`+`), Pengurangan (`-`), Perkalian (`*`), Pembagian (`/`).
- **Contoh**:
  ```python
  # Menambahkan angka
  print(1 + 1)  # Output: 2
  print(2.5 * 2)  # Output: 5.0
  ```

---

#### 3. Boolean

- **Boolean** hanya memiliki dua nilai: **True** atau **False**.
- Digunakan untuk **logika** dalam program, seperti perbandingan.
- **Contoh**:
  ```python
  print(10 < 5)  # Output: False
  print(9 < 12)  # Output: True
  ```

---

#### 4. List

- **List** adalah kumpulan data dalam urutan tertentu.
- Setiap elemen list dipisahkan dengan **koma** dan diapit oleh **bracket** (`[]`).
- Elemen dalam list bisa berupa string, angka, atau bahkan list lainnya.
- **Contoh**:
  ```python
  # Membuat dan mencetak list
  usernames = ["Alice", "Bob", "Charlie"]
  print(usernames)  # Output: ['Alice', 'Bob', 'Charlie']
  ```
- **Catatan**: List akan sering digunakan untuk menyimpan kumpulan data.

---

### Kesimpulan

- **Tipe data utama dalam Python**:
  1. **String**: Data teks.
  2. **Integer**: Angka bulat.
  3. **Float**: Angka desimal.
  4. **Boolean**: Nilai logika (True/False).
  5. **List**: Kumpulan data berurutan.
- Memahami tipe data sangat penting untuk memulai coding Python dan menyelesaikan berbagai masalah dengan efisien.

_"Dengan memahami tipe data, kamu bisa mulai membuat program Python yang lebih kompleks dan efisien!"_
