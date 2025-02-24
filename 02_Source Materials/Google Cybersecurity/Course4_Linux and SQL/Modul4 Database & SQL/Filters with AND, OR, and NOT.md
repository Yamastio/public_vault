---
id: Filters with AND, OR, and NOT
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Penyaringan Data di SQL dengan Operator Logika

### **1. Pentingnya Penyaringan dengan Multiple Conditions**

- Dalam tugas keamanan siber, sering kali kita perlu menyaring data dengan lebih dari satu kondisi, misalnya:

  - **Kerentanan perangkat** tergantung pada kombinasi sistem operasi tertentu dan klien email tertentu.

- Operator logika seperti **AND**, **OR**, dan **NOT** memungkinkan kita untuk membuat filter yang lebih kompleks.

### **2. Operator AND**

- **Definisi**: Mengharuskan **kedua kondisi** terpenuhi secara bersamaan.
- **Analogi**: Memilih apel besar **dan** segar (hasil hanya termasuk apel yang memenuhi **keduanya**).
- **Contoh Query SQL**:
  ```sql
  SELECT *
  FROM machines
  WHERE operating_system = 'OS 1'
    AND email_client = 'Email Client 1';
  ```
  - Mengembalikan semua baris dengan OS 1 **dan** klien email 1.
  - Area hasil digambarkan sebagai **irisan (intersection)** dalam diagram Venn.

### **3. Operator OR**

- **Definisi**: Memenuhi **salah satu** kondisi atau keduanya.
- **Analogi**: Memilih buah yang **apakah jeruk atau apel** (atau keduanya).
- **Contoh Query SQL**:
  ```sql
  SELECT *
  FROM machines
  WHERE operating_system = 'OS 1'
    OR operating_system = 'OS 3';
  ```
  - Mengembalikan semua baris dengan OS 1 **atau** OS 3.
  - Hasilnya meliputi **gabungan (union)** dari dua kondisi pada diagram Venn.

### **4. Operator NOT**

- **Definisi**: Mengembalikan semua baris yang **tidak memenuhi** kondisi tertentu.
- **Analogi**: Memilih semua buah yang **bukan apel** (lebih efisien daripada menyebutkan setiap buah selain apel).
- **Contoh Query SQL**:
  ```sql
  SELECT *
  FROM machines
  WHERE NOT operating_system = 'OS 3';
  ```
  - Mengembalikan semua baris kecuali perangkat dengan OS 3.
  - Hasilnya digambarkan sebagai area **di luar lingkaran** dalam diagram Venn.

### **Kesimpulan Utama**

- **AND**: Hasil harus memenuhi **semua kondisi**.
- **OR**: Hasil dapat memenuhi **salah satu atau lebih kondisi**.
- **NOT**: Mengabaikan data yang memenuhi **kondisi tertentu**.
- **Penerapan**: Operator logika ini memungkinkan analisis data keamanan yang lebih spesifik dan efisien.

Langkah berikutnya: Pelajari **JOIN** untuk menggabungkan tabel dan memperluas cakupan query! 🚀
