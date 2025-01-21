Tags: [[hacking_tools]] [[hacking_intermediate]]

## Apa itu Find Subdomain?

- **Find Subdomain** adalah proses pencarian _subdomain_ dari suatu domain utama.  
    Subdomain adalah bagian dari nama domain yang berada sebelum domain utama (contoh: `blog.example.com` adalah subdomain dari `example.com`).
- **Tujuan utama**:
    - Memperluas area pencarian saat melakukan penilaian keamanan atau serangan.
    - Jika domain utama tidak memiliki celah keamanan, subdomain dapat menjadi target alternatif.
    - Membantu dalam pemantauan aset digital untuk keamanan atau audit.

---

## Manfaat Mencari Subdomain

1. **Penilaian Keamanan**
    - Subdomain sering kali memiliki konfigurasi yang kurang diperhatikan dan bisa menjadi titik lemah keamanan.
2. **Informasi Tambahan**
    - Dapat menemukan server tambahan, aplikasi, atau API yang tidak terdaftar di domain utama.
3. **Pemantauan**
    - Memastikan tidak ada subdomain tak dikenal yang digunakan tanpa izin.
4. **Identifikasi Infrastruktur**
    - Subdomain dapat memberikan informasi seperti teknologi yang digunakan, IP Address, atau penyedia layanan hosting.

---

## Tools dan Teknik untuk Find Subdomain

### 1. Menggunakan c99 Subdomain Finder

- [c99 Subdomain Finder](https://subdomainfinder.c99.nl/) adalah alat berbasis web untuk menemukan subdomain secara otomatis.
- **Fitur utama**:
    - Menampilkan daftar subdomain yang ditemukan.
    - Informasi tambahan seperti IP Address, penggunaan _firewall_, dan lainnya.
- **Langkah penggunaan**:
    1. Masukkan domain utama di kolom pencarian.
    2. Tunggu hasil daftar subdomain.
    3. Analisis subdomain untuk informasi lebih lanjut.

---

### 2. Menggunakan Google Dorking

- Teknik untuk mencari subdomain menggunakan mesin pencari Google dengan memanfaatkan operator pencarian.
    
- **Dork yang sering digunakan**:
    
    - `site:example.com`
        - Mencari semua halaman yang terindeks di domain utama.
    - `site:*.example.com`
        - Mencari semua halaman yang terindeks di subdomain dari `example.com`.
    - `site:dpr.go.id`
        - Mencari semua halaman di domain `dpr.go.id`.
- **Tips tambahan untuk Dorking**:
    
    - Gabungkan dengan kata kunci seperti `login`, `admin`, `portal` untuk menemukan halaman sensitif.  
        Contoh: `site:*.example.com inurl:login`.

---

### 3. Tools Lainnya untuk Find Subdomain

- **Sublist3r**:
    
    - Alat berbasis Python untuk menemukan subdomain menggunakan berbagai sumber seperti search engines, DNS brute force, dan lainnya.
    - Instalasi: `pip install sublist3r`.
    - Penggunaan:
        
        ```bash
        sublist3r -d example.com
        ```
        
- **Amass**:
    
    - Alat _open-source_ untuk _asset discovery_ dan _subdomain enumeration_.
    - Instalasi:
        
        ```bash
        sudo apt install amass
        ```
        
    - Penggunaan:
        
        ```bash
        amass enum -d example.com
        ```
        
- **crt.sh**:
    
    - Layanan berbasis web untuk menemukan subdomain dengan menganalisis sertifikat SSL/TLS.
    - Link: [crt.sh](https://crt.sh/).

## Pentingnya Etika dan Legalitas

- Pastikan pencarian subdomain dilakukan sesuai izin, terutama jika digunakan untuk penilaian keamanan.
- Gunakan data hanya untuk tujuan yang etis dan tidak melanggar hukum atau peraturan.
