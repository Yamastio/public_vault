---
id: Activity Decrypt & Encrypt
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Aktivitas: Mendekripsi Pesan yang Terenkripsi

### Pendahuluan
Dalam aktivitas ini, Anda akan belajar cara mendekripsi file terenkripsi menggunakan Linux commands. Anda akan menggunakan *Caesar cipher*, salah satu algoritma kriptografi awal, untuk menemukan pesan tersembunyi dan memahami pentingnya enkripsi dalam melindungi data online.

**Skenario:** Semua file di direktori Anda telah dienkripsi. Tugas Anda adalah menemukan file tersembunyi, memecahkan Caesar cipher, dan mendekripsi file untuk membaca pesan tersembunyi.

---

### **Langkah-Langkah**

### **Task 1: Membaca Isi File**
1. Pastikan Anda berada di direktori home: `/home/analyst`.
2. Jalankan perintah berikut untuk melihat daftar file:
   ```bash
   ls
   ```
   **Hasil:** Anda akan melihat tiga item:
   - File: `Q1.encrypted`
   - File: `README.txt`
   - Direktori: `caesar`

3. Gunakan perintah berikut untuk membaca isi file `README.txt`:
   ```bash
   cat README.txt
   ```
   **Pesan:** File tersembunyi ada di dalam direktori `caesar`.

---

### **Task 2: Menemukan File Tersembunyi**
1. Masuk ke direktori `caesar`:
   ```bash
   cd caesar
   ```
2. Tampilkan semua file (termasuk file tersembunyi) dengan:
   ```bash
   ls -a
   ```
   **Hasil:** Anda akan melihat file tersembunyi bernama `.leftShift3`.

3. Baca isi file `.leftShift3`:
   ```bash
   cat .leftShift3
   ```
   **Hasil:** Pesan dalam file terenkripsi menggunakan Caesar cipher.

4. Gunakan perintah berikut untuk mendekripsi isi file dengan *shift* 3 huruf ke kiri:
   ```bash
   cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"
   ```
   **Hasil:** Anda akan mendapatkan perintah untuk mendekripsi file di Task 3.

5. Kembali ke direktori home:
   ```bash
   cd ~
   ```

---

### **Task 3: Mendekripsi File Terenkripsi**
1. Gunakan perintah berikut untuk mendekripsi file `Q1.encrypted`:
   ```bash
   openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
   ```
   - **openssl:** Perintah untuk enkripsi/dekripsi.
   - **aes-256-cbc:** Algoritma enkripsi simetris yang aman.
   - **-pbkdf2:** Opsi keamanan tambahan untuk kunci.
   - **-a:** Menggunakan encoding ASCII.
   - **-d:** Mode dekripsi.
   - **-in:** File input.
   - **-out:** File output.
   - **-k:** Kata sandi (`ettubrute`).

2. Verifikasi bahwa file `Q1.recovered` telah dibuat:
   ```bash
   ls
   ```

3. Baca isi file hasil dekripsi:
   ```bash
   cat Q1.recovered
   ```
   **Hasil:** Pesan tersembunyi berhasil ditemukan!

---

### **Kesimpulan**
Dalam aktivitas ini, Anda telah berhasil:
- Menggunakan Linux commands untuk menemukan file tersembunyi.
- Memecahkan Caesar cipher.
- Mendekripsi file terenkripsi menggunakan *openssl*.

Langkah-langkah ini memberikan pengalaman praktis tentang cara melindungi dan memulihkan data dengan enkripsi dan dekripsi.

---

### **Akhiri Lab**
1. Klik **End Lab** untuk menyelesaikan aktivitas.
2. Berikan umpan balik jika diperlukan.

Selamat! Anda telah menyelesaikan aktivitas ini dengan sukses. 🎉
