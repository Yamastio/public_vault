---
id: Add and delete users
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Ringkasan: Menambahkan dan Menghapus Pengguna di Linux

### Pentingnya Menambah dan Menghapus Pengguna

- **Authentication**: Proses verifikasi identitas pengguna di sistem, mirip dengan keamanan fisik dalam sebuah gedung. Tidak semua pengguna diizinkan mengakses sistem.
- **Menambah Pengguna**: Dibutuhkan ketika ada pengguna baru yang bergabung dalam organisasi atau grup. Pengguna baru bisa berasal dari perubahan struktur organisasi atau perintah manajemen.
- **Menghapus Pengguna**: Penting ketika pengguna meninggalkan organisasi atau berpindah grup. Pengguna yang sudah tidak relevan harus dihapus agar tidak memiliki akses ke sistem lagi.

### Pengguna Root

- **Root User**: Pengguna dengan hak istimewa untuk memodifikasi sistem. Pengguna biasa memiliki batasan, tetapi root memiliki akses tanpa batas.
- **Masalah Penggunaan Root**:
  1. **Keamanan**: Akun root menjadi target utama bagi aktor jahat, oleh karena itu login root harus dinonaktifkan.
  2. **Kesalahan Tidak Dapat Dibalik**: Perintah yang salah dapat menyebabkan kerusakan permanen pada sistem, misalnya menghapus direktori penting.
  3. **Akuntabilitas**: Dalam lingkungan multi-pengguna, tidak ada cara untuk melacak siapa yang menjalankan perintah sebagai root.

### Solusi dengan sudo

- **sudo**: Perintah yang memberikan akses sementara dengan hak istimewa tanpa perlu login sebagai root. Pengguna yang diberi akses melalui **sudoers file** dapat menjalankan perintah dengan hak istimewa setelah memasukkan kata sandi mereka.

### Menambah Pengguna dengan useradd

- **useradd**: Perintah untuk menambah pengguna baru ke sistem. Hanya root atau pengguna dengan hak **sudo** yang bisa menggunakannya.
- **Contoh**: Menambahkan pengguna baru "salesrep7":
  ```bash
  sudo useradd salesrep7
  ```
  Perintah ini tidak menampilkan output, namun jika tidak ada pesan kesalahan, berarti berhasil.

### Menghapus Pengguna dengan userdel

- **userdel**: Perintah untuk menghapus pengguna dari sistem. Sama seperti **useradd**, **userdel** membutuhkan akses root.
- **Contoh**: Menghapus pengguna "salesrep7" yang telah meninggalkan perusahaan:
  ```bash
  sudo userdel salesrep7
  ```
  Perintah ini juga tidak menampilkan output jika berhasil, hanya mengembalikan prompt baru.

### Kesimpulan

- **sudo** memungkinkan pengguna untuk menjalankan perintah dengan hak istimewa secara terbatas, menghindari masalah keamanan dan kesalahan besar saat menggunakan akun root.
- Menambah dan menghapus pengguna memerlukan **sudo** untuk memastikan hanya pihak yang berwenang yang dapat mengakses dan memodifikasi sistem.
