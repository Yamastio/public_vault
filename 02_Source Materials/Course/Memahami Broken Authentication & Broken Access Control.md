---
id: Memahami Broken Authentication & Broken Access Control
aliases: []
tags:
  - hacking_fundamentals
date: "2024-12-05"
---

Tags: [[hacking_fundamentals]]

# Broken Access Control

**Broken Access Control** adalah situasi di mana sistem kontrol akses tidak dikelola dengan baik sehingga memungkinkan penyerang mengakses data atau fitur yang seharusnya terbatas.

### Penyebab Umum:

- Kurangnya validasi akses berdasarkan peran pengguna.
- Parameter input yang dapat dimodifikasi untuk mendapatkan akses.
- Hak akses default yang tidak diamankan.
- Kesalahan konfigurasi akses kontrol.

### Risiko:

- Pencurian data sensitif.
- Penyalahgunaan fitur aplikasi oleh penyerang.
- Eskalasi hak akses yang tidak sah.

---

## Ilustrasi Broken Access Control

![[Broken Access Control.png]]

1. **Deskripsi:**
   - Aplikasi web tidak memiliki mekanisme validasi yang kuat terhadap akses fitur.
   - Penyerang dapat memanfaatkan celah ini untuk mengakses data/fitur yang seharusnya dibatasi.
2. **Skema:**
   - User yang tidak memiliki hak akses mencoba fitur tertentu dengan manipulasi URL atau parameter.
   - Sistem tidak memvalidasi permintaan sehingga memberikan akses tidak sah kepada penyerang.

---

## Tipe Serangan Broken Access Control

### 1. **Bypassing Access Control**

- Penyerang mengakses fitur atau data dengan memodifikasi parameter input atau mengakses endpoint tertentu.
- Contoh: Mengubah ID pengguna di URL untuk mendapatkan informasi pengguna lain.

### 2. **Forceful Browsing**

- Penyerang mencoba mengakses URL tersembunyi atau fitur yang seharusnya tidak terlihat oleh pengguna biasa.
- Contoh: Mengakses `/admin/dashboard` pada aplikasi tanpa autentikasi.

### 3. **Privilege Escalation**

- Penyerang mengeksploitasi celah untuk meningkatkan hak akses, misalnya dari pengguna biasa menjadi administrator.
- Contoh: Mengirimkan permintaan API dengan header manipulasi untuk mendapatkan hak admin.

### 4. **Default Account**

- Penyerang menggunakan akun default dengan kredensial bawaan (misalnya: username `admin`, password `admin`).

---

# Broken Authentication

**Broken Authentication** adalah kondisi di mana mekanisme autentikasi tidak diimplementasikan dengan benar, memungkinkan penyerang mengambil alih akun pengguna yang sah.

### Penyebab Umum:

- Kebijakan kata sandi yang lemah.
- Penyimpanan kredensial yang tidak aman.
- Tidak adanya pembatasan pada upaya login yang gagal.
- Penanganan token sesi yang tidak aman.

### Risiko:

- Pencurian akun pengguna.
- Penyalahgunaan data atau fitur aplikasi.
- Kehilangan kepercayaan dari pengguna.

---

## Ilustrasi Broken Authentication

![[Broken Authentication.svg]]

1. **Deskripsi:**
   - Penyerang memanfaatkan celah pada mekanisme reset password.
   - Penyerang mengirimkan tautan phishing atau memodifikasi header permintaan untuk mencuri token reset pengguna.
2. **Skema Serangan:**
   - Penyerang mengirim link phishing kepada korban.
   - Korban membuka tautan dan mencoba mereset password.
   - Penyerang memodifikasi header host untuk mendapatkan token reset.
   - Token ini digunakan untuk mengambil alih akun korban.

---

## Tipe Serangan Broken Authentication

### 1. **Password Cracking**

- Penyerang menggunakan metode brute force untuk menebak kombinasi username dan password.

### 2. **Session Hijacking**

- Penyerang mencuri token sesi pengguna untuk mengakses akun mereka tanpa login.

### 3. **Social Engineering**

- Penyerang mengelabui korban untuk memberikan informasi sensitif seperti kata sandi atau kode OTP.
- Contoh: Mengirim email phishing yang meminta korban untuk memperbarui kredensial.

### 4. **Insecure Communication**

- Penyerang menyadap komunikasi pengguna melalui serangan Man-in-the-Middle (MITM).
- Contoh: Intercept data yang tidak terenkripsi dalam komunikasi HTTP.

### 5. **Default Credentials**

- Penyerang memanfaatkan kredensial bawaan yang tidak diubah oleh pengguna atau pengembang aplikasi.

---

## Langkah Mitigasi

