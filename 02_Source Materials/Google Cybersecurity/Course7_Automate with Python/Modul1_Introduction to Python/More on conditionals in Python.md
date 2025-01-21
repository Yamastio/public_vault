---
id: More on conditionals in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Penjelasan tentang Conditional Statements di Python

### Apa itu Conditional Statement?

Conditional statement adalah pernyataan dalam kode yang digunakan untuk mengevaluasi suatu kondisi. Ketika kondisi terpenuhi (True), Python akan menjalankan tindakan tertentu. Jika tidak terpenuhi (False), Python tidak akan menjalankan tindakan tersebut.

- **Contoh kondisi sederhana:**
  - `status == 200` → Bernilai True jika `status` sama dengan 200.
- **Hasil evaluasi kondisi:** Boolean (`True` atau `False`).

---

### Operator Perbandingan

Operator ini sering digunakan untuk membandingkan nilai dalam conditional statement:

| Operator | Deskripsi                    |
| -------- | ---------------------------- |
| `>`      | lebih besar dari             |
| `<`      | lebih kecil dari             |
| `>=`     | lebih besar atau sama dengan |
| `<=`     | lebih kecil atau sama dengan |
| `==`     | sama dengan                  |
| `!=`     | tidak sama dengan            |

> **Catatan:** Operator `==` dan `!=` juga sering digunakan untuk membandingkan string.

---

### Struktur Dasar Conditional Statements

#### **`if` Statement**

Digunakan untuk memulai conditional statement. Jika kondisi bernilai True, Python akan menjalankan aksi dalam blok kode.

```python
if status == 200:
    print("OK")
```

- **Header:**
  - Dimulai dengan `if` diikuti oleh kondisi (`status == 200`).
  - Harus diakhiri dengan tanda titik dua (`:`).
- **Body:**
  - Tindakan yang dilakukan jika kondisi terpenuhi.
  - Harus di-_indent_ (dengan spasi atau tab).

---

#### **`else` Statement**

Digunakan untuk menentukan aksi jika kondisi dalam `if` bernilai False.

```python
if status == 200:
    print("OK")
else:
    print("check other status")
```

- **Header:**
  - Diawali dengan `else`, diakhiri dengan `:`.
- **Body:**
  - Harus di-_indent_ sama seperti blok `if`.

---

#### **`elif` Statement**

Digunakan untuk menambahkan kondisi tambahan. Python akan memeriksa kondisi dalam `elif` hanya jika kondisi sebelumnya bernilai False.

```python
if status == 200:
    print("OK")
elif status == 400:
    print("Bad Request")
elif status == 500:
    print("Internal Server Error")
else:
    print("check other status")
```

- Python hanya akan menjalankan satu blok `if`/`elif` yang pertama kali bernilai True.
- Gunakan `else` untuk menangani kondisi di luar yang sudah disebutkan.

---

### Operator Logika

Untuk menggabungkan lebih dari satu kondisi, Anda bisa menggunakan operator logika berikut:

#### **`and`**

Kedua kondisi di kiri dan kanan harus bernilai True.

```python
if status >= 200 and status <= 226:
    print("successful response")
```

#### **`or`**

Hanya salah satu kondisi di kiri atau kanan yang perlu bernilai True.

```python
if status == 100 or status == 102:
    print("informational response")
```

#### **`not`**

Membalikkan nilai dari suatu kondisi: True menjadi False, atau sebaliknya.

```python
if not (status >= 200 and status <= 226):
    print("check status")
```

> **Catatan:** Gunakan tanda kurung `()` agar Python tahu bahwa `not` diterapkan pada semua kondisi.

---

### Hal yang Penting Diperhatikan

- Gunakan titik dua (`:`) setelah `if`, `else`, dan `elif`.
- Blok kode (body) harus di-_indent_ agar Python tahu bagian mana yang dijalankan.
- Python akan menghentikan evaluasi pada `elif` pertama yang bernilai True.

---

### Kesimpulan

- **Kata kunci utama:** `if`, `else`, `elif`.
- **Operator logika:** `and`, `or`, `not` untuk kondisi yang lebih kompleks.
- **Praktik terbaik:** Gunakan tanda kurung `()` untuk meningkatkan keterbacaan dan memastikan evaluasi kondisi yang benar.

Dengan memahami conditional statements, Anda dapat membuat program Python yang lebih fleksibel dan dinamis.
