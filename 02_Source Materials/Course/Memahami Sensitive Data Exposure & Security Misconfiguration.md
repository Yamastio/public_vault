---
id: Memahami Sensitive Data Exposure & Security Misconfiguration
aliases: []
tags: []
date: 2024-12-05 14:18
---

Tags: [[celah_keamanan]]

## Sensitive Data Exposure

**Sensitive Data Exposure** adalah kondisi di mana data sensitif, seperti kata sandi, email, atau informasi pribadi lainnya, tidak terlindungi dengan baik sehingga dapat diakses oleh pihak yang tidak berwenang.

### Penyebab Utama:

- **Manajemen data yang buruk** dalam aplikasi.
- **Kurangnya enkripsi** pada data sensitif.
- **Penggunaan protokol yang tidak aman**, seperti HTTP tanpa SSL/TLS.
- **Penyimpanan file konfigurasi di lokasi yang mudah diakses.**

### Risiko:

- Kehilangan kredibilitas perusahaan.
- Kerugian finansial akibat pencurian data atau pelanggaran hukum.
- Serangan **MITM (Man-in-the-Middle)** yang memungkinkan penyadapan data selama transmisi.

---

## Security Misconfiguration

**Security Misconfiguration** adalah salah satu penyebab utama Sensitive Data Exposure. Hal ini terjadi ketika sistem atau aplikasi tidak dikonfigurasi dengan benar sehingga menciptakan celah keamanan.

### Contoh Umum:

1. **Fitur yang Tidak Diperlukan Terpasang**
   - Fitur, komponen, atau dokumentasi yang tidak digunakan dibiarkan aktif.
   - Contoh: direktori `/backup` yang tidak dihapus setelah pengujian.
2. **Akun Default atau Kata Sandi Default Aktif**
   - Informasi login bawaan vendor tidak diubah, seperti:
     - Username: `admin`, Password: `admin`.
3. **Kebijakan Kata Sandi yang Lemah**
   - Tidak adanya persyaratan untuk kata sandi kuat, seperti:
     - Panjang minimal 8 karakter.
     - Kombinasi huruf besar, kecil, angka, dan simbol.
4. **Fitur Keamanan yang Tidak Dipelihara**
   - File sensitif atau direktori tidak dilindungi.
   - Pesan error yang terlalu detail, seperti menunjukkan struktur direktori atau stack trace.
5. **Penggunaan Versi Perangkat Lunak yang Usang**
   - Aplikasi atau server berjalan di versi lama dengan celah keamanan yang diketahui.
6. **CORS (Cross-Origin Resource Sharing) yang Salah Konfigurasi**
   - Memberikan izin akses terlalu luas ke sumber daya aplikasi dari domain luar.

---

## Contoh pada DVWA (Damn Vulnerable Web Application)

### 1. Akses Root Folder

- Semua pengguna dapat mengakses folder root web `/var/www/html`.

- File seperti `config.inc.php.bak` dapat diakses melalui URL:

  ```
  <http://localhost:4280/config/config.inc.php.bak>
  ```

- File ini menyimpan kredensial database seperti:

  ```sql
  $db_user = 'root';
  $db_password = 'password';
  ```

### 2. File Setup yang Tidak Aman

- File `setup.php` memungkinkan siapa saja yang mengakses untuk:
  - Mereset database.
  - Membuat/menghapus tabel hanya dengan klik tombol.

### 3. Pencarian Endpoint dengan Tools

- Tools seperti **Dirsearch** digunakan untuk menemukan direktori sensitif.

- Contoh penggunaan Google Dork untuk pencarian file konfigurasi bisa juga cek di web `ghdb`:

  ```
  intitle:"index of" inurl:/backup/"wp-config"
  ```

- Dork ini mencari file `wp-config` di direktori `/backup`.

### 4. Masalah pada Situs Contoh ([testphp.vulnweb.com](http://testphp.vulnweb.com))

- Kebijakan password lemah: pengguna dapat mendaftar dengan password berupa angka saja.
- Informasi sensitif ditampilkan setelah pendaftaran, seperti username dan password.

### 5. Penggunaan Teknologi Usang

- Dengan ekstensi browser seperti **Wappalyzer**, dapat ditemukan bahwa situs menggunakan PHP versi 5, yang sudah tidak didukung dan memiliki banyak celah keamanan.

---

## Langkah Mitigasi

1. **Lindungi Data Sensitif:**
   - Gunakan enkripsi untuk data yang disimpan dan dalam proses transmisi.
   - Terapkan protokol HTTPS menggunakan sertifikat SSL/TLS.
2. **Konfigurasi Keamanan yang Baik:**
   - Hapus fitur atau file yang tidak diperlukan.
   - Nonaktifkan akun atau kata sandi default setelah instalasi.
   - Terapkan kebijakan kata sandi yang kuat.
3. **Update dan Patch:**
   - Selalu perbarui aplikasi, server, dan perangkat lunak lainnya.
   - Gunakan versi perangkat lunak yang didukung dengan patch keamanan terbaru.
4. **Proteksi File dan Direktori:**
   - Jangan simpan file konfigurasi di root folder yang dapat diakses publik.
   - Lindungi direktori sensitif dengan autentikasi tambahan atau izin akses yang ketat.
5. **Audit Keamanan:**
   - Lakukan pemeriksaan rutin untuk mendeteksi misconfiguration.
   - Gunakan tools seperti:
     - **Nmap** untuk memeriksa port yang terbuka.
     - **Dirbuster** untuk menemukan direktori tersembunyi.
     - **Burp Suite** untuk pengujian keamanan aplikasi web.
6. **Pengaturan CORS:**
   - Batasi domain yang diizinkan untuk mengakses sumber daya aplikasi.

Dengan langkah-langkah di atas, risiko **Sensitive Data Exposure** dan **Security Misconfiguration** dapat diminimalkan secara signifikan.
