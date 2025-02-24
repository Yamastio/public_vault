---
id: Operators for filtering dates and numbers
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Penyaringan Data Numerik dan Date/Time dengan Operator di SQL

### **Tipe Data yang Sering Digunakan dalam Keamanan Siber**

1. **Numerik**:

   - Jumlah login attempts.
   - Hitungan tipe log tertentu.
   - Volume data yang dikirim dari/destinasi tertentu.

2. **Date and Time**:
   - Timestamps dalam log.
   - Tanggal dan waktu login.
   - Tanggal patch.
   - Durasi koneksi.

### **Operator Perbandingan dalam SQL**

- `<` : **Less than** (kurang dari).
- `>` : **Greater than** (lebih besar dari).
- `=` : **Equal to** (sama dengan).
- `<=` : **Less than or equal to** (kurang dari atau sama dengan).
- `>=` : **Greater than or equal to** (lebih besar dari atau sama dengan).
- `<>` atau `!=` : **Not equal to** (tidak sama dengan).

### **Penerapan Operator dalam Filter SQL**

- **Contoh Penggunaan Operator `>`**
  Query:
  ```sql
  SELECT firstname, lastname, birthdate
  FROM employees
  WHERE birthdate > '1970-01-01';
  ```
  - Mengembalikan nama depan dan belakang karyawan yang lahir **setelah** 1 Januari 1970.
  - **Catatan**: Operator `>` **eksklusif**, sehingga nilai 1970-01-01 tidak termasuk. Jika menggunakan `>=`, maka nilai tersebut akan disertakan.

### **Operator BETWEEN**

- Digunakan untuk menyaring data dalam **rentang angka atau tanggal**.
- **Contoh Penggunaan BETWEEN**
  Query:
  ```sql
  SELECT firstname, lastname, hiredate
  FROM employees
  WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';
  ```
  - Mengembalikan nama depan dan belakang karyawan yang direkrut **antara** 1 Januari 2002 hingga 1 Januari 2003.
  - **Catatan**: Operator BETWEEN **inklusif**, sehingga kedua tanggal tersebut disertakan dalam hasil.

### **Kesimpulan Utama**

- Gunakan **operator eksklusif** seperti `<` untuk menyaring data tanpa menyertakan nilai pembanding.
- Gunakan **operator inklusif** seperti `<=` atau `BETWEEN` untuk menyaring data dengan menyertakan nilai pembanding.
- Operator sangat penting dalam menyaring data numerik dan date/time agar hasil query lebih spesifik dan relevan.
