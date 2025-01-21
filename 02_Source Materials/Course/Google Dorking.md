Tags: [[hacking_intermediate]] [[hacking_tools]]

## Apa Itu Google Dorking?

**Google Dorking** adalah teknik yang digunakan untuk melakukan **information gathering** (pengumpulan informasi) dengan memanfaatkan fitur **Advanced Search** pada mesin pencari Google.  
- Teknik ini memungkinkan pengguna untuk menemukan informasi tersembunyi atau sensitif yang tidak terlihat melalui pencarian biasa.  
- Informasi yang dapat ditemukan meliputi:  
  - Data sensitif (username, password).  
  - File konfigurasi.  
  - Direktori sistem.  
  - Panel administrasi.  

---

## Tujuan Google Dorking
1. **Mengumpulkan Data Awal (Reconnaissance):**  
   - Memahami teknologi, struktur, dan informasi target.  

2. **Menganalisis Potensi Kerentanan:**  
   - Melacak file sensitif, halaman login, atau endpoint yang bisa dieksploitasi.  

3. **Membantu Ethical Hacking:**  
   - Menemukan area yang dapat diperbaiki untuk mencegah akses tidak sah.  

---

## Cara Melakukan Google Dorking

### 1. Menggunakan Google Advanced Search
Buka halaman **Google Advanced Search** di:  
[https://www.google.com/advanced_search](https://www.google.com/advanced_search)  

### 2. Menggunakan Google Search Operators
Operator ini digunakan untuk mempersempit hasil pencarian secara efektif:  

#### Operator Dasar
- **Mencari kata/frasa spesifik:**  
  - `"password file"` → Mencari frasa lengkap "password file".  

- **Menggunakan OR/AND:**  
  - `site:kominfo.go.id AND inurl:login` → Mencari halaman login di domain Kominfo.  

- **Mengecualikan kata tertentu:**  
  - `intitle:"admin panel" -site:example.com` → Mengecualikan hasil dari `example.com`.  

#### Operator Lokasi
- **Mencari kata dalam URL:**  
  - `inurl:admin` → Mencari URL yang mengandung "admin".  

- **Mencari kata dalam judul halaman:**  
  - `intitle:"index of /"` → Mencari direktori terbuka.  

- **Mencari dalam teks halaman:**  
  - `intext:"vulnerable"` → Mencari halaman dengan kata "vulnerable" dalam teksnya.  

#### Operator Waktu
- **Sebelum tahun tertentu:**  
  - `site:ugm.ac.id before:2010` → Mencari konten sebelum 2010 di `ugm.ac.id`.  
- **Setelah tahun tertentu:**  
  - `site:ugm.ac.id after:2022` → Mencari konten setelah 2022.  

#### Operator File
- **Mencari file tertentu:**  
  - `filetype:pdf site:example.com` → Mencari file PDF di domain `example.com`.  
  - `filetype:xls intext:password` → Mencari file Excel dengan kata "password".  

#### Operator Lainnya
- **Mencari kamera langsung (live cameras):**  
  - `inurl:/view.shtml` → Mengakses kamera yang tidak dilindungi.  

- **Mencari halaman login:**  
  - `inurl:/login` → Mencari URL login.  

- **Mencari direktori terbuka:**  
  - `intitle:"index of /" confidential` → Mencari folder terbuka dengan konten sensitif.  

---

## Contoh Penggunaan Google Dorking dalam Ethical Hacking

1. **Mengidentifikasi Informasi Sensitif:**  
   - `filetype:txt intext:password`  
   - `intitle:"index of /" intext:backup`  

2. **Mencari Panel Admin:**  
   - `inurl:admin`  
   - `intitle:"admin panel" site:example.com`  

3. **Mencari Server yang Rentan:**  
   - `inurl:http:// site:example.com`  
   - `inurl:wp-login.php` → Mencari login WordPress.  

4. **Menemukan Kamera Terbuka:**  
   - `inurl:/axis-cgi/mjpg` → Kamera Axis yang tidak terlindungi.  

---

## Etika dan Batasan Hukum
1. **Etika:**  
   - Teknik ini harus digunakan untuk tujuan edukasi atau evaluasi keamanan dengan izin resmi dari pemilik sistem.  
   - Jangan menyalahgunakan informasi yang ditemukan untuk tujuan berbahaya.  

2. **Hukum:**  
   - Banyak negara memiliki hukum yang melarang pengambilan informasi tanpa izin.  
   - Pelanggaran dapat dianggap sebagai akses ilegal dan dapat mengakibatkan sanksi pidana.  

---

## Tips untuk Penggunaan Google Dorking
1. **Kombinasikan Operator:**  
   - Gabungkan beberapa operator untuk hasil yang lebih spesifik, contoh:  
     - `inurl:login filetype:php site:example.com`.  

2. **Gunakan Dork Databases:**  
   - Referensi dari komunitas seperti Exploit-DB memiliki daftar **Google Dorks** yang sering digunakan oleh pentester.  

3. **Gunakan dengan Tujuan Positif:**  
   - Memahami risiko dan memberikan saran mitigasi kepada pemilik sistem adalah inti dari **ethical hacking**.  

---

## Kesimpulan
Google Dorking adalah alat yang sangat kuat dalam **information gathering**. Jika digunakan secara bertanggung jawab, teknik ini dapat membantu memperkuat keamanan sistem dan mencegah kebocoran data.  
Namun, harus selalu diingat untuk mematuhi etika dan hukum saat menggunakan teknik ini.  
