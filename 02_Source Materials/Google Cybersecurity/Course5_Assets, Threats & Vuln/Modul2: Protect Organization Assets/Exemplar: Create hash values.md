---
id: "Exemplar: Create hash values"
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Ringkasan Exemplar: Create Hash Values**

### **Gambaran Aktivitas**
- Anda akan belajar cara membuat hash nilai untuk membandingkan dua file menggunakan Linux command line.
- **Hash** digunakan untuk:
  - Mengidentifikasi isi file secara unik.
  - Memastikan integritas file dengan mendeteksi perubahan pada file.

---

### **Langkah-Langkah Aktivitas**

#### **Task 1: Generate Hashes for Files**
1. **List file di direktori**:
   - Perintah: `ls`
   - File yang tersedia: `file1.txt` dan `file2.txt`.

2. **Lihat isi file**:
   - Perintah:
     ```bash
     cat file1.txt
     cat file2.txt
     ```
   - Hasil: Kedua file tampaknya memiliki konten yang sama.

3. **Generate hash untuk kedua file**:
   - Perintah:
     ```bash
     sha256sum file1.txt
     sha256sum file2.txt
     ```
   - Hasil:
     - Hash `file1.txt`: `131f95c51cc819465fa1797f6ccacf9d494aaaff46fa3eac73ae63ffbdfd8267`
     - Hash `file2.txt`: `2558ba9a4cad1e69804ce03aa2a029526179a91a5e38cb723320e83af9ca017b`
   - **Kesimpulan**: Kedua file memiliki hash berbeda, yang menunjukkan adanya perbedaan isi.

---

#### **Task 2: Compare Hashes**
1. **Simpan hash ke file terpisah**:
   - Perintah:
     ```bash
     sha256sum file1.txt >> file1hash
     sha256sum file2.txt >> file2hash
     ```

2. **Tampilkan hash dari file baru**:
   - Perintah:
     ```bash
     cat file1hash
     cat file2hash
     ```
   - Hasil: Hash pada `file1hash` dan `file2hash` berbeda.

3. **Bandingkan file hash**:
   - Perintah:
     ```bash
     cmp file1hash file2hash
     ```
   - Hasil:
     - Output: `file1hash file2hash differ: char 1, line 1`
     - **Kesimpulan**: File memiliki perbedaan pada byte pertama di baris pertama.

---

### **Kesimpulan Aktivitas**
- Anda telah berhasil:
  1. **Menghitung hash** dengan `sha256sum`.
  2. **Menampilkan hash** dengan `cat`.
  3. **Membandingkan hash** dengan `cmp`.
- **Pemahaman penting**:
  - Hash berbeda → File tidak identik.
  - **Penggunaan**: Validasi integritas data dan deteksi perubahan file.

> Anda kini siap menggunakan keterampilan ini untuk menjaga keamanan organisasi Anda! 🎉
