---
id: Learn more about the TCP/IP model
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

### **Model TCP/IP: Konsep dan Lapisan**

Model **TCP/IP** adalah kerangka kerja yang digunakan untuk memvisualisasikan bagaimana data diorganisasi dan dikirimkan melalui jaringan. Model ini mempermudah profesional keamanan dan jaringan untuk:

- Menganalisis proses jaringan.
- Mengidentifikasi potensi ancaman keamanan atau gangguan berdasarkan lapisan yang terpengaruh.

**Empat lapisan dalam Model TCP/IP**:

1. **Network Access Layer** (Lapisan Akses Jaringan)
2. **Internet Layer** (Lapisan Internet)
3. **Transport Layer** (Lapisan Transportasi)
4. **Application Layer** (Lapisan Aplikasi)

---

### **1. Network Access Layer (Lapisan Akses Jaringan)**

- **Tugas Utama**:
  - Membuat dan mengirimkan paket data melalui perangkat keras jaringan.
  - Mengelola perangkat fisik seperti **hub**, modem, kabel, dan switch.
- **Protokol Penting**:
  - **ARP (Address Resolution Protocol)**:
    - Menghubungkan **alamat IP** dengan **alamat MAC** untuk komunikasi dalam jaringan lokal.
- **Contoh Kasus**:
  - Data dari satu perangkat menuju perangkat lain dalam jaringan lokal menggunakan kabel Ethernet.

---

### **2. Internet Layer (Lapisan Internet)**

- **Tugas Utama**:
  - Menangani routing dan pengalamatan paket data.
  - Menentukan protokol yang akan digunakan untuk mengirimkan data ke tujuan.
- **Protokol Penting**:
  - **IP (Internet Protocol)**:
    - Mengarahkan paket data antar jaringan (LAN ke WAN).
    - Membantu memastikan paket sampai ke tujuan dengan bantuan protokol di lapisan transport.
  - **ICMP (Internet Control Message Protocol)**:
    - Memberikan informasi tentang kesalahan, seperti paket yang hilang atau gagal dikirim.
    - Digunakan untuk troubleshooting jaringan (misalnya, perintah _ping_).

---

### **3. Transport Layer (Lapisan Transportasi)**

- **Tugas Utama**:
  - Mengatur pengiriman data antara dua perangkat di jaringan.
  - Memastikan aliran data aman dan teratur.
- **Protokol Penting**:
  - **TCP (Transmission Control Protocol)**:
    - Memastikan transmisi data yang andal dengan membuat koneksi terlebih dahulu.
    - Digunakan untuk aplikasi seperti email dan transfer file.
  - **UDP (User Datagram Protocol)**:
    - Protokol tanpa koneksi (connectionless) yang lebih cepat tetapi kurang andal.
    - Cocok untuk aplikasi real-time seperti streaming video.

---

### **4. Application Layer (Lapisan Aplikasi)**

- **Tugas Utama**:
  - Mengelola permintaan layanan jaringan, seperti browsing atau pengiriman email.
  - Menentukan cara paket data berinteraksi dengan perangkat penerima.
- **Protokol Penting**:
  - **HTTP (Hypertext Transfer Protocol)**: Untuk komunikasi web.
  - **SMTP (Simple Mail Transfer Protocol)**: Untuk pengiriman email.
  - **SSH (Secure Shell)**: Untuk akses jarak jauh yang aman.
  - **FTP (File Transfer Protocol)**: Untuk transfer file.
  - **DNS (Domain Name System)**: Untuk menerjemahkan nama domain ke alamat IP.

---

![Osi VS TCP/IP](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RbNt47PDRTGJZ6q_QtaNMg_9b9098ac04e84c2d8ad04b220c5456f1_CS_R-210_TCP-vs-OSI.png?expiry=1734998400000&hmac=xSZSy45dHDR4vNYRcSsQKlB-mQwEC_FHZDT6llzC9Ac)

### **Perbandingan Model TCP/IP dan OSI**

1. **Model OSI** memiliki **7 lapisan**, sedangkan **Model TCP/IP** hanya memiliki **4 lapisan**.
   - TCP/IP menyederhanakan lapisan dengan menggabungkan beberapa fungsi OSI.
2. **Lapisan OSI yang Digabungkan**:
   - Application, Presentation, dan Session(OSI) → **Application Layer** (TCP/IP).
   - Jaringan Data dan Fisik (OSI) → **Network Access Layer** (TCP/IP).
3. **Penggunaan**:
   - **Model TCP/IP** lebih sering digunakan secara praktis.
   - **Model OSI** digunakan untuk diskusi teknis dan troubleshooting.

---

### **Kesimpulan Penting**

- **Model TCP/IP** dan **Model OSI** adalah kerangka kerja konseptual untuk memahami proses dan protokol jaringan.
- **TCP/IP** lebih sederhana dan sering digunakan dalam implementasi jaringan modern.
- Memahami kedua model membantu profesional keamanan dalam menganalisis, mendeteksi, dan menyelesaikan ancaman jaringan dengan lebih efektif.
