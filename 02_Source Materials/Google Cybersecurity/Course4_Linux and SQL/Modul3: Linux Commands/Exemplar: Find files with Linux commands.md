---
id: "Exemplar: Find files with Linux commands"
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## **Ringkasan Aktivitas: Menggunakan Perintah Linux untuk Menemukan File**

### **Gambaran Aktivitas**

- Anda akan berlatih menggunakan perintah shell Linux untuk:
  - Menavigasi struktur direktori.
  - Melihat dan membaca isi file.
- Aktivitas ini dirancang untuk meningkatkan keterampilan Anda dalam bekerja dengan sistem Linux, terutama dalam skenario tanpa antarmuka grafis.

---

### **Skenario**

- Anda akan bekerja di direktori `/home/analyst` dan melakukan beberapa tugas:
  - Menemukan direktori dan file.
  - Membaca isi file untuk menjawab beberapa pertanyaan.
- **Tujuan:** Mengembangkan keahlian navigasi file sebagai seorang _security analyst_.

---

### **Tugas dan Solusi**

#### **Tugas 1: Informasi Direktori Saat Ini**

1. **Tampilkan direktori kerja saat ini:**

   - Perintah: `pwd`
   - Output: `/home/analyst`
   - **Jawaban:** Direktori kerja saat ini adalah `/home/analyst`.

2. **Tampilkan isi direktori:**
   - Perintah: `ls`
   - Output: `logs  projects  reports  temp`
   - **Jawaban:** Direktori ini memiliki 4 subdirektori: `logs`, `projects`, `reports`, dan `temp`.

---

#### **Tugas 2: Ubah Direktori dan Lihat Subdirektori**

1. **Navigasi ke `/home/analyst/reports`:**

   - Perintah (jalur relatif): `cd reports`
   - Perintah (jalur absolut): `cd /home/analyst/reports`

2. **Tampilkan isi direktori:**
   - Perintah: `ls`
   - Output: `users`
   - **Jawaban:** Subdirektori dalam `/home/analyst/reports` adalah `users`.

---

#### **Tugas 3: Temukan dan Baca Isi File**

1. **Navigasi ke `/home/analyst/reports/users`:**

   - Perintah: `cd /home/analyst/reports/users`

2. **Tampilkan file dalam direktori ini:**

   - Perintah: `ls`

3. **Baca isi file `Q1_added_users.txt`:**

   - Perintah: `cat Q1_added_users.txt`

   - **Jawaban Pertanyaan:**
     - **Departemen username `aezra`:** Human Resources.
     - **Employee_id username `mreed` (Information Technology):** 1104.

---

#### **Tugas 4: Navigasi Direktori dan Temukan File**

1. **Navigasi ke `/home/analyst/logs`:**

   - Perintah: `cd /home/analyst/logs`

2. **Tampilkan file dalam direktori ini:**

   - Perintah: `ls`
   - Output: `server_logs.txt`

3. **Tampilkan 10 baris pertama file:**

   - Perintah: `head server_logs.txt`

   - **Jawaban:** Terdapat **3 pesan peringatan (warning)** pada 10 baris pertama file `server_logs.txt`.

---

### **Kesimpulan**

- Anda telah mempraktikkan perintah dasar Linux seperti:
  - **`pwd`**: Menampilkan direktori kerja saat ini.
  - **`cd`**: Navigasi antar direktori.
  - **`ls`**: Menampilkan isi direktori.
  - **`cat`** dan **`head`**: Membaca isi file.
