---
id: "Exemplar: Decrypt an encrypted a message"
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan Lab "Decrypt an Encrypted Message"

**Tujuan:** Mempraktikkan perintah Linux untuk mendekripsi file yang dienkripsi menggunakan metode Caesar cipher dan AES-256-CBC.

---

## **Langkah-langkah**

### **1. Membaca Isi File**

- **Tujuan:** Mengeksplor direktori home dan membaca instruksi awal dari file.
- **Perintah:**
  1. **List direktori:**
     ```bash
     ls /home/analyst
     ```
     Output: `Q1.encrypted`, `README.txt`, `caesar`.
  2. **Baca isi file `README.txt`:**
     ```bash
     cat README.txt
     ```
     **Output:**
     ```
     Hello,
     All of your data has been encrypted. To recover your data, you will need to solve a cipher. To get started look for a hidden file in the caesar subdirectory.
     ```

---

### **2. Menemukan File Tersembunyi**

- **Tujuan:** Menemukan file tersembunyi dan mendekripsi cipher.
- **Langkah:**
  1. **Masuk ke direktori `caesar`:**
     ```bash
     cd caesar
     ```
  2. **List file tersembunyi:**
     ```bash
     ls -a
     ```
     Output: `.leftShift3`.
  3. **Baca isi file tersembunyi:**
     ```bash
     cat .leftShift3
     ```
     Output: Pesan terenkripsi (Caesar cipher dengan shift kiri 3).
  4. **Dekripsi menggunakan `tr`:**
     ```bash
     cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"
     ```
     **Output:**
     ```
     In order to recover your files you will need to enter the following command:

     openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
     ```

---

### **3. Mendekripsi File**

- **Tujuan:** Mendekripsi file `Q1.encrypted` menggunakan AES-256-CBC.
- **Langkah:**
  1. **Dekripsi file:**
     ```bash
     openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
     ```
  2. **List file di direktori:**
     ```bash
     ls
     ```
     Output: File `Q1.recovered` muncul.
  3. **Baca isi file hasil dekripsi:**
     ```bash
     cat Q1.recovered
     ```

---

## **Kesimpulan**

Anda berhasil:
- Melist file tersembunyi.
- Mendekripsi pesan Caesar cipher.
- Mendekripsi file terenkripsi dengan AES-256-CBC.

Pemahaman ini penting untuk meningkatkan keterampilan analisis keamanan data di dunia nyata.
