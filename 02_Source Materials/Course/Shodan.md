Tags: [[hacking_intermediate]] [[hacking_tools]]

## Apa itu Shodan?

Shodan adalah mesin pencari yang secara khusus memindai dan mengindeks perangkat yang terhubung ke internet. Berbeda dengan Google yang mencari halaman web, Shodan fokus pada perangkat seperti server, router, CCTV, printer, dan perangkat Internet of Things (_IoT_). Karena kemampuannya untuk mendeteksi perangkat yang terekspos, Shodan sering digunakan dalam konteks keamanan siber.

---

## Fungsi Utama Shodan

1. **Pemetaan Jaringan Global**
    
    - Shodan memindai perangkat di seluruh dunia untuk menemukan perangkat yang dapat diakses secara publik.
    - Informasi yang dikumpulkan mencakup:
        - Alamat IP.
        - Port yang terbuka.
        - Layanan atau protokol yang berjalan (HTTP, FTP, SSH, dll.).
        - Versi perangkat lunak atau sistem operasi.
        - Banner protokol (_service banner_).
2. **Keamanan dan Penilaian Risiko**
    
    - Profesional keamanan menggunakan Shodan untuk mencari perangkat dengan konfigurasi rentan, seperti:
        - Default credentials (username/password bawaan).
        - Protokol tidak aman (misalnya: HTTP tanpa SSL).
    - Memberikan wawasan tentang perangkat yang mungkin menjadi titik masuk bagi peretas.
3. **Pencarian Canggih**
    
    - Shodan memungkinkan pengguna melakukan pencarian terfokus dengan filter tertentu, seperti:
        - Lokasi geografis.
        - Port spesifik.
        - Perangkat spesifik (contoh: webcam, server FTP).

---

## Keunikan Shodan

- **Informasi yang Spesifik**  
    Tidak hanya menunjukkan perangkat ada di internet, tetapi juga memberikan detail lengkap seperti konfigurasi layanan, teknologi yang digunakan, dan _uptime_.
    
- **Peringatan Ancaman (Alert)**
    
    - Pengguna dapat mengatur peringatan untuk melacak perubahan perangkat yang diawasi.
    - Berguna untuk mendeteksi ancaman keamanan yang mungkin muncul.
- **Tren dan Statistik Global**
    
    - Peneliti keamanan dapat menggunakan Shodan untuk memahami tren tentang perangkat dan teknologi yang paling sering terekspos.

---

## Praktik Penggunaan Shodan

### Akses Shodan

1. Pergi ke website resmi Shodan: [https://www.shodan.io](https://www.shodan.io/).
2. Buat akun untuk mendapatkan akses lebih banyak fitur.

### Contoh Query Pencarian

- `http.title:"hacked by"`
    - Mencari situs web yang telah diretas dan memiliki pesan "hacked by".
- `country:ID port:22`
    - Menemukan perangkat dengan port 22 (SSH) terbuka di Indonesia.
- `ssl:"Let's Encrypt"`
    - Mencari perangkat yang menggunakan sertifikat SSL dari Let's Encrypt.
- `os:Windows`
    - Menemukan perangkat dengan sistem operasi Windows.
- `camera`
    - Menemukan perangkat kamera yang terekspos.

### Data yang Didapat

Shodan memberikan data detail, seperti:

- **Hostname**: Nama perangkat atau domain.
- **Provider**: Penyedia layanan hosting atau ISP.
- **Lokasi Geografis**: Negara, kota, dan bahkan koordinat GPS.
- **Teknologi yang Digunakan**: Versi perangkat lunak, layanan aktif, dan lainnya.

---

## Manfaat dan Etika Penggunaan Shodan

### Manfaat

1. **Keamanan Jaringan**
    - Menilai keamanan jaringan internal maupun eksternal.
2. **Pemantauan Perangkat IoT**
    - Melacak perangkat yang terekspos dan memastikan mereka terlindungi.
3. **Riset Keamanan Siber**
    - Mengidentifikasi tren dan kerentanan pada perangkat global.

### Etika Penggunaan

- **Hanya Gunakan untuk Tujuan yang Legal**
    - Pemindaian perangkat milik orang lain tanpa izin dapat dianggap ilegal di beberapa negara.
- **Patuhi Hukum Lokal dan Internasional**
    - Jangan gunakan data Shodan untuk tindakan yang melanggar hukum, seperti peretasan atau eksploitasi perangkat.

---

Shodan adalah alat yang kuat dalam keamanan siber, tetapi penggunaannya memerlukan tanggung jawab dan etika. Dengan memanfaatkan fitur Shodan secara tepat, Anda dapat meningkatkan keamanan perangkat IoT dan infrastruktur digital secara keseluruhan.