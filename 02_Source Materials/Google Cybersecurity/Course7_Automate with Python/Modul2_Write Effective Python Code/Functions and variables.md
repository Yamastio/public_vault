---
id: Functions and variables
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Variabel dan Fungsi di Python

### Parameter dan Argumen

- **Parameter**: Objek yang didefinisikan di header fungsi dan digunakan dalam tubuh fungsi. Contoh:

  ```python
  def remaining_login_attempts(maximum_attempts, total_attempts):
      print(maximum_attempts - total_attempts)
  ```

  Di sini, `maximum_attempts` dan `total_attempts` adalah parameter.

- **Argumen**: Data yang dikirim ke fungsi saat dipanggil. Contoh:
  ```python
  remaining_login_attempts(3, 2)
  ```
  Angka `3` dan `2` adalah argumen yang masuk ke parameter `maximum_attempts` dan `total_attempts`.

### Return Statement

- Kata kunci `return` digunakan untuk mengembalikan nilai dari fungsi.
  Contoh:
  ```python
  def remaining_login_attempts(maximum_attempts, total_attempts):
      return maximum_attempts - total_attempts
  ```
- Nilai yang dikembalikan dapat disimpan dalam variabel untuk digunakan kembali:
  ```python
  remaining_attempts = remaining_login_attempts(3, 3)
  if remaining_attempts <= 0:
      print("Your account is locked")
  ```

### Variabel Global dan Lokal

- **Global Variable**: Variabel yang didefinisikan di luar fungsi dan dapat diakses dari mana saja dalam program.
  Contoh:

  ```python
  device_id = "7ad2130bd"
  ```

  Variabel ini bisa dipakai di dalam atau di luar fungsi.

- **Local Variable**: Variabel yang didefinisikan di dalam fungsi dan hanya bisa diakses dalam fungsi tersebut.
  Contoh:
  ```python
  def greet_employee(name):
      total_string = "Welcome " + name
      return total_string
  ```

### Perbedaan Global dan Lokal

1. Variabel global tetap bisa diakses dalam fungsi, tapi bukan praktik terbaik jika mengganti nilainya di dalam fungsi.
2. Jika nama variabel global digunakan ulang di dalam fungsi, Python membuat variabel lokal baru tanpa mengubah nilai global.
   Contoh:

   ```python
   username = "elarson"
   print("1:", username)

   def greet():
       username = "bmoreno"
       print("2:", username)

   greet()
   print("3:", username)
   ```

   Hasil:

   - "1: elarson" (global)
   - "2: bmoreno" (lokal)
   - "3: elarson" (global)

#### Praktik Terbaik

- Hindari mencampur penggunaan variabel global dan lokal dalam fungsi.
- Gunakan parameter untuk memasukkan data ke fungsi daripada mengandalkan variabel global.

---

### Ringkasan

- **Parameter**: Variabel dalam definisi fungsi.
- **Argumen**: Data yang dikirim ke fungsi saat dipanggil.
- **Return**: Mengembalikan nilai dari fungsi.
- **Global Variable**: Dapat diakses di seluruh program.
- **Local Variable**: Hanya dapat diakses dalam fungsi tempat ia didefinisikan.
- **Tips**: Beri nama variabel yang unik untuk menghindari konflik antara variabel lokal dan global.
