---
id: "Activity: Assign Python variables"
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Aktivitas: Menetapkan Variabel Python

### Pendahuluan

Variabel membantu analis keamanan melacak berbagai informasi terkait keamanan. Misalnya, variabel dapat digunakan untuk menyimpan daftar pengguna yang diizinkan login, jumlah maksimal percobaan login, jumlah percobaan login saat ini, dan status login.

Dalam lab ini, kita akan mempraktikkan penetapan nilai pada variabel dan menentukan tipe datanya.

---

### **Tips untuk Menyelesaikan Lab**

1. Pahami skenario dan tugas dengan jelas.
2. Gunakan fungsi bawaan Python untuk mempermudah pekerjaan.
3. Ganti placeholder `### YOUR CODE HERE ###` dengan kode Python yang sesuai.

---

### **Skenario**

Sebagai analis keamanan, Anda perlu menulis kode untuk menganalisis percobaan login pada perangkat tertentu. Langkah pertama adalah membuat variabel untuk melacak informasi yang relevan, seperti:

- ID perangkat,
- daftar pengguna yang diizinkan (allow list),
- jumlah maksimal percobaan login,
- jumlah percobaan login saat ini,
- status login.

---

### **Task 1: Menetapkan Variabel `device_id`**

Tugas: Tetapkan nilai `"72e08x0"` pada variabel `device_id` dan tampilkan isinya.

```python
device_id = "72e08x0"
print(device_id)
```

---

### **Task 2: Menentukan Tipe Data `device_id`**

Tugas: Gunakan fungsi `type()` untuk menentukan tipe data `device_id`, lalu simpan hasilnya pada variabel `device_id_type` dan tampilkan.

```python
device_id_type = type(device_id)
print(device_id_type)
```

**Pertanyaan 1:** Apa tipe data dari `device_id`?

> Tipe data `device_id` adalah `str` (string), karena menyimpan nilai berupa teks.

---

### **Task 3: Membuat Daftar `username_list`**

Tugas: Buat variabel `username_list` yang berisi daftar pengguna yang diizinkan: `"madebowa"`, `"jnguyen"`, `"tbecker"`, `"nhersh"`, dan `"redwards"`. Tampilkan isi daftar tersebut.

```python
username_list = ["madebowa", "jnguyen", "tbecker", "nhersh", "redwards"]
print(username_list)
```

---

### **Task 4: Menentukan Tipe Data `username_list`**

Tugas: Gunakan fungsi `type()` untuk menentukan tipe data `username_list`, simpan pada variabel `username_list_type`, dan tampilkan.

```python
username_list_type = type(username_list)
print(username_list_type)
```

**Pertanyaan 2:** Apa tipe data dari `username_list`?

> Tipe data `username_list` adalah `list`, karena menyimpan kumpulan nilai dalam bentuk daftar.

---

### **Task 5: Memperbarui Daftar `username_list`**

Tugas: Tambahkan pengguna baru `"lpope"` ke dalam daftar. Tampilkan isi daftar sebelum dan sesudah diperbarui.

```python
# Sebelum diperbarui
username_list = ["madebowa", "jnguyen", "tbecker", "nhersh", "redwards"]
print(username_list)

# Setelah diperbarui
username_list = ["madebowa", "jnguyen", "tbecker", "nhersh", "redwards", "lpope"]
print(username_list)
```

**Pertanyaan 3:** Apa yang berubah dalam daftar setelah diperbarui?

> Daftar diperbarui dengan menambahkan satu elemen baru di bagian akhir.

---

### **Task 6: Menetapkan Variabel `max_logins`**

Tugas: Tetapkan nilai `3` pada variabel `max_logins`. Tentukan tipe datanya menggunakan `type()`, simpan pada variabel `max_logins_type`, dan tampilkan.

```python
max_logins = 3
max_logins_type = type(max_logins)
print(max_logins_type)
```

**Pertanyaan 4:** Apa tipe data dari `max_logins`?

> Tipe data `max_logins` adalah `int`, karena menyimpan bilangan bulat.

---

### **Task 7: Menetapkan Variabel `login_attempts`**

Tugas: Tetapkan nilai `2` pada variabel `login_attempts`. Tentukan tipe datanya menggunakan `type()`, simpan pada variabel `login_attempts_type`, dan tampilkan.

```python
login_attempts = 2
login_attempts_type = type(login_attempts)
print(login_attempts_type)
```

**Pertanyaan 5:** Apa tipe data dari `login_attempts`?

> Tipe data `login_attempts` adalah `int`.

---

### **Task 8: Membandingkan `max_logins` dan `login_attempts`**

Tugas: Tentukan apakah nilai `login_attempts` kurang dari atau sama dengan `max_logins`. Tampilkan hasil perbandingan dalam bentuk Boolean.

```python
max_logins = 3
login_attempts = 2
print(login_attempts <= max_logins)
```

**Pertanyaan 6:** Apa arti output yang dihasilkan?

> Output berupa `True`, yang berarti jumlah percobaan login saat ini (2) masih dalam batas maksimal yang diizinkan (3).

---

### **Task 9: Mengubah Nilai `login_attempts`**

Tugas: Ubah nilai `login_attempts` ke angka yang lebih tinggi dari `max_logins` (misalnya 4). Amati bagaimana hasil perbandingan berubah.

```python
max_logins = 3
login_attempts = 4
print(login_attempts <= max_logins)
```

**Pertanyaan 7:** Apa yang Anda amati dari perubahan nilai?

> Ketika `login_attempts` lebih besar dari `max_logins`, output menjadi `False`, menunjukkan bahwa batas telah terlampaui.

---

### **Task 10: Menetapkan Variabel Boolean `login_status`**

Tugas: Tetapkan nilai `False` pada variabel `login_status`. Tentukan tipe datanya menggunakan `type()`, simpan pada variabel `login_status_type`, dan tampilkan.

```python
login_status = False
login_status_type = type(login_status)
print(login_status_type)
```

**Pertanyaan 8:** Apa tipe data dari `login_status`?

> Tipe data `login_status` adalah `bool`, karena menyimpan nilai Boolean (`True` atau `False`).

---

### **Kesimpulan**

- **String (`str`)**: Digunakan untuk menyimpan teks, seperti ID perangkat.
- **List (`list`)**: Digunakan untuk menyimpan kumpulan nilai, seperti daftar pengguna.
- **Integer (`int`)**: Digunakan untuk menyimpan bilangan bulat, seperti batas login atau percobaan login.
- **Boolean (`bool`)**: Digunakan untuk menyimpan nilai logika `True` atau `False`.

Dengan memahami tipe data ini, Anda dapat menyusun logika dan mengelola informasi keamanan dengan lebih efisien.
