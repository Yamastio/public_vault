---
id: Compare types of joins
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## **Ringkasan: Tipe-Tipe Joins dalam SQL**

Joins digunakan untuk menggabungkan data dari beberapa tabel berdasarkan kolom yang sama. Berikut adalah penjelasan masing-masing tipe joins:

### **1. Inner Join**

![inner](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9y5ZKSySQTuS5RQ-MJLXrA_6b756cb30b9442c8ae576607a6ab3ff1_CS_R-080_Inner-joins.png?expiry=1735948800000&hmac=Hk9Gc2nkxW8bRMzcYFl0r-iqV8AKd1LFhaJSgvVY9Po)

- **Mengembalikan**: Hanya baris yang memiliki nilai yang cocok di kedua tabel.
- **Sintaks**:
  ```sql
  SELECT *
  FROM employees
  INNER JOIN machines ON employees.device_id = machines.device_id;
  ```
- **Catatan**:
  - Menggunakan `INNER JOIN` akan mengembalikan semua kolom dari kedua tabel (jika menggunakan `SELECT *`).
  - Jika kolom memiliki nama sama di kedua tabel, perlu menyebutkan tabel dan kolomnya (contoh: `employees.device_id`).

---

### **2. Left Join**

![left](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GsYCwSiOSMmymUqPUAQJ5w_5beed7e470c546fca088a83dfd9465f1_CS_R-080_Left-joins.png?expiry=1735948800000&hmac=hdp6gA1apOC5sZ73doGMVmUN-EGo2p4ti-0aqHRXskY)

- **Mengembalikan**:
  - Semua baris dari tabel pertama (kiri).
  - Hanya baris yang cocok dari tabel kedua (kanan).
  - Baris dari tabel kedua yang tidak memiliki kecocokan akan bernilai `NULL`.
- **Sintaks**:
  ```sql
  SELECT *
  FROM employees
  LEFT JOIN machines ON employees.device_id = machines.device_id;
  ```

---

### **3. Right Join**

![right](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/YHXRMOLiQheppUjthmM5yQ_cfb18a8315e34357bd1299f7eefafcf1_CS_R-080_Right-joins.png?expiry=1735948800000&hmac=Lj3UEXenqDvIuuIDoiz22kfcUv2R0I2aDOArN_wo_ns)

- **Mengembalikan**:
  - Semua baris dari tabel kedua (kanan).
  - Hanya baris yang cocok dari tabel pertama (kiri).
  - Baris dari tabel pertama yang tidak memiliki kecocokan akan bernilai `NULL`.
- **Sintaks**:
  ```sql
  SELECT *
  FROM employees
  RIGHT JOIN machines ON employees.device_id = machines.device_id;
  ```
- **Catatan**:
  - Hasil `RIGHT JOIN` bisa sama dengan `LEFT JOIN` jika urutan tabel ditukar.

---

### **4. Full Outer Join**

![full outer](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/oRzF__GaTqSGMmUqXKbSrQ_92db9841a00244c2aa214e60bb07f1f1_CS_R-080_FULL-OUTER-JOIN.png?expiry=1735948800000&hmac=r2rNQIr83PPKwUKgzmxCCw794wJTJOD6RuNVAjL45GU)

- **Mengembalikan**: Semua baris dari kedua tabel, baik yang cocok maupun yang tidak cocok.
  - Baris tanpa kecocokan akan memiliki nilai `NULL` untuk kolom dari tabel lain.
- **Sintaks**:
  ```sql
  SELECT *
  FROM employees
  FULL OUTER JOIN machines ON employees.device_id = machines.device_id;
  ```

---

### **Poin Penting**

- **Inner Join**: Hanya baris yang cocok di kedua tabel.
- **Left Join**: Semua baris dari tabel kiri, ditambah baris cocok dari tabel kanan.
- **Right Join**: Semua baris dari tabel kanan, ditambah baris cocok dari tabel kiri.
- **Full Outer Join**: Semua baris dari kedua tabel.

> **Tips**: Anda dapat memilih jenis join sesuai kebutuhan data. Untuk informasi spesifik, gunakan `INNER JOIN`; untuk cakupan lebih luas, gunakan outer joins seperti `LEFT JOIN` atau `FULL OUTER JOIN`.
