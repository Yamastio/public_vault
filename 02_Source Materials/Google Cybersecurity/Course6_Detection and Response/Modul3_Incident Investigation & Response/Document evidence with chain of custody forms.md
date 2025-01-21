---
id: Document evidence with chain of custody forms
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Rangkuman: Chain of Custody dalam Dokumentasi Keamanan**

### **Apa Itu Chain of Custody?**
- **Definisi**: Proses mendokumentasikan kepemilikan dan pengendalian bukti selama siklus insiden.
- **Tujuan**:
  - Memastikan transparansi dalam penanganan bukti.
  - Menyediakan catatan yang dapat dipercaya untuk digunakan dalam proses hukum.

### **Proses Chain of Custody**
1. **Pengumpulan Bukti**:
   - Contoh: Hard drive yang terkompromi.
   - Langkah pertama: Melindungi hard drive dengan **write protection** untuk mencegah pengeditan atau penghapusan data.
   - Hitung dan catat **cryptographic hash** dari citra hard drive untuk mendeteksi potensi perubahan data.

2. **Pelacakan Transfer Bukti**:
   - Setiap kali bukti dipindahkan ke orang lain, transfer ini harus dicatat dalam **formulir chain of custody**.
   - Catatan meliputi:
     - Nama orang yang menyerahkan dan menerima bukti.
     - Tanggal, waktu, dan tujuan transfer.

3. **Pengendalian Integritas Bukti**:
   - Perubahan data dapat dideteksi dengan membandingkan hash asli dengan hash saat ini.

### **Elemen Utama Formulir Chain of Custody**
- **Deskripsi Bukti**:
  - Informasi identifikasi seperti lokasi, hostname, MAC address, atau IP address.
- **Custody Log**:
  - Nama orang yang menyerahkan dan menerima bukti.
  - Tanggal dan waktu pengumpulan atau transfer bukti.
  - Tujuan transfer.

### **Risiko: Broken Chain of Custody**
- **Definisi**: Ketidakkonsistenan dalam pengumpulan dan pencatatan bukti.
- **Dampak**:
  - Memengaruhi integritas, keandalan, dan akurasi bukti.
  - Bukti dapat ditolak di pengadilan karena tidak memenuhi standar hukum.

### **Kesimpulan**
- **Pentingnya Chain of Custody**:
  - Membantu memastikan bukti dapat digunakan dalam proses hukum untuk menahan aktor jahat bertanggung jawab atas tindakan mereka.
- **Konsistensi Adalah Kunci**:
  - Formulir chain of custody harus diisi dengan teliti untuk menghindari kerusakan pada kepercayaan terhadap bukti.
