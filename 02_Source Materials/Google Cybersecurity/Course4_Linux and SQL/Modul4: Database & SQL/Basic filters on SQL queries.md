---
id: Basic filters on SQL queries
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Penyaringan Data dalam SQL

- **Definisi Filtering**:
  Filtering adalah proses memilih data yang memenuhi kondisi tertentu. Seperti memilih apel segar dari keranjang buah, filtering memungkinkan kita hanya mengambil data yang sesuai kriteria.

- **Contoh Penggunaan**:
  Sebagai security analyst, filtering dapat digunakan untuk menemukan log-in attempts dari negara tertentu, misalnya "Canada."

- **Operator dalam SQL**:
  Operator adalah simbol atau kata kunci yang merepresentasikan operasi, seperti:

  - `=` untuk membandingkan nilai tertentu (contoh: `country = 'USA'`).
  - `LIKE` untuk mencari pola tertentu.

- **Cara Menggunakan Filtering dalam SQL**:

  1. Tambahkan klausa `WHERE` untuk menentukan kondisi filter.
  2. Contoh:
     ```sql
     SELECT *
     FROM log_in_attempts
     WHERE country = 'USA';
     ```
     Hasilnya: Semua baris dengan nilai `country = 'USA'`.

- **Mencari Pola dengan `LIKE`**:

  - Gunakan `%` sebagai wildcard (karakter tidak spesifik).
  - Contoh:
    - `WHERE office LIKE 'East%'` akan mencocokkan semua yang diawali "East" seperti `East-120` atau `East-435`.
    - Jika ingin menemukan entri seperti `US` atau `USA`, gunakan:
      ```sql
      SELECT *
      FROM log_in_attempts
      WHERE country LIKE 'US%';
      ```

- **Keuntungan Filtering**:

  - Memungkinkan pencarian data lebih spesifik dan sesuai kebutuhan.
  - Mampu menangani data yang tidak konsisten seperti format nama negara (`US` atau `USA`).

- **Kesimpulan**:
  Dengan filtering, kita dapat mengambil data yang sangat presisi hanya dengan satu query SQL. Menggunakan operator seperti `=` dan `LIKE` memberikan fleksibilitas untuk berbagai kebutuhan pencarian.
