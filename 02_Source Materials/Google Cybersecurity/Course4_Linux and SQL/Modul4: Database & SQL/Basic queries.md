---
id: Basic queries
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## **Ringkasan**

- **Tujuan Video**: Belajar menjalankan **query SQL pertama** dengan contoh tugas umum seorang analis keamanan, yaitu mencari komputer yang diberikan kepada seorang karyawan.

- **Tabel dan Kolom**: Tabel `employees` memiliki lima kolom, tetapi fokus pada kolom `employee_id` dan `device_id`.

- **Konsep Dasar SQL**:

  - **Kata Kunci**:
    - `SELECT`: Menentukan kolom yang ingin ditampilkan.
    - `FROM`: Menentukan tabel tempat data diambil.
  - **Contoh**:
    ```sql
    SELECT employee_id, device_id FROM employees;
    ```
    - Koma digunakan untuk memisahkan kolom yang ingin ditampilkan.
  - **Syntax**:
    - SQL tidak case-sensitive, tetapi kata kunci sering ditulis dalam huruf kapital untuk kemudahan membaca.
    - Setiap pernyataan diakhiri dengan **tanda titik koma (;)**.

- **Menampilkan Semua Kolom**: Gunakan tanda asterisk (`*`) setelah `SELECT` untuk menampilkan seluruh kolom dari tabel.

  - **Contoh**:
    ```sql
    SELECT * FROM employees;
    ```

- **Hasil**:

  - Query pertama berhasil menghubungkan karyawan dengan komputer mereka.
  - Query kedua menampilkan seluruh tabel sebagai output.

- **Langkah Berikutnya**: Di video berikutnya, akan mempelajari **cara menambahkan filter** pada query SQL.
