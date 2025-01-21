---
id: Work with built-in functions
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Memahami Built-in Functions di Python

### Apa itu Built-in Functions?

Built-in functions adalah fungsi bawaan yang sudah tersedia di Python dan dapat langsung digunakan tanpa harus mendefinisikan ulang. Beberapa contoh built-in functions yang sering digunakan adalah `print()`, `type()`, `max()`, `min()`, dan `sorted()`.

---

### 1. `print()`

Fungsi `print()` digunakan untuk menampilkan objek ke layar.
**Ciri-ciri:**

- Menerima _arguments_ dalam jumlah tak terbatas.
- Dapat mencetak data dari berbagai tipe, baik string, angka, atau kombinasi keduanya.

**Contoh:**

```python
month = "September"
print("Investigate failed login attempts during", month, "if more than", 100)
```

Hasil:

```
Investigate failed login attempts during September if more than 100
```

---

### 2. `type()`

Fungsi `type()` mengembalikan tipe data dari sebuah objek.
**Ciri-ciri:**

- Hanya menerima satu _argument_.
- Sangat berguna untuk memastikan tipe data suatu variabel agar terhindar dari kesalahan kode.

**Contoh:**

```python
print(type("security"))  # Mengembalikan str
print(type(7))           # Mengembalikan int
```

Hasil:

```
<class 'str'>
<class 'int'>
```

---

### 3. Kombinasi Fungsi (Passing One Function to Another)

Hasil dari satu fungsi dapat dijadikan input fungsi lain.
**Contoh:**

```python
print(type("This is a string"))
```

- Fungsi `type()` diproses terlebih dahulu.
- Hasilnya (`<class 'str'>`) kemudian dicetak oleh fungsi `print()`.

---

### 4. `max()` dan `min()`

Fungsi `max()` mengembalikan nilai terbesar, sedangkan `min()` mengembalikan nilai terkecil.
**Ciri-ciri:**

- Bisa menerima banyak angka atau _iterable_ seperti list sebagai _argument_.

**Contoh:**

```python
time_list = [12, 2, 32, 19, 57, 22, 14]
print(min(time_list))  # Mengembalikan 2
print(max(time_list))  # Mengembalikan 57
```

Hasil:

```
2
57
```

---

### 5. `sorted()`

Fungsi `sorted()` digunakan untuk mengurutkan elemen dari sebuah _iterable_.
**Ciri-ciri:**

- Mengurutkan angka dari kecil ke besar.
- Mengurutkan string secara alfabetis.
- Tidak mengubah _iterable_ asli, hanya mengembalikan versi terurut.

**Contoh:**

```python
time_list = [12, 2, 32, 19, 57, 22, 14]
print(sorted(time_list))  # [2, 12, 14, 19, 22, 32, 57]
print(time_list)          # Tetap [12, 2, 32, 19, 57, 22, 14]
```

**Catatan Penting:**
Fungsi `sorted()` tidak dapat digunakan untuk _iterable_ dengan elemen dari tipe data campuran, misalnya `[1, 2, "hello"]`.

---

### **Kesimpulan**

- **`print()`**: Menampilkan objek ke layar.
- **`type()`**: Mengembalikan tipe data objek.
- **`max()` dan `min()`**: Mengembalikan nilai terbesar/kecil dari _iterable_.
- **`sorted()`**: Mengurutkan elemen dari _iterable_.

Python menyediakan berbagai built-in functions lain yang sangat bermanfaat. Untuk informasi lebih lanjut, silakan kunjungi dokumentasi [Python Standard Library](https://docs.python.org/3/library/functions.html).
