---
id: Conditional statements in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Memahami Conditional Statement di Python

### Pengantar Automasi

- **Automasi** adalah penggunaan teknologi untuk mengurangi usaha manual dalam melakukan tugas berulang.
- Contohnya, komputer bisa melakukan tugas tertentu secara otomatis sehingga kita punya lebih banyak waktu untuk kegiatan lain.

### Conditional Statement

- **Conditional statement** memungkinkan kita membuat logika di dalam kode, yaitu mengevaluasi apakah suatu kondisi terpenuhi (True) atau tidak (False).
- Kata kunci penting untuk conditional statement adalah `if`.
  - **if statement** digunakan untuk memulai pernyataan kondisi.
  - Misalnya:
    - Jika suhu dingin, maka kita pakai jaket.
    - Jika hujan, maka kita bawa payung.

### Struktur `if` Statement

1. **Header**: Baris pertama berisi kata kunci `if`, diikuti kondisi yang dicek, lalu diakhiri dengan tanda titik dua (`:`).
   Contoh:
   ```python
   if failed_attempts > 5:
   ```
2. **Body**: Baris berikutnya berisi aksi yang akan dilakukan jika kondisi bernilai True. Baris ini **harus diindentasi**.
   Contoh:
   ```python
       print("Account locked")
   ```

### Operator dalam Kondisi

- **Operator perbandingan**:
  - `>`: Lebih dari
  - `<`: Kurang dari
  - `>=`: Lebih dari atau sama dengan
  - `<=`: Kurang dari atau sama dengan
  - `==`: Sama dengan (gunakan **dua tanda sama dengan**)
  - `!=`: Tidak sama dengan
- **Boolean Value**:
  - Evaluasi kondisi menghasilkan **True** (benar) atau **False** (salah).

### Contoh `if` Statement

Kode berikut mengecek apakah jumlah login yang gagal lebih dari 5, dan jika ya, akan mencetak pesan:

```python
failed_attempts = 6

if failed_attempts > 5:
    print("Account locked")
```

### Menggunakan `else` Statement

- **else** digunakan untuk memberikan aksi jika kondisi dalam `if` tidak terpenuhi (False).
- Struktur:
  1. Tuliskan `else`, diikuti dengan titik dua (`:`).
  2. Indentasi aksi yang ingin dijalankan jika kondisi `if` False.

#### Contoh:

Kode berikut mengecek apakah sistem operasi adalah "OS 2". Jika tidak, akan memberikan pesan berbeda:

```python
operating_system = "OS 3"

if operating_system == "OS 2":
    print("Updates needed")
else:
    print("No updates needed")
```

- Hasil: Karena `operating_system` tidak sama dengan "OS 2", maka akan mencetak:
  ```
  No updates needed
  ```

### Kesimpulan

- **if statement** memungkinkan kita menjalankan aksi berdasarkan kondisi.
- **else statement** digunakan jika kondisi tidak terpenuhi.
- Dengan conditional statement, kita dapat menambahkan logika ke dalam kode dan membuat program lebih dinamis.

Cobalah menulis kode Anda sendiri dengan `if` dan `else` untuk memahami konsep ini lebih dalam!
