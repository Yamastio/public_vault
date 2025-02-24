---
id: Types of joins
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Jenis-Jenis Outer Join dalam SQL

Selain INNER JOIN, terdapat **outer joins** yang memungkinkan kita menggabungkan dua tabel tanpa memerlukan kecocokan pada kolom tertentu. Jenis-jenis outer join adalah:

### LEFT JOIN

#### Penjelasan

- Mengembalikan **semua baris dari tabel pertama (left table)**, meskipun tidak ada kecocokan di tabel kedua (right table).
- Jika tidak ada kecocokan, kolom dari tabel kedua akan diisi dengan `NULL`.

#### Contoh Tabel

**employees** (left table):
| employee_id | username | office |
|-------------|------------|--------|
| 1188 | John Smith | NY |
| 1189 | Jane Doe | LA |
| 1190 | Alice Brown| SF |

**machines** (right table):
| employee_id | operating_system |
|-------------|------------------|
| 1188 | Windows |
| 1189 | macOS |

Hasil LEFT JOIN:
| username | office | operating_system |
|------------|--------|------------------|
| John Smith | NY | Windows |
| Jane Doe | LA | macOS |
| Alice Brown| SF | NULL |

#### Query LEFT JOIN

```sql
SELECT username, office, operating_system
FROM employees
LEFT JOIN machines
ON employees.employee_id = machines.employee_id;
```

---

### RIGHT JOIN

#### Penjelasan

- Mengembalikan **semua baris dari tabel kedua (right table)**, meskipun tidak ada kecocokan di tabel pertama (left table).
- Jika tidak ada kecocokan, kolom dari tabel pertama akan diisi dengan `NULL`.

#### Contoh Tabel

Menggunakan tabel yang sama seperti sebelumnya, hasil RIGHT JOIN adalah:
| username | office | operating_system |
|------------|--------|------------------|
| John Smith | NY | Windows |
| Jane Doe | LA | macOS |
| NULL | NULL | NULL |

#### Query RIGHT JOIN

```sql
SELECT username, office, operating_system
FROM employees
RIGHT JOIN machines
ON employees.employee_id = machines.employee_id;
```

---

### FULL OUTER JOIN

#### Penjelasan

- Mengembalikan **semua baris dari kedua tabel**.
- Jika tidak ada kecocokan, nilai yang hilang akan diisi dengan `NULL`.

#### Hasil FULL OUTER JOIN

| username    | office | operating_system |
| ----------- | ------ | ---------------- |
| John Smith  | NY     | Windows          |
| Jane Doe    | LA     | macOS            |
| Alice Brown | SF     | NULL             |
| NULL        | NULL   | NULL             |

#### Query FULL OUTER JOIN

```sql
SELECT username, office, operating_system
FROM employees
FULL OUTER JOIN machines
ON employees.employee_id = machines.employee_id;
```

---

### Kesimpulan

- **LEFT JOIN**: Semua baris dari tabel kiri, ditambah baris yang cocok dari tabel kanan.
- **RIGHT JOIN**: Semua baris dari tabel kanan, ditambah baris yang cocok dari tabel kiri.
- **FULL OUTER JOIN**: Semua baris dari kedua tabel, tanpa memandang kecocokan.

Anda dapat memilih jenis join sesuai kebutuhan analisis data. Jangan ragu untuk mencari dokumentasi SQL saat diperlukan!
