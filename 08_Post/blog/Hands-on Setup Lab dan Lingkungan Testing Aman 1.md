---
id: Hands-on Setup Lab dan Lingkungan Testing Aman
aliases: []
tags:
  - hacking_fundamentals
authors:
  - name: "Yamastio link: https://github.com/yamastio image: https://github.com/yamastio.png"
  - name: "Octocat link: https://github.com/octocat image: https://github.com/octocat.png"
date: "2024-12-07"
excludeSearch: true
title: Hands-On Setp Lab dan Lingkungan Testing Aman
---

Tags: [[hacking_fundamentals]]

## 1. Memahami Komponen Utama
- **Ubuntu 24.04**: Digunakan sebagai OS utama untuk host karena stabilitas dan fleksibilitasnya.
- **Kali Linux 2024.3**: Sebagai distro khusus pengujian penetrasi dengan beragam tools bawaan.
- **GNS3**: Emulator jaringan untuk membangun topologi kompleks dan simulasi serangan/pertahanan.

## 2. Langkah-langkah Setup
### i. Instalasi Ubuntu 24.04
- Unduh ISO dari situs resmi Ubuntu.
- Buat media bootable (USB atau DVD) dan instal Ubuntu pada perangkat keras Anda.
### ii. Instalasi Kali Linux (Opsional)
- Unduh ISO Kali Linux 2024.3 dari situs resmi.
- Instal pada VM menggunakan software virtualisasi seperti **VirtualBox** atau **VMware**.
### iii. Instalasi GNS3
- Unduh dan instal GNS3 dari situs resminya.
- Konfigurasikan agar GNS3 dapat bekerja dengan VM Anda (misalnya untuk menghubungkan Kali Linux di dalam VM).
### iv. Konfigurasi Jaringan
- Pastikan mesin host dan VM dapat berkomunikasi.
- Stabilkan koneksi internet untuk mengunduh tools dan update.
### v. Instalasi Tools
- **Di Kali Linux**: Sebagian besar tools untuk ethical hacking sudah tersedia secara default.
- **Di Ubuntu**: Instal tools melalui **apt**, seperti:
    - **Nmap**: Untuk pemindaian jaringan.
    - **Metasploit**: Framework eksploitasi.
    - **Wireshark**: Analisis lalu lintas jaringan.
    - **John the Ripper**: Cracking password.
    - **Burp Suite**: Pengujian aplikasi web.

### vi. Membangun Topologi Jaringan di GNS3
- Tambahkan perangkat jaringan seperti router, switch, firewall di GNS3.
- Konfigurasikan perangkat dan hubungkan sesuai kebutuhan topologi.
## 3. Contoh Topologi Sederhana
- **Host**: Kali Linux (mesin attacker).
- **Target**: Ubuntu Server (mesin target).
- **Router**: Mikrotik di GNS3.
- **Switch**: Built-in switch di GNS3.
## 4. Lingkungan Testing Aman
- **Isolasi Jaringan**: Pisahkan dari jaringan produksi.
- **Firewall**: Batasi akses ke layanan tertentu.
- **IDS (Intrusion Detection System)**: Pantau aktivitas jaringan.
- **Virtualisasi**: Isolasi setiap eksperimen untuk meminimalkan risiko.
- **Backup**: Lakukan backup secara berkala.
## 5. Hands-On Aktivitas
- **Scanning Jaringan**: Gunakan **Nmap** untuk memindai dan mengidentifikasi perangkat.
- **Eksploitasi Kerentanan**: Gunakan **Metasploit** pada kerentanan yang ditemukan.
- **Analisis Traffic**: Gunakan **Wireshark** untuk melihat pola traffic.
- **Password Cracking**: Gunakan **John the Ripper**.
- **Web Application Hacking**: Uji aplikasi web menggunakan **Burp Suite**.
## 6. Tips Tambahan
- **Pelajari Dasar-Dasar Jaringan** untuk memahami lebih baik.
- **Ikuti Tutorial dan Dokumentasi** terkait tools yang digunakan.
- **Praktikkan Secara Teratur** untuk meningkatkan keterampilan.
- **Etika**: Selalu patuhi hukum dan prinsip ethical hacking.
## 7. Penting
- Jangan menyerang sistem tanpa izin.
- Patuhi kebijakan keamanan yang berlaku.
