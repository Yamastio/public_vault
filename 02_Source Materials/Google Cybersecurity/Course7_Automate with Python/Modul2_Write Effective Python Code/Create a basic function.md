---
id: Create a basic function
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Membuat dan Menjalankan User-Defined Function di Python

### Apa Itu User-Defined Function?

- **User-defined function** adalah fungsi yang kita buat sendiri untuk melakukan tugas tertentu dalam program.
- Fungsi ini perlu **didefinisikan** terlebih dahulu sebelum bisa digunakan.

### Cara Mendefinisikan Function

1. **Gunakan Kata Kunci `def`**:
   - Kata kunci ini memberi tahu Python bahwa kita akan mendefinisikan sebuah fungsi.
2. **Beri Nama Fungsi**:
   - Nama fungsi harus menjelaskan tujuan fungsi tersebut.
   - Contoh: `greet_employee` (untuk menyapa karyawan setelah login).
3. **Tambahkan Tanda Kurung `()`**:
   - Tanda kurung dapat digunakan untuk menambahkan parameter (akan dibahas nanti). Untuk fungsi sederhana, biarkan kosong.
4. **Tambahkan Tanda Titik Dua `:`**:
   - Menandakan bahwa baris berikutnya adalah isi fungsi.
5. **Isi Fungsi**:
   - Tambahkan logika atau perintah yang akan dijalankan saat fungsi dipanggil.
   - Baris ini **harus diindentasi** untuk menunjukkan bahwa itu bagian dari fungsi.

#### Contoh:

```python
# Mendefinisikan fungsi untuk menyapa karyawan
def greet_employee():
    print("Selamat datang di sistem!")
```

### Memanggil Function

- Setelah fungsi didefinisikan, kita harus **memanggilnya** agar fungsi dapat dijalankan.
- Pemanggilan fungsi dilakukan dengan menuliskan nama fungsi diikuti tanda kurung `()`.

#### Contoh:

```python
# Memanggil fungsi greet_employee
greet_employee()
```

### Penjelasan Langkah-langkah

1. Mendefinisikan fungsi:
   - Kita memberi tahu Python bahwa fungsi `greet_employee` ada, tapi belum menjalankannya.
2. Memanggil fungsi:
   - Saat memanggil `greet_employee()`, Python menjalankan semua perintah di dalam fungsi tersebut.

### Kesimpulan

- Mendefinisikan fungsi hanyalah langkah awal. Fungsi tidak akan berjalan sampai kita memanggilnya.
- Fungsi sederhana seperti ini adalah dasar untuk membuat program yang lebih kompleks.

Mari kita lanjutkan untuk mempelajari bagaimana menambahkan parameter dan meningkatkan fungsionalitas fungsi! 🚀
