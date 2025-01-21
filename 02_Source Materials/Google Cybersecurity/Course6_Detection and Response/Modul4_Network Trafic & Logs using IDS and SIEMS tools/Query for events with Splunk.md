---
id: Query for events with Splunk
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan tentang SIEM, Pencarian, dan Query

### **Apa itu SIEM?**

- SIEM (Security Information and Event Management) adalah aplikasi untuk:

  - Mengumpulkan dan menganalisis data log.
  - Memantau aktivitas kritis dalam organisasi.
  - Mempermudah akses dan analisis data dengan cara normalisasi dan pengindeksan.

- **Proses SIEM:**
  1. **Pengumpulan Data:** Mengambil data dari berbagai sumber, meskipun formatnya berbeda-beda.
  2. **Normalisasi Data:** Mengubah data mentah menjadi format konsisten agar lebih mudah dianalisis.
  3. **Pengindeksan:** Data yang diindeks memungkinkan pencarian cepat di berbagai sumber.

### **Contoh SIEM Tools**

1. **Splunk:**
   - Platform analisis data dengan fitur pencarian, analisis, dan visualisasi data.
   - Menggunakan query language khusus bernama SPL (Search Processing Language).
2. **Chronicle:**
   - SIEM dari Google Cloud untuk menyimpan, menganalisis, dan memvisualisasikan data keamanan.
   - Data yang diunggah akan dinormalisasi sebelum diindeks.

### **Cara Mencari dan Query di SIEM**

- **Tantangan Pencarian di SIEM:**

  - Jumlah data yang besar (berbulan-bulan hingga bertahun-tahun) menyulitkan pencarian.
  - Query yang terlalu umum memperlambat mesin pencari dan menghasilkan terlalu banyak data.

- **Tips untuk Pencarian Efektif:**
  - Tambahkan **parameter spesifik** seperti Event ID, rentang waktu, atau kata kunci tertentu.
  - Gunakan **Boolean operator** seperti `AND`, `OR`, dan `NOT` untuk mengkombinasikan kata kunci.
  - Gunakan **wildcard** (misalnya `fail*`) untuk memperluas pencarian berdasarkan awalan kata.

### **Contoh Pencarian di Splunk**

1. **Query Dasar:**

   - Contoh: `buttercupgames error OR fail*`
   - Arti:
     - Cari data pada index `buttercupgames`.
     - Gunakan kata kunci `error` atau variasi dari `fail` (misalnya, `failed`).

2. **Langkah Pencarian:**

   - Tentukan rentang waktu (misalnya, 30 hari terakhir).
   - Perhatikan hasil dalam **timeline** untuk pola aktivitas.
   - Analisis **events viewer** untuk detail data log.

3. **Mengoptimalkan Pencarian:**
   - Gunakan filter, seperti mengecualikan host tertentu dengan menambahkan `host!=www1` ke query.
   - Raw log search cenderung lebih lambat; gunakan **commands** untuk mempercepat performa pencarian.

### **Kesimpulan**

- Sebagai seorang Security Analyst, penting untuk memahami:
  - Dasar-dasar pencarian data log dalam SIEM.
  - Cara membuat query yang efisien dan spesifik.
  - Beradaptasi dengan berbagai platform SIEM yang digunakan oleh organisasi.
