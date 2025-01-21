---
id: For loops
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Iterative Statements: For Loops

Dalam pemrograman, terkadang kita membutuhkan program untuk melakukan tugas berulang. Tugas-tugas yang membosankan sering kali membuat manusia kehilangan fokus, tetapi komputer bisa melakukan tugas berulang tanpa lelah menggunakan **iterative statements** atau yang sering disebut **loops**.

### Apa itu Iterative Statements?

- **Iterative statement** adalah kode yang menjalankan serangkaian instruksi secara berulang.
- Contoh: Jika kita ingin mencetak semua angka dalam sebuah daftar, kita dapat menggunakan loop untuk melakukannya tanpa harus menulis banyak perintah `print`.

### Jenis Loop

Ada dua jenis loop yang akan kita pelajari:

1. **For loop** (dibahas dalam video ini)
2. **While loop** (dibahas di video berikutnya)

### Apa itu For Loop?

- **For loop** digunakan untuk mengulangi kode berdasarkan urutan tertentu.
- Contoh: Mencetak semua elemen dalam sebuah **list**.

### Struktur For Loop

For loop terdiri dari dua bagian utama:

1. **Loop header**: Baris kode yang dimulai dengan kata kunci `for` dan diakhiri dengan tanda titik dua (`:`).
   - Komponen dalam loop header:
     - Kata kunci `for`: Menandakan dimulainya loop.
     - **Loop variable**: Variabel sementara yang digunakan untuk iterasi. Biasanya diberi nama `i`, tetapi bisa menggunakan nama lain.
     - Operator `in`: Digunakan untuk menunjukkan urutan yang akan diiterasi.
     - **Sequence**: Urutan nilai yang akan dilewati oleh loop (contoh: list, range).
2. **Loop body**: Baris kode yang berada di bawah loop header dan diindentasi.
   - Loop body berisi tindakan yang akan dilakukan berulang kali selama loop berjalan.

### Contoh For Loop

```python
for i in [1, 2, 3, 4]:
    print(i)
```

- **Loop header**: `for i in [1, 2, 3, 4]:`
  - Loop ini akan mengiterasi angka 1 hingga 4.
- **Loop body**: `print(i)`
  - Tindakan ini mencetak nilai `i` pada setiap iterasi.

Hasilnya: Loop akan mencetak angka 1, 2, 3, dan 4 satu per satu.

### For Loop dengan Fungsi Range

Fungsi **range** digunakan untuk membuat urutan angka dengan mudah.

- Sintaks: `range(start, stop)`
  - **Start**: Titik awal (opsional, default adalah 0).
  - **Stop**: Titik akhir (angka ini tidak termasuk dalam urutan).

Contoh:

```python
for i in range(10):
    print(i)
```

- Loop akan mencetak angka dari 0 hingga 9 (10 iterasi).

### Contoh Penggunaan For Loop dengan Range

Untuk mengulangi suatu proses beberapa kali:

```python
for i in range(10):
    print("Cannot connect to the destination.")
```

- Loop ini mencetak pesan kesalahan sebanyak 10 kali tanpa harus mengetik ulang perintah `print`.

### Kesimpulan

- **For loop** mempermudah pengulangan tugas dalam kode.
- **Loop header** menentukan iterasi, sedangkan **loop body** menentukan tindakan yang akan diulang.
- Menggunakan **range** sangat berguna untuk pengulangan berbasis angka.
- Dengan for loop, kita dapat menghemat waktu dan usaha, terutama dalam tugas-tugas berulang.

Pada video berikutnya, kita akan mempelajari **while loop** untuk skenario lain yang melibatkan pengulangan.
