---
id: Change permissions
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Mengubah Permissions dengan `chmod`

**Konsep Utama:**

- Permissions pada file atau directory mungkin perlu diubah karena alasan seperti perubahan tugas atau kelompok kerja pengguna.
- Mengontrol akses dengan benar penting untuk melindungi file sistem dari perubahan yang tidak disengaja atau disengaja.

**Perintah Utama: `chmod`**

- `chmod` digunakan untuk mengubah permissions file atau directory.
- Terdapat dua mode pengubahan permissions, namun video ini fokus pada _symbolic mode_.

**Format Dasar `chmod` dalam Symbolic Mode:**

1. **Jenis Owner:**

   - `u`: User (pemilik file).
   - `g`: Group (kelompok pengguna).
   - `o`: Other (pengguna lain di sistem).

2. **Operator:**

   - `+`: Menambahkan permissions.
   - `-`: Menghapus permissions.

3. **Jenis Permissions:**

   - `r`: Read (membaca file).
   - `w`: Write (mengubah/menghapus file).
   - `x`: Execute (menjalankan file/directory).

4. **Contoh Format:**
   ```
   chmod g+w,o-r nama_file
   ```
   - `g+w`: Tambahkan write permission ke group.
   - `o-r`: Hapus read permission dari other.

**Contoh Praktik:**

1. **Cek Permissions Awal:**

   - Gunakan `ls -l` untuk melihat permissions file.
   - Contoh:
     ```
     -rw-r--r-- 1 analyst security 1024 Dec 23 12:00 access.txt
     ```
     - User: Read & Write (`rw-`).
     - Group: Read (`r--`).
     - Other: Read (`r--`).

2. **Ubah Permissions:**

   - Tambahkan write permission untuk group dan hapus read permission dari other:
     ```
     chmod g+w,o-r access.txt
     ```

3. **Cek Hasil:**
   - Gunakan `ls -l` lagi:
     ```
     -rw-rw---- 1 analyst security 1024 Dec 23 12:00 access.txt
     ```
     - Group sekarang memiliki write permission (`rw-`).
     - Other kehilangan semua permissions (`---`).

**Catatan Penting:**

- Jangan khawatir harus menghafal seluruh sintaks; referensi tersedia untuk digunakan.
- Praktik berulang akan membuat penggunaan Linux lebih alami.
