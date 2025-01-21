---
id: List operations in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## List di Python: Dasar dan Penggunaannya

### Apa itu List?

- **List** adalah tipe data di Python yang memungkinkan kita menyimpan banyak data dalam satu variabel.
- Dalam dunia **security**, list sering digunakan, misalnya:
  - **Daftar IP** yang mengakses jaringan.
  - **Daftar aplikasi** yang diblokir dari sistem.

### Cara Membuat List

- List dibuat dengan **menempatkan elemen di dalam tanda kurung siku (`[]`)** dan memisahkannya dengan koma.
- Contoh:
  ```python
  my_list = ['A', 'B', 'C', 'D', 'E']
  ```

### Akses Elemen dalam List

- Menggunakan **index** (dimulai dari 0).
  - Contoh: Akses elemen kedua.
    ```python
    print(my_list[1])  # Output: 'B'
    ```

### Operasi pada List

#### 1. **Konkatenasi (Concatenation)**

- **Menggabungkan dua list** menggunakan tanda `+`.
- Contoh:
  ```python
  list1 = ['A', 'B', 'C']
  list2 = [1, 2, 3]
  result = list1 + list2
  print(result)  # Output: ['A', 'B', 'C', 1, 2, 3]
  ```

#### 2. **Mengubah Elemen List**

- Tidak seperti **string** (yang immutable), list bersifat **mutable** sehingga bisa diubah.
- Contoh: Ubah elemen kedua menjadi angka 7.
  ```python
  my_list[1] = 7
  print(my_list)  # Output: ['A', 7, 'C', 'D', 'E']
  ```

#### 3. **Menambah Elemen dengan `insert`**

- Gunakan metode `.insert(index, elemen)` untuk menambah elemen pada posisi tertentu.
- Contoh: Tambahkan angka 7 di index ke-1.
  ```python
  my_list.insert(1, 7)
  print(my_list)  # Output: ['A', 7, 'B', 'C', 'D', 'E']
  ```
- **Catatan:** Elemen setelah index tersebut akan **bergeser**.

#### 4. **Menghapus Elemen dengan `remove`**

- Gunakan metode `.remove(elemen)` untuk menghapus elemen tertentu.
- Contoh: Hapus elemen `'D'`.
  ```python
  my_list.remove('D')
  print(my_list)  # Output: ['A', 'B', 'C', 'E']
  ```
- **Catatan:** Metode ini hanya menghapus **kemunculan pertama** elemen yang sesuai.

### Pentingnya List untuk Security

- List sangat berguna untuk menyimpan data dinamis, misalnya:
  - Menambahkan IP **malicious** yang terdeteksi ke dalam daftar.
  - Mencari elemen tertentu untuk analisis keamanan.

Dengan memahami cara kerja list, kita dapat mengelola data lebih efektif dan efisien dalam pekerjaan sehari-hari sebagai security analyst.
