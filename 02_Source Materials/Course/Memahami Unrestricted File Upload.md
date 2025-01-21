Tags: [[celah_keamanan]]

## Apa itu Unrestricted File Upload?

Unrestricted File Upload adalah kelemahan yang terjadi ketika aplikasi web tidak menerapkan validasi atau pembatasan yang tepat pada file yang diunggah. **Potensi bahaya:**

1. **Eksekusi kode berbahaya**: File berisi skrip (seperti `.php`, `.jsp`, atau `.asp`) dapat dieksekusi di server.
2. **Pencurian data**: File yang diunggah dapat mencuri atau membocorkan data sensitif.
3. **Pengambilalihan sistem**: Hacker bisa mendapatkan akses penuh ke server.
4. **Serangan lainnya**: Contoh seperti defacing, penanaman backdoor, atau penyebaran malware.

---

## Bagaimana Cara Menemukan Bug Ini?

### Langkah-langkah Pentest:

1. **Identifikasi fitur unggahan file**: Cari endpoint yang memungkinkan pengguna mengunggah file (misalnya, profil pengguna, unggahan dokumen, dll.).
2. **Uji format file**:
    - Unggah file yang tidak sesuai seperti `.php`, `.jsp`, atau `.exe`.
    - Uji file dengan ekstensi yang diubah, misalnya `test.php.jpg`.
3. **Uji ukuran file**:
    - Coba unggah file dengan ukuran besar untuk melihat apakah ada batasan ukuran.
4. **Periksa rename file**:
    - Jika file diubah namanya oleh server, coba manipulasi nama file sebelum atau setelah unggahan.
5. **Uji mekanisme ekstrak file**:
    - Jika aplikasi menerima file ZIP, coba unggah file ZIP yang berisi file berbahaya.
6. **Evaluasi mekanisme blokir**:
    - Cek apakah aplikasi memindai file berbahaya atau memvalidasi tipe MIME.

---

## Cara Kerja Bug

1. Pengguna mengunggah file berbahaya ke server.
2. Server tidak memvalidasi format, ekstensi, atau isi file.
3. File disimpan dan dapat diakses melalui URL tertentu.
4. Jika file dapat dieksekusi (seperti skrip PHP), hacker dapat menjalankan kode pada server.

---

## Pencegahan

1. **Validasi MIME Type**:
    - Pastikan server hanya menerima tipe file yang sesuai (misalnya `image/png`, `image/jpeg`).
2. **Validasi Ekstensi File**:
    - Gunakan whitelist ekstensi file yang diperbolehkan (contoh: `.jpg`, `.png`, `.pdf`).
3. **Validasi Isi File (Content Validation)**:
    - Analisis isi file (misalnya header file) untuk memastikan kecocokan dengan formatnya.
4. **Rename File**:
    - Selalu ubah nama file secara otomatis untuk menghindari eksekusi langsung dari file yang diunggah.
5. **Penyimpanan di luar direktori web root**:
    - Simpan file yang diunggah di lokasi yang tidak dapat diakses langsung melalui browser.
6. **Batasi akses file**:
    - Gunakan izin file yang membatasi akses hanya untuk proses tertentu.
7. **Gunakan library khusus**:
    - Ada library seperti **OWASP File Upload Security Project** yang dapat membantu menangani unggahan file dengan aman.

---

## Studi Kasus: Serangan pada Lab DVWA

1. **Start DVWA**:
    
    - Pastikan container Docker berjalan dan buka DVWA di browser.
2. **Masuk ke menu `file upload`**.
    
3. **Unggah file normal (seperti gambar)**:
    
    - Pastikan file tersimpan dan lihat lokasi penyimpanan di server.
4. **Unggah file berbahaya:**
    
    - **File HTML**:
    
    Jika berhasil diunggah, berarti tidak ada validasi tipe file.
    
     ```html
     <h1>You has been hacked</h1>
     ```
    
    - **File PHP**:
    
    Jika file ini berhasil diakses, hacker dapat menjalankan perintah sistem.
    
     ```php
     <?php echo system("id"); ?>
    ```
    
5. **Eksploitasi lebih lanjut**:
    
    - Gunakan perintah tambahan seperti:
    
    Untuk melihat isi direktori di server.
    
     ```php
     <?php echo system("ls -al"); ?>
     ```
    
6. **Lokasi file:**
    
    - File disimpan di `hackable/uploads/`, yang bisa diakses tanpa batasan validasi.

---

## Catatan Tambahan

Kerentanan seperti ini sering ditemukan di aplikasi yang dibuat tanpa mempertimbangkan keamanan file upload. Oleh karena itu:

- Penting untuk selalu melakukan pentest pada fitur unggahan file.
- Menggunakan framework atau library yang sudah diuji keamanannya untuk menangani unggahan file.

Jika Anda ingin mencoba atau mendalami eksploitasi lebih lanjut, pastikan hanya dilakukan di lingkungan lab atau sistem yang Anda kendalikan untuk tujuan pembelajaran.