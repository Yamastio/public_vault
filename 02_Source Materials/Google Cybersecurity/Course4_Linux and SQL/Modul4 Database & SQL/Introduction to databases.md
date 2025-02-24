---
id: Introduction to databases
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## **Pentingnya Database dalam Dunia Modern**

### **Pengertian Database**

- **Database** adalah koleksi data yang terorganisir dan dapat diakses dengan mudah.
- **Perbandingan dengan Spreadsheet**: Spreadsheet seperti Google Sheets lebih cocok untuk pengguna tunggal atau tim kecil dan biasanya menyimpan data dalam jumlah kecil. Sebaliknya, **database** dapat menyimpan jumlah data yang sangat besar dan dapat diakses oleh banyak orang sekaligus.

### **Mengapa Database Penting untuk Security Analyst?**

- **Keperluan Akses Data**: Sebagai security analyst, Anda sering kali perlu mengakses database yang berisi informasi penting seperti **login attempts**, **software updates**, atau **data perangkat**.
- **Kemampuan Database**: Database memungkinkan penyimpanan dan pengaksesan data yang besar dengan cepat dan mudah.

### **Relational Database**

- **Pengertian Relational Database**: Ini adalah database yang disusun dalam **tabel-tabel yang saling berhubungan**. Kita akan fokus pada jenis database ini dalam kursus ini.
- **Struktur Tabel**:
  - Setiap tabel memiliki **kolom** yang berisi informasi spesifik seperti **employee_id**, **device_id**, dan **username**.
  - Setiap baris dalam tabel disebut **record**, yang berisi data terkait dengan kolom.
  - Contoh: Pada tabel karyawan, baris pertama berisi informasi tentang karyawan dengan **id 1,000** yang bekerja di departemen marketing.

### **Mengenal Key dalam Relational Database**

1. **Primary Key**:

   - Kolom yang memiliki nilai unik untuk setiap baris.
   - Tidak boleh ada nilai yang duplikat atau kosong.
   - **Contoh**: Pada tabel karyawan, **employee_id** adalah primary key, karena setiap karyawan memiliki id yang unik.

2. **Foreign Key**:
   - Kolom di tabel yang merujuk pada primary key di tabel lain.
   - Bisa memiliki nilai kosong atau duplikat.
   - **Contoh**: Kolom **employee_id** di tabel mesin adalah foreign key yang merujuk pada primary key **employee_id** di tabel karyawan.

### **Hubungan Antar Tabel**

- **Relasi Antar Tabel**: Dengan menggunakan foreign key, dua tabel dapat dihubungkan.
- **Contoh**: Tabel karyawan dan tabel mesin dapat dihubungkan dengan **employee_id** sebagai foreign key di tabel mesin.

### **Persiapan untuk SQL**

Dengan pengetahuan tentang struktur relational database ini, kita siap untuk mempelajari **SQL** (Structured Query Language), bahasa yang memungkinkan kita bekerja dengan database. Dalam bagian ini, Anda akan mendapatkan pengalaman praktis tentang konsep-konsep yang baru saja dibahas.
