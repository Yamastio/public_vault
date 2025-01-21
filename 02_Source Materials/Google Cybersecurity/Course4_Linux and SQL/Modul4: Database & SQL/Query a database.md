---
id: Query a database
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## **Ringkasan**

- **Pentingnya SQL**:
  - SQL adalah alat penting dalam cybersecurity, terutama untuk melakukan **query database**.
  - Kata kunci dasar: **SELECT** dan **FROM**.
  - Kursus ini menggunakan **Chinook database** sebagai contoh, yang mencakup tabel seperti `employees`, `customers`, dan `invoices`.

### **Dasar Query SQL**

- **SELECT**:

  - Menentukan kolom yang ingin diambil.
  - Contoh:
    ```sql
    SELECT customerid, city, country
    FROM customers;
    ```
  - Gunakan tanda koma (`,`) untuk memilih banyak kolom.
  - Gunakan asterisk (`*`) untuk memilih semua kolom.
    ```sql
    SELECT * FROM customers;
    ```
  - Catatan: Hindari `SELECT *` pada database besar karena hasilnya sulit dipahami dan lambat diproses.

- **FROM**:
  - Menentukan tabel yang akan di-query.
  - Letakkan setelah `SELECT`, biasanya di baris baru.

### **Mengatur Output dengan ORDER BY**

- **ORDER BY**:

  - Mengurutkan hasil query berdasarkan kolom tertentu.
  - Default: **ascending order** (angka dari kecil ke besar, huruf dari A ke Z).
    ```sql
    SELECT customerid, city, country
    FROM customers
    ORDER BY city;
    ```
  - **Descending order**: Tambahkan `DESC` untuk mengurutkan dari besar ke kecil atau dari Z ke A.
    ```sql
    SELECT customerid, city, country
    FROM customers
    ORDER BY city DESC;
    ```

- **Pengurutan Berdasarkan Kolom Ganda**:
  - Urutkan hasil berdasarkan lebih dari satu kolom.
  - Contoh:
    ```sql
    SELECT customerid, city, country
    FROM customers
    ORDER BY country, city;
    ```

### **Kesimpulan**

- **SELECT** dan **FROM** adalah dasar query SQL.
- **ORDER BY** membantu mengatur data agar lebih terstruktur.
- Pemahaman dasar ini menjadi landasan untuk mempelajari query SQL yang lebih kompleks.
