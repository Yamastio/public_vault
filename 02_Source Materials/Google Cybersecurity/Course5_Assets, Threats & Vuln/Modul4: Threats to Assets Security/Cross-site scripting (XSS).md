---
id: Cross-site scripting (XSS)
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan: Web-Based Exploits dan Cross-Site Scripting (XSS)

**Web-Based Exploits**
Web-based exploits adalah kode atau perilaku berbahaya yang memanfaatkan celah pada aplikasi web untuk mencuri informasi sensitif. Salah satu serangan umum adalah **injection attacks**, di mana kode berbahaya disisipkan ke aplikasi yang rentan.

### Penyebab Kerentanan
- **Interaksi pengguna yang tinggi**: Aplikasi web berinteraksi dengan banyak pengguna dan platform, sehingga sulit untuk memastikan semua data input aman.
- **Validasi input yang lemah**: Aplikasi tidak selalu memvalidasi data yang dimasukkan pengguna secara benar.

**Cross-Site Scripting (XSS)**
XSS adalah jenis injection attack yang memanfaatkan HTML dan JavaScript untuk menyisipkan kode berbahaya ke situs atau aplikasi web. Ada tiga jenis utama XSS:

#### 1. Reflected XSS
- **Cara Kerja**:
  - Penyerang mengirim link berisi skrip berbahaya ke korban.
  - Link tersebut mengirim permintaan HTTP ke server yang rentan.
  - Server memproses dan mengembalikan skrip ke browser korban.
  - Browser, yang mempercayai server, menjalankan skrip dan mengirim data sensitif seperti cookie ke penyerang.
- **Contoh**: Kotak pencarian di situs web.

#### 2. **Stored XSS**
- **Cara Kerja**:
  - Penyerang langsung menyimpan skrip berbahaya di server, misalnya di elemen seperti gambar atau tombol.
  - Skrip aktif saat pengguna mengunjungi situs tanpa perlu tindakan tambahan.
- **Bahaya**: Pengguna tidak bisa mengetahui bahwa situs tersebut sudah terinfeksi.

#### 3. **DOM-Based XSS**
- **Cara Kerja**:
  - Skrip berbahaya disisipkan ke parameter URL situs.
  - Browser memproses parameter tersebut sebagai bagian dari HTML dan menjalankan JavaScript berbahaya tanpa perlu dikirim ke server.
- **Contoh**: Penyerang mengubah parameter URL yang seharusnya digunakan untuk memilih tema warna, lalu menyisipkan JavaScript berbahaya.

**Dampak XSS**
- Mencuri cookie sesi.
- Akses ke geolokasi, mikrofon, atau kamera.
- Informasi sensitif lainnya.

**Langkah Keamanan**
- Validasi dan sanitasi semua input pengguna.
- Gunakan filter dan perlindungan terhadap XSS.
- Edukasi tim pengembang tentang kerentanan injeksi.

Injection attacks, termasuk XSS, adalah ancaman serius terhadap aplikasi web. Sebagai profesional keamanan, memahami cara kerja serangan ini dan cara melindungi sistem adalah langkah penting dalam mengamankan data dan pengguna.
