---
id: Filter dates and numbers
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Penyaringan dengan Data Numeric dan Date/Time di SQL

- **Tipe Data Umum di Database**:

  1. **String**: Data berupa urutan karakter (contoh: `analyst10`).
  2. **Numeric**: Data berupa angka yang dapat dioperasikan secara matematis (contoh: jumlah login attempts).
  3. **Date and Time**: Data berupa tanggal/waktu (contoh: `2021-03-01`).

- **Operator untuk Numeric dan Date/Time**:

  - `=` : Sama dengan
  - `>` : Lebih besar dari
  - `<` : Lebih kecil dari
  - `!=` : Tidak sama dengan
  - `>=` : Lebih besar atau sama dengan
  - `<=` : Lebih kecil atau sama dengan

- **Contoh Penyaringan Login Attempts Setelah Jam 6 Sore**:

  - Query:
    ```sql
    SELECT *
    FROM log_in_attempts
    WHERE time > '18:00';
    ```
  - Hasil: Daftar login attempts setelah jam 6 sore.

- **Operator BETWEEN**:

  - Digunakan untuk mencari data dalam rentang angka atau tanggal.
  - Contoh: Mencari patch yang diinstal antara 1 Maret 2021 dan 1 September 2021:
    ```sql
    SELECT *
    FROM machines
    WHERE OS_patch_date BETWEEN '2021-03-01' AND '2021-09-01';
    ```

- **Hal Penting**:
  - String, tanggal, dan waktu: Gunakan tanda kutip (`' '`) saat menulis nilai.
  - Angka: Tidak memerlukan tanda kutip.

Dengan pemahaman ini, kamu siap menyaring data numeric dan date/time untuk berbagai kebutuhan analisis! Di video berikutnya, kita akan belajar cara menggabungkan beberapa kondisi dalam satu query.
