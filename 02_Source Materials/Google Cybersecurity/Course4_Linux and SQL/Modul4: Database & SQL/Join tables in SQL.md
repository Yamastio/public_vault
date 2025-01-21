---
id: Join tables in SQL
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Bergabungnya Tabel dalam SQL (Joins)

Bergabung atau _joining_ tabel memungkinkan Anda menggabungkan data dari dua tabel yang berbeda dalam database. Ini sangat berguna untuk mengidentifikasi informasi gabungan, seperti mesin rentan di perusahaan Anda berdasarkan OS dan data pengguna.

### Konsep Dasar Joins

- **Menggunakan Nama Tabel dan Kolom**
  Ketika dua tabel memiliki nama kolom yang sama, gunakan format `tabel.kolom` untuk membedakan keduanya. Contoh:

  - `employees.employee_id` (dari tabel `employees`)
  - `machines.employee_id` (dari tabel `machines`)

- **Kolom Bersama (Primary Key dan Foreign Key)**
  - **Primary Key**: Unik untuk setiap baris di tabel (contoh: `employee_id` di `employees`).
  - **Foreign Key**: Menghubungkan ke primary key di tabel lain (contoh: `employee_id` di `machines`).

### INNER JOIN

#### Penjelasan

- **INNER JOIN** hanya mengembalikan baris yang memiliki nilai yang cocok di kedua tabel.
- Kolom yang digunakan untuk menyatukan adalah kolom yang sama di kedua tabel (contoh: `employee_id`).

#### Contoh Tabel

**employees**:
| employee_id | username | office |
|-------------|------------|---------|
| 1188 | John Smith | NY |
| 1189 | Jane Doe | LA |

**machines**:
| employee_id | operating_system |
|-------------|------------------|
| 1188 | Windows |
| 1189 | macOS |

Setelah _INNER JOIN_:
| username | office | operating_system |
|------------|--------|------------------|
| John Smith | NY | Windows |
| Jane Doe | LA | macOS |

#### Query INNER JOIN

```sql
SELECT username, office, operating_system
FROM employees
INNER JOIN machines
ON employees.employee_id = machines.employee_id;
```

- **Penjelasan Query**:
  1. **`FROM employees`**: Tabel pertama (_left table_).
  2. **`INNER JOIN machines`**: Tabel kedua (_right table_).
  3. **`ON employees.employee_id = machines.employee_id`**: Kondisi untuk mencocokkan baris.

### NULL dalam Joins

- **NULL** mewakili nilai yang hilang. Contoh: Mesin yang belum terhubung ke pengguna.
- _INNER JOIN_ tidak akan mengembalikan baris yang memiliki nilai `NULL` pada kolom yang cocok.

### Output Query

Hasil akan menampilkan hanya kolom yang diminta di bagian `SELECT`, dengan data gabungan dari kedua tabel.
