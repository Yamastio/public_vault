---
id: Man pages within the shell
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## Sumber Bantuan di Shell Linux

### **man**

- Menampilkan informasi lengkap tentang perintah, termasuk deskripsi dan opsi.
- Cara penggunaan:
  - `man [nama_perintah]`
  - Contoh:
    - `man usermod`: Menampilkan opsi seperti `-d` untuk mengubah direktori home pengguna.

### **whatis**

- Memberikan deskripsi singkat tentang perintah dalam satu baris.
- Cara penggunaan:
  - `whatis [nama_perintah]`
  - Contoh:
    - `whatis tail`: Menjelaskan bahwa perintah ini menampilkan bagian akhir file.

### **apropos**

- Mencari deskripsi manual berdasarkan kata kunci tertentu.
- Cara penggunaan:
  - `apropos [kata_kunci]`
  - Contoh:
    - `apropos password`: Menampilkan perintah-perintah terkait kata "password".
  - Gunakan opsi tambahan:
    - `apropos -a [kata_kunci_1] [kata_kunci_2]` untuk mempersempit hasil pencarian.
    - Contoh: `apropos -a change password`: Hasil terbatas pada perintah relevan dengan "change" dan "password".

### **Kesimpulan**

Sebagai analis baru, Anda tidak perlu mengetahui semua jawaban langsung, tetapi penting untuk memahami sumber-sumber bantuan yang tersedia di shell Linux, seperti `man`, `whatis`, dan `apropos`.
