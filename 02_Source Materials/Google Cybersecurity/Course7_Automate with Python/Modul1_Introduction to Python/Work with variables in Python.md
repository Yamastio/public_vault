---
id: Work with variables in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Variabel dalam Python

Ketika bekerja dengan data dalam Python, kita menggunakan **variabel** sebagai wadah untuk menyimpan data, mirip dengan wadah yang kita gunakan di dapur untuk menyimpan bahan makanan. Berikut adalah poin-poin penting tentang variabel dalam Python:

### Apa itu Variabel?

- Variabel adalah **wadah** yang digunakan untuk menyimpan data.
- Kita membuat variabel dengan:
  - Memberikan **nama variabel**.
  - Menggunakan tanda **sama dengan (`=`)** untuk melakukan **assignment**.
  - Menyimpan data (disebut sebagai **objek**) di dalamnya.

### Contoh Pembuatan Variabel

```python
device_ID = "h32rb17"  # Variabel menyimpan string
```

- Nama variabel sebaiknya relevan dengan data yang disimpan agar mudah dibaca.
- String (teks) disimpan dengan tanda **kutip**.

### Memanggil Variabel

- Untuk menggunakan variabel, cukup tuliskan **nama variabel**.
  Contoh:
  ```python
  print(device_ID)  # Output: h32rb17
  ```
- Saat memanggil variabel dalam fungsi `print`, **jangan gunakan tanda kutip**.

### Perbedaan Memanggil String Langsung dan Variabel

Contoh kode:

```python
print(device_ID)   # Memanggil variabel
print("m50pi31")   # Memanggil string langsung
```

Hasil:

- Baris pertama mencetak nilai dari variabel `device_ID`.
- Baris kedua mencetak string literal.

**Kenapa menggunakan variabel?**

- Mempermudah penulisan kode, terutama jika data panjang atau digunakan berulang kali.
- Membuat kode lebih bersih dan mudah dibaca.

---

## Data Type pada Variabel

- Variabel dapat menyimpan **berbagai jenis data**, seperti:
  - **String**: Teks di dalam tanda kutip.
  - **Integer**: Angka tanpa desimal.
  - **Float**: Angka dengan desimal.
  - **Boolean**: Nilai `True` atau `False`.
  - **List**: Kumpulan data.

### Mengecek Data Type

- Gunakan fungsi `type()` untuk mengetahui tipe data yang disimpan.
  Contoh:

```python
device_ID = "h32rb17"
data_type = type(device_ID)
print(data_type)  # Output: <class 'str'>
```

---

## Error Tipe Data

- Jika tipe data tidak sesuai, Python akan menghasilkan **TypeError**.
- Contoh kesalahan:

```python
device_ID = "h32rb17"  # String
number = 42            # Integer
print(device_ID + number)  # Error: tidak bisa menambahkan string dengan integer
```

---

## Reassignment (Mengubah Isi Variabel)

- Variabel bisa diubah isinya setelah didefinisikan.
- Contoh:

```python
device_ID = "h32rb17"   # Awal
print(device_ID)        # Output: h32rb17

device_ID = "n73ab07"   # Reassignment
print(device_ID)        # Output: n73ab07
```

- Variabel juga bisa diubah ke tipe data lain:

```python
device_ID = 12345  # Variabel diubah dari string ke integer
```

---

## Kesimpulan

- Variabel adalah elemen penting dalam Python untuk menyimpan data.
- Mereka dapat menyimpan berbagai tipe data dan isinya bisa diubah kapan saja.
- Dengan memahami variabel, kita bisa membuat kode lebih bersih, efisien, dan mudah dibaca.
