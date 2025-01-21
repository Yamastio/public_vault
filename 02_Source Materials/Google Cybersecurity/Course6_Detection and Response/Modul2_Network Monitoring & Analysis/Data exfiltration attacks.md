---
id: Data exfiltration attacks
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan: Pemantauan Jaringan untuk Mendeteksi dan Menanggapi Serangan Eksfiltrasi Data

**Pandangan Penyerang**:
- **Akses Awal**: Penyerang sering memulai serangan eksfiltrasi data dengan **serangan rekayasa sosial** seperti **phishing**, yang memanipulasi target untuk memberikan kredensial.
- Setelah memperoleh akses, penyerang melakukan **pergerakan lateral** untuk mengakses sistem lain di jaringan dan menjaga akses mereka tanpa terdeteksi.
- Penyerang mencari **aset bernilai**, seperti kode propriatari, informasi pribadi (PII), atau data finansial, yang kemudian mereka **kumpulkan, kemas, dan siapkan** untuk **eksfiltrasi**.
- Penyerang bisa **mengurangi ukuran data** untuk menyembunyikan data yang dicuri dan menghindari deteksi.

**Cara Menanggapi Serangan Eksfiltrasi Data**:
1. **Pencegahan Akses Penyerang**:
   - Gunakan **otentikasi multi-faktor** untuk mencegah akses tidak sah.
2. **Pemantauan Aktivitas Jaringan**:
   - **Pemantauan jaringan** untuk mendeteksi aktivitas mencurigakan seperti **login dari IP luar** yang harus diselidiki.
   - Semua **aset** harus terdaftar dalam **inventaris aset** dan dilindungi dengan **kontrol keamanan**.
3. **Deteksi dan Penghentian Eksfiltrasi**:
   - **Pemantauan jaringan** untuk mendeteksi tanda-tanda **pengumpulan data** yang tidak biasa, seperti:
     - Transfer file internal besar
     - Upload eksternal besar
     - Penulisan file yang tidak terduga
   - Alat **SIEM** dapat digunakan untuk mendeteksi dan memberikan peringatan terhadap aktivitas ini.
   - Setelah peringatan dikirim, **alamat IP penyerang** dapat diblokir dengan **aturan firewall** untuk menghentikan serangan.

**Kesimpulan**:
- Serangan eksfiltrasi data dapat dideteksi dan dihentikan dengan **pemantauan jaringan** yang efektif.
- Menggunakan **alat seperti SIEM** dan **packet sniffers** dapat membantu mendeteksi aktivitas yang mencurigakan dan menjaga keamanan jaringan.

Pemantauan jaringan adalah langkah penting dalam mengidentifikasi dan mencegah serangan, termasuk serangan **eksfiltrasi data** yang berbahaya.
