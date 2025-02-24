---
id: More on filters with AND, OR, and NOT
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Lebih Lanjut tentang Filter dengan AND, OR, dan NOT

Pada pembahasan sebelumnya, kita telah mempelajari cara menggunakan operator **AND**, **OR**, dan **NOT** dalam SQL untuk menambahkan filter pada query. Di sini, kita akan melanjutkan eksplorasi mengenai bagaimana operator ini dapat membantu menyaring data lebih spesifik untuk mendukung pekerjaan Anda sebagai analis keamanan.

## **Operator Logika**

**AND**, **OR**, dan **NOT** adalah operator logika yang digunakan untuk menyaring query dan mengembalikan informasi spesifik sesuai kebutuhan. Berikut adalah penjelasan rinci:

### **AND**

- **Fungsi:** Menggabungkan dua kondisi, dan hanya mengembalikan data jika _kedua kondisi_ terpenuhi.
- **Contoh:** Jika terdapat masalah keamanan yang hanya memengaruhi akun pelanggan yang:
  1. Ditangani oleh support representative dengan ID `5`
  2. Berlokasi di **USA**

Gunakan **AND** untuk mencari pelanggan tersebut:

```sql
SELECT firstname, lastname, email, country, supportrepid
FROM customers
WHERE supportrepid = 5 AND country = 'USA';
```

- **Hasil:** Data pelanggan yang memenuhi _kedua kondisi_ akan dikembalikan.

## **OR**

- **Fungsi:** Menggabungkan dua kondisi, tetapi **cukup satu** kondisi yang terpenuhi untuk mengembalikan data.
- **Contoh:** Untuk mencari pelanggan yang berada di **USA** atau **Canada**, gunakan **OR**:

```sql
SELECT firstname, lastname, email, country
FROM customers
WHERE country = 'Canada' OR country = 'USA';
```

- **Catatan Penting:**
  Jika kondisi berasal dari kolom yang sama (misalnya `country`), Anda harus menulis kedua kondisi secara lengkap. Contoh:
  ```sql
  WHERE country = 'Canada' OR country = 'USA';
  ```

## **NOT**

- **Fungsi:** Membalikkan atau menegasikan kondisi, yaitu mengembalikan semua data yang _tidak sesuai_ dengan kondisi yang diberikan.
- **Contoh:** Untuk mencari pelanggan yang **bukan dari USA**, gunakan **NOT**:

```sql
SELECT firstname, lastname, email, country
FROM customers
WHERE NOT country = 'USA';
```

- **Tips Alternatif:**
  Anda juga dapat menggunakan operator berikut untuk hasil yang sama:
  - `<>` → `WHERE country <> 'USA'`
  - `!=` → `WHERE country != 'USA'`

## **Menggabungkan Operator Logika**

Anda dapat mengombinasikan **AND**, **OR**, dan **NOT** dalam query untuk membuat filter yang lebih spesifik.

- **Contoh Kombinasi:** Untuk mencari pelanggan yang **bukan dari Canada** dan **bukan dari USA**:

```sql
SELECT firstname, lastname, email, country
FROM customers
WHERE NOT country = 'Canada' AND NOT country = 'USA';
```

### **Kesimpulan Penting**

- **AND:** Memerlukan kedua kondisi benar.
- **OR:** Memerlukan salah satu atau kedua kondisi benar.
- **NOT:** Menegasikan kondisi.
- Kombinasi operator memungkinkan penyaringan yang lebih kompleks sesuai kebutuhan keamanan.

Dengan memahami operator logika ini, Anda dapat membangun query SQL yang lebih spesifik untuk menemukan informasi yang relevan dalam analisis keamanan.
