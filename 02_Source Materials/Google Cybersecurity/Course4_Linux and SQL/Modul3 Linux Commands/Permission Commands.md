---
id: Permission Commands
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Ringkasan: Perintah Permissions di Linux

### Pengertian Permissions

Permissions di Linux direpresentasikan dalam string 10 karakter, dengan arti:

- **read (r)**: Membaca file atau isi direktori.
- **write (w)**: Mengubah file atau menambah isi direktori.
- **execute (x)**: Menjalankan file atau mengakses isi direktori.

### Tipe Owner

1. **User (u)**: Pemilik file.
2. **Group (g)**: Grup yang termasuk pemilik file.
3. **Other (o)**: Pengguna lain di sistem.

### Struktur String Permissions

- Karakter pertama: Tipe file (`d` untuk direktori, `-` untuk file biasa).
- Karakter berikutnya: Permissions untuk user, group, dan other (dibagi menjadi 3 segmen masing-masing: r, w, x).

### Memeriksa Permissions

Gunakan perintah **ls** untuk melihat permissions:

- `ls -a`: Menampilkan file termasuk yang tersembunyi.
- `ls -l`: Menampilkan permissions file, nama pemilik, ukuran, dan waktu modifikasi.
- `ls -la`: Kombinasi dari keduanya.

### Mengubah Permissions dengan chmod

Perintah **chmod** digunakan untuk mengatur permissions:

- Format: `chmod [owner][operator][permissions] [file/directory]`
  - **u**: User
  - **g**: Group
  - **o**: Other
  - **+**: Menambah permissions
  - **-**: Menghapus permissions
  - **=**: Menetapkan permissions secara spesifik

#### Contoh:

- Tambah semua permissions:
  `chmod u+rwx,g+rwx,o+rwx login_sessions.txt`
- Hapus semua permissions:
  `chmod u-rwx,g-rwx,o-rwx login_sessions.txt`
- Tetapkan hanya read:
  `chmod u=r,g=r,o=r login_sessions.txt`

### Prinsip Least Privilege

- Hanya memberikan akses minimal yang diperlukan.
- Contoh: Menghapus permissions grup dari file sensitif:
  - Sebelum: `-rw-rw----`
  - Perintah: `chmod g-rw bonuses.txt`
  - Sesudah: Hanya user yang dapat mengakses file.

### Kesimpulan

- Gunakan **ls** untuk memeriksa permissions file/direktori.
- Gunakan **chmod** untuk memastikan permissions sesuai dengan prinsip **least privilege**, melindungi data sensitif dari akses yang tidak diperlukan.
