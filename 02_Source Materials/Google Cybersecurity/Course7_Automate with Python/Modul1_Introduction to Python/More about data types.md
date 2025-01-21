---
id: More about data types
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Tipe Data dalam Python

Tipe data adalah kategori untuk jenis data tertentu. Dalam Python, terdapat beberapa tipe data yang sering digunakan, yaitu **string**, **list**, **integer**, **float**, dan **Boolean**. Selain itu, ada tiga tipe tambahan: **tuple**, **dictionary**, dan **set**. Berikut adalah penjelasan sederhana tentang masing-masing tipe data:

---

### String

- **Pengertian**: Data berupa urutan karakter yang teratur. Karakter dapat berupa huruf, angka, simbol, atau spasi.
- **Ciri-ciri**: Harus ditulis di antara tanda kutip ("" atau '').
- **Contoh**:
  ```python
  "updates needed"
  "20%"
  "35"
  ""  # String kosong
  ```
- **Catatan**: Gunakan satu jenis tanda kutip secara konsisten untuk mempermudah membaca kode.

---

### List

- **Pengertian**: Struktur data berisi kumpulan data dalam urutan tertentu. Elemen dalam list bisa berupa tipe data apa saja (string, integer, Boolean, bahkan list lainnya).
- **Ciri-ciri**: Ditulis di dalam tanda kurung siku `[]` dan dipisahkan dengan koma.
- **Contoh**:
  ```python
  [12, 36, 54, 1, 7]
  ["eraab", "arusso", "drosas"]
  [True, False, True]
  []  # List kosong
  ```
- **Catatan**: List bersifat **mutable**, artinya isi elemen di dalamnya bisa diubah.

---

### Integer

- **Pengertian**: Angka bulat tanpa desimal.
- **Ciri-ciri**: Tidak perlu tanda kutip.
- **Contoh**:
  ```python
  -100, -12, 0, 20, 500
  ```
- **Fungsi tambahan**:
  - Operasi matematika seperti penjumlahan, pengurangan, perkalian, dan pembagian.
  - Contoh:
    ```python
    print(5 + 2)  # Output: 7
    ```

---

### Float

- **Pengertian**: Angka dengan desimal.
- **Ciri-ciri**: Tidak perlu tanda kutip.
- **Contoh**:
  ```python
  -2.2, 0.0, 3.14
  ```
- **Fungsi tambahan**:
  - Hasil pembagian dua bilangan (`/`) selalu menghasilkan float.
  - Gunakan `//` untuk mendapatkan hasil bilangan bulat.
  - Contoh:
    ```python
    print(1 / 4)  # Output: 0.25
    print(1 // 4)  # Output: 0
    ```

---

### Boolean

- **Pengertian**: Data logika dengan dua nilai: **True** atau **False**.
- **Ciri-ciri**: Tidak menggunakan tanda kutip.
- **Fungsi tambahan**: Digunakan untuk perbandingan logika.
- **Contoh**:
  ```python
  print(True)
  print(9 > 10)  # Output: False
  ```

---

### Tipe Data Tambahan

#### Tuple

- **Pengertian**: Struktur data berisi kumpulan data yang tidak bisa diubah (**immutable**).
- **Ciri-ciri**: Ditulis dengan tanda kurung biasa `()` dan elemen dipisahkan koma.
- **Contoh**:
  ```python
  ("wjaffrey", "arutley", "dkot")
  (46, 2, 13)
  (True, False, True)
  ```
- **Catatan**: Lebih efisien dalam penggunaan memori dibandingkan list.

#### Dictionary

- **Pengertian**: Data dalam format pasangan kunci-nilai (key-value).
- **Ciri-ciri**: Ditulis di dalam tanda kurung kurawal `{}` dengan tanda titik dua `:` antara kunci dan nilai.
- **Contoh**:
  ```python
  {1: "East", 2: "West", 3: "North"}
  ```
- **Kegunaan**: Mempermudah penyimpanan dan pengambilan data dengan cara yang terprediksi.

#### Set

- **Pengertian**: Kumpulan data yang tidak berurutan dan hanya berisi elemen unik.
- **Ciri-ciri**: Ditulis di dalam tanda kurung kurawal `{}` dan elemen dipisahkan koma.
- **Contoh**:
  ```python
  {"jlanksy", "drosas", "nmason"}
  ```

---

### Kesimpulan

- Tipe data yang umum digunakan: **string**, **list**, **integer**, **float**, dan **Boolean**.
- Tipe data tambahan: **tuple**, **dictionary**, dan **set**.
- Memahami tipe data mempermudah pengelolaan data saat membuat program Python.
