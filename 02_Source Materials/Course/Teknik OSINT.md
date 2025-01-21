Tags: [[hacking_fundamentals]] 

**Open Source Intelligence (OSINT)** adalah proses pengumpulan dan analisis informasi dari sumber-sumber terbuka yang tersedia secara publik. OSINT digunakan oleh peneliti keamanan, pentester, atau bahkan penyerang untuk memahami target dengan lebih baik tanpa harus berinteraksi langsung dengan sistem mereka, membuatnya berguna terutama dalam fase pengintaian pasif (passive reconnaissance). Berikut adalah beberapa teknik OSINT yang umum digunakan:

---

## 1. Search Engine Dorking

- **Deskripsi**: Memanfaatkan mesin pencari dengan query atau kata kunci khusus untuk menemukan informasi sensitif atau konfigurasi yang salah. Ini dapat mencakup file terbuka, halaman admin yang tidak dilindungi, konfigurasi server, dll.
- **Contoh alat**: _Google Dorks_, _Bing Dorking_.

## 2. Social Media Scraping

- **Deskripsi**: Mengumpulkan data dari media sosial seperti LinkedIn, Facebook, atau Twitter untuk mengetahui detail tentang struktur organisasi, informasi karyawan, email, atau data sensitif lainnya.
- **Contoh alat**: _Maltego_, _SpiderFoot_.

## 3. DNS and WHOIS Enumeration

- **Deskripsi**: Menggunakan layanan pencarian DNS dan WHOIS untuk mengidentifikasi detail domain, server, alamat IP, serta informasi pemilik domain.
- **Contoh alat**: _WHOIS Lookup_, _DNSDumpster_.

## 4. Email Harvesting

- **Deskripsi**: Mengumpulkan alamat email yang terkait dengan domain target melalui pencarian di situs web, forum, atau media sosial.
- **Contoh alat**: [_Hunter.io_](http://hunter.io/), _theHarvester_.

## 5. Metadata Extraction

- **Deskripsi**: Mengekstraksi metadata dari dokumen atau file gambar yang tersedia secara online. Metadata ini bisa mengungkapkan informasi seperti versi perangkat lunak, pengguna, dan lokasi file.
- **Contoh alat**: _ExifTool_, _FOCA_.

## 6. Public Code Repositories

- **Deskripsi**: Mengeksplorasi repositori kode terbuka seperti GitHub untuk menemukan kode sumber, dokumentasi teknis, atau kunci API yang mungkin tidak dihapus oleh pengembang.
- **Contoh alat**: _GitHub_, _GitLab_, _Bitbucket_.

## 7. Online Footprint Mapping

- **Deskripsi**: Mencari jejak digital online, seperti subdomain, layanan cloud, situs web terkait, atau riwayat perubahan dan arsitektur layanan target.
- **Contoh alat**: _Shodan_, _Censys_.

## 8. Breached Database Search

- **Deskripsi**: Mencari informasi yang telah bocor dalam pelanggaran data sebelumnya untuk mendapatkan data login, password, atau informasi sensitif lainnya.
- **Contoh alat**: _Have I Been Pwned_, _Dehashed_.

## 9. Website Scraping dan Analysis

- **Deskripsi**: Mengambil dan menganalisis data dari situs web target untuk memahami struktur halaman, komentar, JavaScript, atau elemen lainnya.
- **Contoh alat**: _Wget_, _Scrapy_, _Burp Suite_.

---

## Manfaat dan Risiko OSINT

### Manfaat:

1. **Mengumpulkan informasi tanpa interaksi langsung**:
    - OSINT memungkinkan pengumpulan data tanpa memengaruhi sistem target secara langsung.
2. **Efektivitas dalam merancang strategi serangan/pengujian**:
    - Informasi yang diperoleh dari OSINT dapat digunakan untuk merencanakan serangan atau pengujian lebih efektif.
3. **Legalitas**:
    - Selama data yang dikumpulkan adalah data publik, OSINT adalah aktivitas legal dan sah secara etika.

### Risiko:

1. **Penggunaan tidak etis**:
    - Jika tidak dikendalikan dengan baik, OSINT dapat disalahgunakan untuk mendukung serangan siber.
2. **Eksposur perusahaan**:
    - Organisasi perlu menyadari seberapa banyak data publik mereka yang dapat dimanfaatkan untuk OSINT dan mengambil langkah-langkah untuk mengurangi jejak digital mereka.

---

**OSINT** adalah bagian integral dalam penetration testing, membantu mengidentifikasi titik lemah tanpa meninggalkan jejak langsung pada target. Penggunaannya tetap harus dilakukan dengan hati-hati, sesuai izin dan etika yang berlaku.