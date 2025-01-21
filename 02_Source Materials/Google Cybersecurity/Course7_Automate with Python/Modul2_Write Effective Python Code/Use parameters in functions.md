---
id: Use parameters in functions
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Menggunakan Parameter dalam Fungsi di Python

Di Python, parameter adalah **objek** yang didefinisikan dalam sebuah fungsi untuk digunakan di dalam fungsi tersebut. Parameter ini diterima melalui tanda kurung `()` setelah nama fungsi.

### Fungsi Tanpa Parameter

Pada contoh sebelumnya, kita membuat fungsi sederhana yang tidak menggunakan parameter. Namun, banyak fungsi yang memerlukan informasi tambahan dari luar untuk berfungsi. Contohnya adalah fungsi **`range()`**, yang memerlukan parameter untuk menentukan:

- **Start**: Titik awal urutan.
- **Stop**: Titik akhir urutan (nilai sebelum titik ini).

Sebagai contoh:
`range(3, 7)` akan menghasilkan urutan **3, 4, 5, 6**.

### Menambahkan Parameter ke Fungsi

Kita dapat membuat fungsi yang lebih fleksibel dengan menambahkan parameter. Misalnya, untuk menyapa karyawan dengan nama mereka, kita dapat membuat fungsi dengan parameter.

#### Langkah Membuat Fungsi dengan Parameter

1. **Definisi Fungsi**
   Tambahkan nama parameter ke dalam tanda kurung setelah nama fungsi:

   ```python
   def greet_employee(name):
   ```

2. **Isi Fungsi**
   Tulis perintah yang memanfaatkan parameter tersebut. Misalnya, untuk menyapa karyawan:

   ```python
       print("You're logged in,", name)
   ```

3. **Memanggil Fungsi**
   Ketika memanggil fungsi, tambahkan **argument** (data yang akan dimasukkan ke parameter):
   ```python
   greet_employee("Charley Patel")
   ```
   Output:
   `You're logged in, Charley Patel`

### Menggunakan Lebih dari Satu Parameter

Fungsi juga bisa menerima lebih dari satu parameter. Sebagai contoh, kita ingin menyapa karyawan menggunakan nama depan dan nama belakang.

#### Langkah Membuat Fungsi dengan Beberapa Parameter

1. **Definisi Fungsi**
   Tambahkan lebih dari satu parameter, dipisahkan dengan koma:

   ```python
   def greet_employee(first_name, last_name):
   ```

2. **Isi Fungsi**
   Gunakan kedua parameter di dalam perintah:

   ```python
       print("Welcome,", first_name, last_name)
   ```

3. **Memanggil Fungsi**
   Saat memanggil fungsi, tambahkan argument untuk setiap parameter:
   ```python
   greet_employee("Kiara", "Carter")
   ```
   Output:
   `Welcome, Kiara Carter`

### Penjelasan Tambahan

- **Parameter**: Objek dalam definisi fungsi.
- **Argument**: Data yang diberikan saat fungsi dipanggil.

### Kesimpulan

- Parameter memungkinkan fungsi menjadi lebih fleksibel.
- Untuk fungsi dengan lebih dari satu parameter, cukup pisahkan dengan koma saat mendefinisikan dan memanggil fungsi.
- Memahami penggunaan parameter sangat penting dalam penulisan Python script.

Contoh lengkap:

```python
def greet_employee(first_name, last_name):
    print("Welcome,", first_name, last_name)

greet_employee("Kiara", "Carter")
```

Dengan memahami ini, Anda dapat membuat fungsi yang lebih dinamis dan dapat menangani berbagai skenario!
