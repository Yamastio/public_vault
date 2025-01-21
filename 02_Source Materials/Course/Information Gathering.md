Tags: [[hacking_fundamentals]]

## Apa itu Information Gathering?

**Information Gathering** adalah salah satu tahapan awal dalam _penetration testing_ (pengujian penetrasi) yang bertujuan untuk mengumpulkan informasi sebanyak mungkin tentang target, baik itu organisasi, sistem, atau individu. Informasi yang dikumpulkan digunakan untuk memahami target dengan lebih baik dan membantu dalam tahap berikutnya seperti eksploitasi atau pemetaan kerentanan.

Tahapan ini sangat penting karena semakin banyak informasi yang diperoleh, semakin besar peluang untuk menemukan celah keamanan.

---

## Jenis Information Gathering

1. **Passive Information Gathering**
    
    - Metode pengumpulan informasi tanpa melakukan interaksi langsung dengan target.
    - Aman dan sulit terdeteksi oleh target.
    - Contoh teknik:
        - **Search Engine**: Menggunakan Google atau Bing untuk mencari informasi tentang target.
        - **Google Dorking**: Teknik pencarian spesifik menggunakan query seperti `site:`, `filetype:`, atau `intitle:`.
        - **DNS Lookup**: Memeriksa data DNS dari target, seperti alamat IP atau subdomain.
        - **Whois Lookup**: Mendapatkan informasi tentang pendaftar domain seperti nama, email, dan alamat.
2. **Active Information Gathering**
    
    - Melibatkan interaksi langsung dengan sistem atau jaringan target.
    - Berisiko lebih besar karena dapat terdeteksi oleh target.
    - Contoh teknik:
        - **Port Scanning**: Memindai port terbuka pada target menggunakan alat seperti Nmap.
        - **Vulnerability Scanning**: Memeriksa sistem untuk menemukan kerentanan yang dikenal.
        - **Banner Grabbing**: Mengambil informasi dari banner layanan (seperti versi perangkat lunak).
        - **Social Engineering**: Menggunakan manipulasi psikologis untuk mendapatkan informasi dari individu.

---

## Tools yang Umum Digunakan

### Passive Tools

- **Maltego**: Untuk analisis hubungan dan informasi publik.
- **Google Dorking**: Query lanjutan untuk menemukan informasi tersembunyi.
- **Whois Lookup**: Informasi tentang pendaftar domain.

### Active Tools

- **Nmap**: Untuk port scanning dan identifikasi layanan.
- **Nikto**: Untuk memeriksa kerentanan web server.
- **Shodan**: Mesin pencari perangkat IoT yang terekspos.
- **Metasploit**: Untuk eksplorasi kerentanan lebih lanjut.

---

## Perbedaan Utama

| **Kategori**      | **Passive Information Gathering** | **Active Information Gathering** |
| ----------------- | --------------------------------- | -------------------------------- |
| **Interaksi**     | Tidak ada interaksi langsung      | Interaksi langsung dengan target |
| **Deteksi**       | Sulit terdeteksi                  | Mudah terdeteksi                 |
| **Contoh Teknik** | Google Dork, DNS, Whois           | Port Scanning, Banner Grabbing   |
| **Resiko**        | Rendah                            | Tinggi                           |

---

Tahap **Information Gathering** membantu seorang _pentester_ memahami target secara mendalam sebelum melangkah ke tahap eksploitasi. Dengan menguasai metode ini, Anda dapat meningkatkan efektivitas dan efisiensi proses pengujian keamanan.