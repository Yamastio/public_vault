---
id: Steganography
aliases: []
tags: []
---

Tags: [[hacking_technique]]

## Introduction

Bayangkan kamu ingin menyampaikan pesan rahasia kepada temanmu tanpa orang lain tahu. Biasanya, kalau kamu menulis pesan di kertas, siapa saja bisa membacanya. Tapi, apa jadinya kalau kamu **menyembunyikan pesan itu di dalam gambar atau foto?** Nah, teknik seperti ini disebut **steganografi**.

---

## Apa itu Steganografi?

**Steganografi** adalah seni menyembunyikan pesan rahasia di dalam sesuatu yang terlihat biasa, seperti:

- Foto
- Lagu
- Video

Contohnya, kamu punya foto kucing yang lucu. Dari luar, foto itu terlihat seperti foto biasa. Tapi di dalamnya, kamu menyisipkan pesan rahasia, misalnya: _"Aku suka pizza."_ Hanya kamu dan temanmu yang tahu cara membaca pesan itu.

---

### Mengapa Steganografi Digunakan?

Steganografi digunakan untuk:

1. **Berkomunikasi secara rahasia** tanpa menarik perhatian.
2. **Mengamankan informasi penting**, seperti dokumen rahasia.
3. **Menyembunyikan file sensitif** agar tidak mudah ditemukan orang lain.

---

### Alat untuk Steganografi

Ada beberapa alat yang bisa kamu gunakan untuk menyembunyikan atau membaca pesan rahasia. Berikut contohnya:

1. **Steghide (Command Line)**

   - Kamu bisa menyisipkan file teks ke dalam gambar atau suara.
   - Format file yang didukung: **JPEG, BMP, WAV, AU.**

   Cara install di Linux:

   ```bash
   sudo apt-get install steghide
   ```

2. **Stegosuite (Graphical)**

   - Alat dengan antarmuka grafis (GUI) yang lebih mudah digunakan.
   - Cocok untuk pemula yang tidak terlalu akrab dengan terminal.

   Cara install di Linux:

   ```bash
   sudo apt-get install stegosuite
   ```

---

### Cara Menggunakan Steghide

1. **Menyisipkan Pesan di Dalam Gambar**

   - Buat file teks untuk menyimpan pesan rahasiamu:
     ```bash
     echo "Ini pesan rahasia" > pesan.txt
     ```
   - Gunakan gambar untuk menyimpan pesan tersebut:

     ```bash
     steghide embed -cf gambar.jpg -ef pesan.txt -sf gambar_berisi.jpg
     ```

     - `-cf`: File gambar asli.
     - `-ef`: File pesan yang ingin disembunyikan.
     - `-sf`: Nama gambar baru yang menyimpan pesan.

   - Masukkan password untuk melindungi pesanmu.

2. **Mengekstrak Pesan dari Gambar**
   Jika temanmu punya file `gambar_berisi.jpg`, dia bisa membaca pesan rahasia dengan perintah ini:
   ```bash
   steghide extract -sf gambar_berisi.jpg
   ```
   Setelah memasukkan password, file `pesan.txt` akan muncul.

---

### Cara Menggunakan Stegosuite

1. **Sembunyikan Pesan:**

   - Buka Stegosuite.
   - Pilih gambar yang ingin digunakan.
   - Tambahkan file teks (pesan rahasia).
   - Masukkan password.
   - Klik **Embed**.

2. **Baca Pesan:**
   - Pilih gambar yang sudah berisi pesan.
   - Masukkan password.
   - Klik **Extract** untuk mendapatkan pesan.

---

### Kesimpulan

- **Steganografi** adalah cara menyembunyikan pesan rahasia di dalam file biasa.
- Kamu bisa menggunakan alat seperti **Steghide** (untuk yang suka command line) atau **Stegosuite** (untuk GUI).
- Teknik ini membantu kamu berkomunikasi secara rahasia tanpa menarik perhatian orang lain.
