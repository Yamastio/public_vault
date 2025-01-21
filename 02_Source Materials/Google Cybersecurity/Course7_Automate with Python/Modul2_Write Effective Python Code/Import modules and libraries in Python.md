---
id: Import modules and libraries in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Import Modules dan Libraries di Python

### Pengantar

- **Module**: File Python yang berisi fungsi, variabel, kelas, dan kode lain yang bisa dijalankan.
- **Library**: Kumpulan module yang menyediakan kode siap pakai untuk program.
- **Python Standard Library**: Koleksi module bawaan Python untuk berbagai tugas umum.
- **External Library**: Library yang diunduh dari luar Python Standard Library.

---

### Python Standard Library

Beberapa module populer dalam Python Standard Library:

- **re**: Mencari pola dalam file log.
- **csv**: Bekerja dengan file `.csv`.
- **glob** dan **os**: Berinteraksi dengan command line.
- **time** dan **datetime**: Bekerja dengan timestamp.
- **statistics**: Menghitung statistik numerik seperti **mean()** (rata-rata) dan **median()** (nilai tengah).

---

### Cara Mengimpor Module di Python

#### Mengimpor Seluruh Module

- Gunakan kata kunci `import`.
- Semua fungsi dalam module akan tersedia, tetapi harus dipanggil menggunakan nama module.

Contoh:

```python
import statistics

monthly_failed_attempts = [20, 17, 178, 33, 15, 21, 19, 29, 32, 15, 25, 19]
mean_failed_attempts = statistics.mean(monthly_failed_attempts)
print("mean:", mean_failed_attempts)
```

Output:

```
mean: 35.25
```

#### Mengimpor Fungsi Tertentu dari Module

- Gunakan `from` dan `import` untuk memilih fungsi tertentu.
- Tidak perlu menyebutkan nama module saat memanggil fungsi.

Contoh:

```python
from statistics import mean, median

monthly_failed_attempts = [20, 17, 178, 33, 15, 21, 19, 29, 32, 15, 25, 19]
mean_failed_attempts = mean(monthly_failed_attempts)
print("mean:", mean_failed_attempts)

median_failed_attempts = median(monthly_failed_attempts)
print("median:", median_failed_attempts)
```

Output:

```
mean: 35.25
median: 20.5
```

---

### External Libraries

- Harus diinstal sebelum digunakan.
- Contoh library eksternal:
  - **Beautiful Soup**: Parsing file HTML.
  - **NumPy**: Array dan perhitungan matematika.

#### Cara Instalasi

Gunakan perintah berikut sebelum impor:

```python
%pip install numpy
```

Setelah diinstal, library dapat diimpor seperti module bawaan:

```python
import numpy
```

---

### Intisari

- **Python Standard Library** menyediakan module seperti `re`, `csv`, `os`, `time`, dan `statistics`.
- **Syntax Import**:
  - Import seluruh module: `import nama_module`
  - Import fungsi tertentu: `from nama_module import fungsi`
- **External Libraries** perlu diinstal terlebih dahulu sebelum digunakan.
