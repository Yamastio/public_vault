---
id: Assign and reassign variables in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Variabel dalam Python

### Apa itu Variabel?

- **Variabel** adalah wadah untuk menyimpan data dalam program.
- Variabel diberi nama untuk mewakili lokasi penyimpanan di memori komputer.
- Data yang disimpan memiliki **tipe data**, seperti `integer`, `string`, atau `Boolean`.
- Nilai dalam variabel dapat diubah kapan saja.

**Analogi:** Variabel seperti kotak berlabel. Isi kotak (nilai variabel) bisa berubah, tapi labelnya tetap sama.

**Contoh Penggunaan oleh Security Analyst:**

- Menyimpan jumlah percobaan login (`login_attempts`).
- Daftar yang diizinkan (`allow_list`).
- Alamat IP (`addresses`).

---

### Cara Menggunakan Variabel

#### 1. **Membuat Variabel (Assignment)**

Untuk membuat variabel, tempatkan nama variabel di kiri tanda sama dengan (`=`), dan nilai di kanannya.

```python
username = "nzhao"  # Contoh variabel dengan nilai string
```

#### 2. **Mengubah Nilai Variabel (Reassignment)**

Nilai dalam variabel dapat diubah tanpa mengganti nama variabelnya.

```python
username = "zhao2"  # Variabel username sekarang berisi "zhao2"
```

#### 3. **Menetapkan Variabel ke Variabel Lain**

Anda dapat menggunakan variabel untuk menetapkan nilai ke variabel lain:

```python
username = "nzhao"
old_username = username  # old_username berisi nilai "nzhao"
```

#### 4. **Contoh Lengkap**

Berikut adalah contoh kode Python yang memperbarui nama pengguna:

```python
username = "nzhao"
old_username = username
username = "zhao2"
print("Previous username:", old_username)
print("Current username:", username)
```

Hasil output:

```
Previous username: nzhao
Current username: zhao2
```

---

### Praktik Terbaik Penamaan Variabel

Agar kode mudah dipahami dan tidak menghasilkan error, ikuti pedoman berikut:

#### **Panduan Sintaks:**

1. Gunakan **huruf**, **angka**, dan **garis bawah (\_)** saja.
   - Contoh valid: `date_3`, `username`, `interval2`
2. Nama variabel bersifat **case-sensitive**.
   - `time`, `Time`, dan `TIME` adalah variabel berbeda.
3. Jangan gunakan **kata kunci bawaan Python** sebagai nama variabel.
   - Contoh: Hindari menggunakan `True`, `False`, atau `if`.

#### **Panduan Gaya Penulisan:**

1. Gunakan **garis bawah** untuk memisahkan kata.
   - Contoh: `login_attempts`, `invalid_user`.
2. Hindari nama yang terlalu mirip.
   - Contoh buruk: `start_time`, `starting_time`, `time_starting`.
3. Jangan gunakan nama variabel yang terlalu panjang.
   - Contoh buruk: `variable_that_equals_3`.
4. Nama variabel harus menjelaskan data yang disimpan, bukan kata acak.
   - Contoh baik: `num_login_attempts`, `device_id`.

**Catatan:**
Alternatif lain untuk pemisahan kata adalah menggunakan format **CamelCase**:

- Contoh: `loginAttempt`

Meskipun CamelCase tidak dilarang untuk variabel di Python, sebaiknya gunakan snake_case untuk mematuhi standar PEP 8 dan menjaga konsistensi dengan gaya penulisan Python yang umum digunakan.

---

### Poin Penting

1. **Variabel adalah wadah data** yang nilainya dapat berubah.
2. **Assignment dan reassignment** memungkinkan Anda menyimpan dan mengubah data.
3. **Penamaan variabel yang baik** membantu membuat kode lebih jelas, fungsional, dan mudah dipahami.

Selamat mencoba!