### Untuk Broken Access Control

1. **Validasi Akses Secara Ketat**
   - Pastikan setiap permintaan API atau fitur aplikasi divalidasi berdasarkan peran pengguna.
2. **Minimalkan Privilege**
   - Terapkan prinsip _least privilege_ untuk setiap pengguna.
3. **Audit dan Monitoring**
   - Lakukan audit rutin terhadap kontrol akses dan log aktivitas pengguna.
4. **Hapus Akun Default**
   - Nonaktifkan atau hapus akun default setelah instalasi.

---

### Untuk Broken Authentication

1. **Perkuat Kebijakan Kata Sandi**
   - Panjang minimal 12 karakter dengan kombinasi huruf, angka, dan simbol.
2. **Amankan Token Sesi**
   - Gunakan cookie dengan atribut `Secure` dan `HttpOnly`.
3. **Batasi Upaya Login Gagal**
   - Terapkan mekanisme pembatasan seperti CAPTCHA atau pemblokiran sementara.
4. **Gunakan Protokol HTTPS**
   - Pastikan semua komunikasi menggunakan protokol SSL/TLS.
5. **Otentikasi Multi-Faktor (MFA)**
   - Implementasikan MFA untuk meningkatkan keamanan autentikasi.

Dengan memahami dan mengimplementasikan langkah-langkah mitigasi ini, risiko **Broken Access Control** dan **Broken Authentication** dapat diminimalkan secara signifikan.

# Demo Serangan

Gunakan lab DVWA dan owasp-juice.shop

Kita akan menggunakan burpsuite

Dowload yang comunity edition

Configurasikan dengan browser yang digunakan, bisa gunakan ekstensi browser FoxyProxy

Download sertifikat cacert.der di http://burpsuite, lalu import ke browser, setelah import sertificate maka bisa browsing biasa

1. Setelah itu akses web DVWA, buka dua tab satu di private tab
2. Satu buka dengan previleges admin, satunya bebas. Akan terlihat menu yang hanya tersedia untuk user admin, atau root user, salahs satunya Authorisation Bypass
3. Walau Authorisation Bypass tidak terlihat di user Smithy bukan user admin, tapi smithy apabila memiliki alamat ke authorisation bypass tetap bisa mengakses, yaitu di alamat `http://127.0.0.1:4280/vulnerabilities/authbypass/`
4. Selain bisa melihat, kita bisa update juga datanya, ini adalah bug di authentication, jadi selain root user bisa mengakses bahkan merubah data yang di dalamnya

Contoh serangan Broken Acces Control

1. Pergi ke web `https://demo.owasp-juice.shop/#/`
2. Login dengan akun baru, email sured@gmail.com
3. Pw test123
4. U test
5. Login sured@gmail.com
6. Gunakan email dumy, sured@gmail.com, pw test123
7. Coba add salah satu barang ke basket
8. Lihat di burpsuite request apa yang dilakukan
9. Cek id basket berapa yang ada, di request getnya
10. Nyalakan intercept lalu klik basket
11. Kirim ke repeater, ubah id misal ke 5 atau berapa, lihat response nya

![[burpsuite.png]]

### Melakukan bypass login

1. Logout lalu login dengan username masukan

   ```livescript
   'or 1=1 --
   ```

2. Dengan memasukan username seperti itu, kita bisa login dengan password apapun
3. Klik login lalu kita berhasil login dengan akun admin/root

### Default Credential

1. Login ke DVWA dengan root, hanya dengan default username dan passwordnya

### Password policy tidak diatur dengan baik juga di juice shop

- Validasi tidak di buat dengan baik
- Di sisi backend tidak ada, hanya ada di sisi frontend nya

### Bruteforce

- Pergi ke dvwa
- Ke menu bruteforce
- Coba username admin, dan pw admin
- Biasanya 3 kali percobaan gagal, kita akan diblokir
- Tapi dalam kasus ini, kita bisa coba bahkan lebih dari 3 kali
- Kita bisa lakukan manual atau pakai burpsuite, atau hydra
- Coba pakai burpsuite, pergi ke http history, cari method getnya
- Klik send to intruder
- Tandain passwordnya, menentukan payloadnya
- Attack type default aja, sniper
- Payload, untuk contoh, admin, password, root, admin123, smity, smithy
- Wordlist bisa juga pakai seclist, atau lainya
- Karena untuk contoh, kita pakai yang sederhana
- Klik start attack, lalu tunggu
- Cek status code nya, 200 semua
- Cek lenght nya, biasanya tidak jauh berbeda, cari yang paling beda lalu pergi ke menu response
- Klik render, terlihat bahwa password smity adalah password yang benar
