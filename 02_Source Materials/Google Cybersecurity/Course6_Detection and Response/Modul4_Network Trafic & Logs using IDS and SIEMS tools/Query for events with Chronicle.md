---
id: Query for events with Chronicle
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Penjelasan Penggunaan Chronicle untuk Mencari dan Memfilter Data Log

### Apa itu Chronicle dan YARA-L?

- **Chronicle**: Alat yang memungkinkan Anda mencari dan memfilter data log.
- **YARA-L**: Bahasa pemrograman yang digunakan untuk menulis aturan deteksi, seperti mendeteksi aktivitas eksfiltrasi data berharga.

### Fitur Pencarian Chronicle

1. **Search Field**:
   - Digunakan untuk mencari data log berdasarkan **hostname**, **domain**, **IP**, **URL**, **email**, **username**, atau **file hash**.
2. **Metode Pencarian**:
   - **UDM Search (Unified Data Model)**:
     - Mencari data log yang sudah **dinormalisasi**.
   - **Raw Log Search**:
     - Mencari data log mentah yang belum dinormalisasi.
     - Berguna untuk menemukan data yang tidak dinormalisasi atau untuk troubleshooting masalah ingest data.

### Apa itu Normalisasi Data?

- **Normalisasi**: Proses ekstraksi dan format ulang data log mentah agar lebih mudah dicari.
  - Contoh: Data log mentah diubah menjadi format yang lebih terstruktur, seperti menambahkan label **event_type** atau **action**.

### Contoh Pencarian Menggunakan UDM Search

#### Langkah-langkah:

1. Klik ikon **Structured Query Builder**.
2. Masukkan query berikut:
   ```plaintext
   metadata.event_type = "USER_LOGIN" AND security_result.action = "BLOCK"
   ```
3. Penjelasan query:

   - `metadata.event_type`: Menentukan tipe event, dalam hal ini **USER_LOGIN** (aktivitas login pengguna).
   - `AND`: Operator logika yang memastikan kedua kondisi terpenuhi.
   - `security_result.action`: Menentukan aksi keamanan, misalnya **BLOCK** (login ditolak/gagal).

4. Klik tombol **Query** untuk menampilkan hasil pencarian.

#### Hasil Pencarian:

- **Timeline Grafik**:
  - Menampilkan pola aktivitas login gagal dalam periode waktu tertentu.
- **Daftar Event**:
  - Menampilkan event spesifik dengan **timestamp** dan informasi terkait, seperti nama perangkat (**asset**) atau pengguna.
- **Raw Logs**:
  - Log mentah yang dapat diakses untuk detail lebih lanjut selama investigasi.

### Quick Filters

- Terletak di sisi kiri layar.
- Contoh: Klik **target.ip** untuk melihat daftar IP.
  - Pilih IP tertentu untuk memfilter hasil pencarian agar hanya menampilkan data terkait IP tersebut.

### Manfaat:

- Mempermudah mencari data spesifik.
- Menghemat waktu selama investigasi.

---

### Kesimpulan

Chronicle mempermudah pencarian dan analisis data log dengan:

- Menggunakan **UDM Search** untuk data normalisasi.
- Menyediakan **Raw Log Search** untuk data mentah.
- Fitur tambahan seperti **Quick Filters** mempercepat proses investigasi.

Dengan fitur ini, Anda bisa lebih efektif dalam memantau dan mendeteksi aktivitas mencurigakan.
