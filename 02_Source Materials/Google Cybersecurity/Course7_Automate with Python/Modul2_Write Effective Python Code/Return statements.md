---
id: Return statements
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Menggunakan Return Statement dalam Fungsi di Python

Selain **memasukkan argument** ke dalam fungsi, kita juga bisa **mengirimkan informasi keluar** dari fungsi menggunakan **return statement**. Return statement adalah perintah di Python yang digunakan untuk mengembalikan nilai dari fungsi ke pemanggil fungsi. Fitur ini sangat berguna dalam banyak skenario, seperti menganalisis data atau membuat keputusan logis.

### Contoh Penggunaan

Misalnya, seorang analis keamanan dapat membuat fungsi untuk memeriksa apakah seseorang diizinkan mengakses file tertentu, dan fungsi tersebut akan **mengembalikan nilai Boolean** (`True` atau `False`).

Kita akan mempelajari lebih lanjut dengan contoh fungsi yang menghitung **persentase login gagal**.

---

### Membuat Fungsi dengan Return Statement

1. **Definisi Fungsi**
   Kita mulai dengan mendefinisikan fungsi bernama `calculate_fails()` yang menerima dua parameter:

   - **`total_attempts`**: Jumlah total percobaan login.
   - **`failed_attempts`**: Jumlah percobaan login yang gagal.

   ```python
   def calculate_fails(total_attempts, failed_attempts):
   ```

2. **Menghitung Persentase**
   Hitung persentase login gagal dan simpan hasilnya dalam variabel `fail_percentage`:

   ```python
       fail_percentage = failed_attempts / total_attempts
   ```

3. **Mengembalikan Nilai dengan Return Statement**
   Gunakan perintah `return` untuk mengembalikan nilai `fail_percentage`:

   ```python
       return fail_percentage
   ```

4. **Memanggil Fungsi**
   Saat memanggil fungsi, masukkan nilai sebagai argument, misalnya 4 untuk `total_attempts` dan 2 untuk `failed_attempts`:

   ```python
   calculate_fails(4, 2)
   ```

   Fungsi akan mengembalikan nilai `0.5` atau **50%**.

---

### Menggunakan Nilai yang Dikembalikan

Agar nilai yang dikembalikan dapat digunakan di bagian program lain:

- Simpan nilai tersebut dalam variabel baru.
- Contoh:
  ```python
  percentage = calculate_fails(4, 2)
  ```

Variabel `percentage` sekarang menyimpan nilai `0.5`.

---

### Contoh Lengkap: Penguncian Akun Otomatis

Berikut adalah contoh lengkap yang menggunakan nilai yang dikembalikan untuk menentukan apakah akun harus dikunci:

```python
def calculate_fails(total_attempts, failed_attempts):
    fail_percentage = failed_attempts / total_attempts
    return fail_percentage

# Memanggil fungsi dan menyimpan nilai yang dikembalikan
percentage = calculate_fails(4, 2)

# Mengecek apakah persentase login gagal >= 50%
if percentage >= 0.5:
    print("Account locked")
```

**Penjelasan**:

- Fungsi `calculate_fails()` menghitung persentase login gagal.
- Nilai yang dikembalikan disimpan dalam variabel `percentage`.
- Jika persentase login gagal lebih besar atau sama dengan 50%, program mencetak pesan **"Account locked"**.

---

### Kesimpulan

- **Return statement** memungkinkan fungsi mengirimkan data keluar untuk digunakan di bagian program lainnya.
- Nilai yang dikembalikan dapat disimpan dalam variabel untuk keperluan lebih lanjut.
- Contoh di atas menunjukkan bagaimana nilai dari fungsi dapat digunakan untuk membuat keputusan logis dalam program Python.

Dengan memahami ini, Anda dapat membuat fungsi yang lebih kompleks dan fleksibel!
