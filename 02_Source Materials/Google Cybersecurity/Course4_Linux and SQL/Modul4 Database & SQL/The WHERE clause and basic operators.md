---
id: The WHERE clause and basic operators
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Penyaringan dengan WHERE Clause dan Operator Dasar

- **Manfaat Filtering**:

  - Membantu menganalisis log keamanan yang besar dan kompleks.
  - Contoh:
    - Menemukan login attempts dari pengguna tertentu.
    - Menemukan perangkat yang menjalankan versi aplikasi tertentu.

- **WHERE Clause**:

  - Digunakan untuk menambahkan kondisi filter.
  - Contoh:
    ```sql
    SELECT firstname, lastname, title, email
    FROM employees
    WHERE title = 'IT Staff';
    ```
    Mengembalikan data hanya dengan `title = 'IT Staff'`.

- **Wildcard**:

  - **%**: Menggantikan sejumlah karakter apa pun.
    - Contoh: `'a%'` menghasilkan `apple123, art, a`.
  - **\_**: Menggantikan satu karakter.
    - Contoh: `'a_'` menghasilkan `as, an, a7`.

- **LIKE Operator**:

  - Digunakan bersama wildcard untuk mencocokkan pola tertentu.
  - Contoh:
    - Mencari karyawan dengan `title` yang dimulai dengan "IT":
      ```sql
      SELECT lastname, firstname, title, email
      FROM employees
      WHERE title LIKE 'IT%';
      ```
    - Mencari pelanggan di negara bagian dengan singkatan 'NY', 'NV', 'NS', atau 'NT':
      ```sql
      SELECT firstname, lastname, state, country
      FROM customers
      WHERE state LIKE 'N_';
      ```

- **Kesimpulan**:
  - Filtering dengan WHERE, LIKE, dan wildcard membantu mempersempit hasil query sesuai kebutuhan.
  - Kombinasi ini efektif untuk pola pencarian data yang spesifik.
