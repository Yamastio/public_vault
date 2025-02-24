---
id: File permissions and ownership
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Ringkasan Materi: **File dan Directory Permissions di Linux**

### **1. Pengertian Permissions**

- Permissions adalah jenis akses yang diizinkan untuk file atau direktori, terkait dengan _authorization_.
- **Authorization**: Konsep memberikan akses ke sumber daya tertentu dengan membatasi akses berdasarkan _need-to-know basis_.

### **2. Jenis Permissions di Linux**

- **Read (r)**:
  - _File_: Isi file dapat dibaca.
  - _Directory_: Semua file di dalam direktori dapat dilihat.
- **Write (w)**:
  - _File_: Isi file dapat dimodifikasi.
  - _Directory_: Bisa membuat file baru dalam direktori.
- **Execute (x)**:
  - _File_: File dapat dijalankan jika berupa _executable file_.
  - _Directory_: Bisa masuk ke direktori dan mengakses file di dalamnya.

### **3. Tipe Pemilik Permissions**

- **User**: Pemilik file saat file dibuat, tapi kepemilikan bisa diubah.
- **Group**: Sekelompok pengguna yang berbagi izin tertentu.
- **Other**: Semua pengguna lain di sistem yang bukan bagian dari _user_ atau _group_.

### **4. Representasi Permissions dalam Linux**

- Permissions ditampilkan dalam bentuk string 10 karakter, seperti `drwxrwxrwx`.
  - Karakter pertama:
    - `d`: Directory.
    - `-`: File biasa.
  - Karakter 2–4: Permissions untuk _user_.
  - Karakter 5–7: Permissions untuk _group_.
  - Karakter 8–10: Permissions untuk _other_.

### **5. Contoh Format Permissions**

- `-rw-r--r--`:
  - **User**: Read & Write.
  - **Group**: Read.
  - **Other**: Read.

### **6. Perintah Mengecek Permissions**

- **`ls -l`**: Menampilkan permissions file dan direktori.
- **`ls -a`**: Menampilkan file tersembunyi (dimulai dengan titik `.`, misalnya `.hidden1.txt`).
- **`ls -la`**: Kombinasi `ls -l` dan `ls -a`.

### **7. Contoh Output `ls -l`**

- Output:
  ```plaintext
  -rw-r--r-- 1 analyst security 1024 Dec 23 14:00 project1.txt
  ```
  - **`-rw-r--r--`**: Permissions.
  - **`analyst`**: Pemilik file (_user_).
  - **`security`**: Nama grup.
  - **`1024`**: Ukuran file dalam byte.
  - **`Dec 23 14:00`**: Tanggal dan waktu modifikasi terakhir.

### **8. Pentingnya Permissions**

- Permissions yang salah dapat membuka risiko keamanan, seperti:
  - **Privacy breach**: Misalnya, file payroll yang dapat dibaca orang di luar grup payroll.
  - **World-writable files**: File yang bisa ditulis oleh semua orang, membuka peluang manipulasi berbahaya.

### **Kesimpulan**

- **Memantau dan mengatur permissions** sangat penting untuk menjaga keamanan informasi.
- Gunakan perintah `ls -l`, `ls -a`, dan `ls -la` untuk memverifikasi permissions file dan direktori.
