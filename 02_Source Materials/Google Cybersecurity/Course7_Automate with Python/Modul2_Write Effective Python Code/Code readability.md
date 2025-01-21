---
id: Code readability
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Panduan Penulisan Kode Python dengan PEP 8

Python adalah bahasa pemrograman yang sangat mudah dibaca. Untuk menjaga konsistensi dalam penulisan kode, komunitas Python memiliki **style guide** bernama **PEP 8** (Python Enhancement Proposals 8). PEP 8 memberikan panduan penulisan kode Python agar lebih rapi, mudah dibaca, dan dipahami oleh programmer lain.

### Mengapa PEP 8 Penting?

- **Kode dibaca lebih sering daripada ditulis.** Panduan ini memastikan kode yang kita tulis mudah dimengerti oleh orang lain atau bahkan diri kita sendiri di masa depan.
- **Meningkatkan kolaborasi tim.** Dengan mengikuti gaya penulisan yang sama, semua orang dalam tim dapat membaca dan memodifikasi kode dengan lebih efisien.

---

### Poin Utama dalam PEP 8

#### 1. **Komentar (Comments)**

- Komentar adalah catatan dalam kode untuk menjelaskan **apa yang dilakukan kode** dan **mengapa**.
- **Contoh tanpa komentar:**

  ```python
  failed_attempts = 6
  if failed_attempts > 5:
      print("Account locked")
  ```

  Orang lain mungkin tidak tahu apa arti variabel `failed_attempts` atau alasan logika di balik program.

- **Contoh dengan komentar:**
  ```python
  # Jika jumlah percobaan gagal lebih dari 5, akun akan dikunci
  failed_attempts = 6
  if failed_attempts > 5:
      print("Account locked")
  ```
  **Tips**:
  - Komentar harus jelas, singkat, dan diperbarui jika kode berubah.

---

#### 2. **Indentasi (Indentation)**

Indentasi adalah menambahkan spasi di awal baris kode untuk meningkatkan keterbacaan dan mengatur logika program. Python menggunakan indentasi untuk menentukan blok kode.

- **Aturan:**

  - Gunakan **4 spasi** untuk setiap level indentasi (sesuai rekomendasi PEP 8).
  - Jangan mencampur spasi dan tab.

- **Contoh indentasi benar:**

  ```python
  if failed_attempts > 5:
      print("Account locked")
  ```

- **Jika tidak diindentasikan:**

  ```python
  if failed_attempts > 5:
  print("Account locked")  # Akan menghasilkan error
  ```

- **Kenapa penting?**
  Tanpa indentasi yang benar, Python tidak dapat memahami blok kode, sehingga program tidak akan berjalan sesuai harapan.

---

### Manfaat Mengikuti PEP 8

1. **Mempermudah pemeliharaan kode:**
   Kode yang rapi lebih mudah diperbarui dan diperluas di masa depan.
2. **Kolaborasi lebih efisien:**
   Tim yang menggunakan panduan gaya yang sama dapat memahami dan bekerja dengan kode lebih cepat.
3. **Mencegah masalah di masa depan:**
   Kode yang buruk bisa menimbulkan masalah jika tidak konsisten, seperti yang terjadi pada pengalaman penulis saat harus memodifikasi script firewall setahun kemudian.

---

### Kesimpulan

PEP 8 adalah panduan penting untuk menulis kode Python yang rapi dan konsisten. Menggunakan komentar, indentasi yang tepat, dan praktik terbaik lainnya membantu memastikan kode dapat dibaca dan dimodifikasi oleh siapa saja. Keterbacaan adalah kunci utama dalam pengembangan Python.
