---
id: Core commands for navigation and reading files
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Ringkasan: **Navigasi dan Membaca File di Linux File System**

### **Pengenalan File System di Linux**

- **Hierarki FHS (Filesystem Hierarchy Standard):**
  - **Root Directory (/):** Tingkatan tertinggi dalam file system, tempat semua direktori bercabang.
  - **Subdirektori:** Bercabang dari root, menggunakan tanda slash `/` untuk menavigasi.
    - Contoh: `/home/analyst` (root → home → analyst).
  - Semua hal di Linux dianggap sebagai file dalam direktori.

### **Perintah Dasar Navigasi File System**

1. **`pwd` (Print Working Directory):**

   - Menampilkan direktori tempat kita bekerja saat ini.
   - Contoh: Output `/home/analyst/logs` menunjukkan lokasi saat ini.

2. **`ls`:**

   - Menampilkan daftar file dan direktori dalam direktori kerja saat ini.
   - Contoh: Output bisa menunjukkan file seperti `updates.txt` dan direktori seperti `logs`.

3. **`cd` (Change Directory):**
   - Mengubah lokasi kerja ke direktori lain.
   - Contoh: `cd logs` akan memindahkan lokasi ke direktori `logs`.

### **Perintah Membaca Isi File**

1. **`cat`:**

   - Menampilkan seluruh isi file.
   - Contoh: `cat access.txt` akan menampilkan semua isi file `access.txt`.

2. **`head`:**
   - Menampilkan beberapa baris awal file (default: 10 baris).
   - Contoh: `head access.txt` hanya akan menampilkan 10 baris pertama dari file tersebut.

### **Aplikasi untuk Security Analyst**

- **Navigasi File System:**
  - Menemukan dan menganalisis file log untuk memantau aktivitas aplikasi dan otentikasi.
- **Membaca File Konfigurasi:**
  - Memeriksa potensi kerentanan atau laporan akses pengguna untuk menyelidiki aktivitas tidak sah.

### **Kesimpulan**

- Memahami perintah navigasi dan membaca file adalah keterampilan dasar bagi security analyst untuk menganalisis log dan memecahkan masalah keamanan. Selanjutnya, kita akan belajar tentang **manajemen sistem di Linux.** 🎯
