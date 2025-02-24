---
id: Navigate Linux and read file content
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Navigasi Linux dan Membaca Konten File

### **Filesystem Hierarchy Standard (FHS)**

![fhs](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/j0RYvFG7TpGNNfni5SSa0Q_012d7d577b564b4fa3ead21d3f69ebf1_Dvcfull14z4M8iWFX3SE6wnrTefQLql8gas9ICAiKpixcG31SsHLbQmACjE1B4qfpEwTcHfkiD1hxEVGhjyYngw0-fXASC-TSuTgXTBpz_qS4pmXtp-Y7i7giD3GJKCkvajg0PzNebmAf6wDKOBNL-SrMDhBJhsE4yH5Es2_bKRVPC0goRafLVPJs81beg?expiry=1735344000000&hmac=QbjeHU43pnZRe-YWNOfpsXZdUnnylOdCIbaBYjRPngU)

- **FHS** adalah komponen Linux yang mengorganisasi data dengan hierarki direktori.
- Setiap file/direktori di Linux memiliki **file path** yang menggambarkan lokasinya. Contohnya:
  - **Absolute Path**: Dimulai dari root (`/`), misalnya `/home/analyst/projects`.
  - **Relative Path**: Dimulai dari direktori saat ini, misalnya `../projects`.

### **Struktur Direktori di FHS**

- **Root Directory**: Level tertinggi, ditunjukkan oleh `/`.
- **Subdirektori Standar**:
  - `/home`: Direktori untuk setiap pengguna.
  - `/bin`: Berisi file binary/executable untuk program.
  - `/etc`: File konfigurasi sistem.
  - `/tmp`: File sementara (sering dimanfaatkan oleh penyerang).
  - `/mnt`: Media seperti USB atau hard drive.
- **Subdirektori Pengguna**: Misalnya `/home/analyst` dengan subdirektori seperti `projects` atau `logs`.

### **Perintah Navigasi Linux**

1. **pwd**: Menampilkan direktori kerja saat ini.

   - Contoh: `pwd` → Output: `/home/analyst`.

2. **ls**: Menampilkan file dan direktori dalam direktori saat ini.

   - Contoh: `ls` → Output: `logs updates.txt`.
   - Melihat direktori lain: `ls /home/analyst/projects`.

3. **cd**: Berpindah direktori.
   - Contoh:
     - `cd logs`: Masuk ke subdirektori `logs`.
     - `cd ..`: Kembali satu level ke atas.

### **Perintah Membaca Konten File**

1. **cat**: Menampilkan seluruh konten file.

   - Contoh: `cat updates.txt`.

2. **head**: Menampilkan baris awal file (default: 10 baris).

   - Contoh: `head updates.txt`.
   - Menentukan jumlah baris: `head -n 5 updates.txt`.

3. **tail**: Menampilkan baris akhir file (default: 10 baris).

   - Contoh: `tail updates.txt`.

4. **less**: Menampilkan konten file satu halaman per kali.
   - Navigasi di `less`:
     - Space bar: Maju satu halaman.
     - `b`: Mundur satu halaman.
     - Panah atas/bawah: Maju/mundur satu baris.
     - `q`: Keluar.

### **Kesimpulan**

- Kemampuan navigasi di sistem file Linux sangat penting bagi analis keamanan.
- Perintah seperti `pwd`, `ls`, dan `cd` membantu menjelajahi file system.
- Membaca konten file menggunakan `cat`, `head`, `tail`, dan `less` mendukung analisis data, seperti log atau file konfigurasi.
