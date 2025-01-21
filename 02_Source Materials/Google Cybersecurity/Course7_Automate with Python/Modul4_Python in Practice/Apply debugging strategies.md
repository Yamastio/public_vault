---
id: Apply debugging strategies
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Panduan Debugging untuk Kode Parsing Log File

### Tujuan Program

Kode ini dirancang untuk:

- **Memproses satu baris** dari file log.
- **Mengabaikan status kode 200**, karena menandakan event berhasil dan tidak memerlukan parsing.
- Mengembalikan hasil parsing baris log untuk status kode selain 200.

---

### Langkah-Langkah Debugging

#### 1. **Menangani Syntax Error**

- **Masalah**: Terdapat **syntax error** pada header fungsi. Python membutuhkan tanda titik dua (`:`) di akhir header fungsi.
- **Solusi**: Tambahkan titik dua di akhir header fungsi untuk memperbaiki error ini.

#### 2. **Memperbaiki Name Error**

- **Masalah**: **Name error** muncul karena variabel `application_name` tidak dikenali.
- **Penyebab**: Penulisan variabel salah, hanya menggunakan satu huruf "p" pada `application_name`.
- **Solusi**:
  - Periksa kembali tempat variabel pertama kali dideklarasikan.
  - Perbaiki penulisan nama variabel agar sesuai.

#### 3. **Memastikan Logika Program Berfungsi**

- Setelah memperbaiki error, program masih memiliki **logic error**.
- **Masalah**: Program tidak mencetak pesan _"Successful event - no parsing needed"_ untuk status kode 200.
- **Diagnosa**:
  - Tambahkan **print statement** di beberapa lokasi strategis untuk melacak alur eksekusi:
    1. Sebelum `return parsed_list`.
    2. Di atas pernyataan `if` untuk memeriksa status kode 200.
    3. Di dalam pernyataan `if` tersebut.
  - Hasilnya menunjukkan bahwa **program tidak masuk ke pernyataan `if`**, karena `return parsed_list` mengeksekusi lebih dulu.
- **Solusi**:
  - Pindahkan pernyataan `if` untuk memeriksa status kode 200 **sebelum** baris `return parsed_list`.

#### 4. **Menghapus Print Statement**

- Setelah logika diperbaiki, hapus **print statement** yang digunakan untuk debugging agar kode lebih efisien.

#### 5. **Pengujian Akhir**

- Jalankan kode dengan status kode 200.
- Hasil: Program mencetak pesan _"Successful event - no parsing needed"_. Logic error telah diperbaiki.

---

### Strategi Debugging yang Digunakan

1. **Identifikasi Jenis Error**:
   - Syntax error.
   - Name error.
   - Logic error.
2. **Gunakan Print Statement**:
   - Mempermudah melacak alur eksekusi program.
   - Membantu menemukan lokasi masalah.
3. **Analisis dan Perbaikan Bertahap**:
   - Fokus pada satu masalah sekaligus.
   - Uji kode setelah setiap perbaikan.

---

### Kesimpulan

- **Debugging** adalah proses belajar, bukan kegagalan.
- Kesalahan adalah kesempatan untuk memahami program lebih baik.
- Pastikan alur logika kode sesuai dengan tujuan awal program.
- Jangan ragu untuk meminta bantuan atau menggunakan alat bantu seperti **print statement** saat menemukan jalan buntu.
