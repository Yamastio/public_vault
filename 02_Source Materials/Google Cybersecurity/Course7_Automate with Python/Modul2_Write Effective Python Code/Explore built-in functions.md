---
id: Explore built-in functions
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Mengenal Fungsi Built-in di Python

Fungsi built-in adalah fungsi bawaan Python yang dapat digunakan langsung tanpa perlu didefinisikan sebelumnya. Berikut ini adalah penjelasan tentang beberapa fungsi built-in yang umum digunakan:

### 1. **Fungsi `print()`**

- **Kegunaan**: Menampilkan objek atau output ke layar.
- **Input**: Menerima semua jenis data (string, integer, float, dll.).
- **Output**: Tidak mengembalikan nilai, hanya mencetak ke layar.
- **Contoh**:
  ```python
  print("Hello, World!")
  print("Data:", 42, "Type:", 3.14)
  ```

### 2. **Fungsi `type()`**

- **Kegunaan**: Menentukan tipe data dari sebuah objek.
- **Input**: Menerima satu parameter berupa data.
- **Output**: Mengembalikan tipe data dari input tersebut.
- **Contoh**:
  ```python
  print(type("security"))  # Output: <class 'str'>
  print(type(73.2))        # Output: <class 'float'>
  ```

### 3. **Menggabungkan Fungsi**

Fungsi dapat digunakan secara bersarang, yaitu output dari satu fungsi menjadi input fungsi lainnya.

- **Contoh**:
  ```python
  print(type("Hello"))  # Output: <class 'str'> dicetak ke layar
  ```

### 4. **Memahami Input dan Output**

- Beberapa fungsi membutuhkan parameter tertentu:
  - **`print()`**: Dapat menerima beberapa parameter, bahkan dari tipe data berbeda.
  - **`type()`**: Hanya menerima satu parameter.
- Penting untuk mengetahui jumlah parameter dan tipe data yang diterima setiap fungsi.

---

### 5. **Fungsi `max()`**

- **Kegunaan**: Mengembalikan nilai terbesar dari sekumpulan angka.
- **Input**: Menerima beberapa parameter angka.
- **Output**: Mengembalikan angka terbesar.
- **Contoh**:
  ```python
  a, b, c = 3, 9, 6
  print(max(a, b, c))  # Output: 9
  ```

### 6. **Fungsi `sorted()`**

- **Kegunaan**: Mengurutkan elemen dalam sebuah list.
- **Input**: Menerima list, baik berupa angka maupun string.
- **Output**: Mengembalikan list yang sudah terurut.
- **Contoh**:
  ```python
  usernames = ["alice", "bob", "charlie"]
  print(sorted(usernames))  # Output: ['alice', 'bob', 'charlie']
  ```

---

### 7. **Tips Menggunakan Fungsi Built-in**

- Pastikan memahami:
  - **Jumlah parameter** yang diperlukan.
  - **Jenis data** yang diterima.
  - **Jenis output** yang dihasilkan.
- Eksplorasi fungsi lain seperti `len()`, `sum()`, dan `round()` untuk memaksimalkan kemampuan Python.

Python memiliki banyak fungsi built-in yang siap digunakan, dan semakin sering Anda mempraktikkannya, semakin mahir Anda mengenal kegunaannya.
