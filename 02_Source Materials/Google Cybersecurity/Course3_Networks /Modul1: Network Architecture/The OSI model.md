---
id: The OSI model
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Penjelasan Model OSI dan Perbedaannya dengan TCP/IP

#### **Model OSI (Open Systems Interconnection)**

- **Tujuan**: Standar konseptual dengan **7 lapisan komunikasi** untuk memahami, merancang, dan menganalisis proses jaringan.
- **Penggunaan**: Membantu profesional jaringan dan keamanan dalam mendeteksi masalah atau ancaman pada jaringan.

#### **Perbandingan Model TCP/IP dan OSI**

- **TCP/IP**:

  - Memiliki **4 lapisan** (Network Access, Internet, Transport, Application).
  - Lebih ringkas dan sering digunakan dalam praktik sehari-hari.
  - Fokus pada implementasi protokol untuk komunikasi internet.

- **OSI**:
  - Memiliki **7 lapisan** (Physical, Data Link, Network, Transport, Session, Presentation, Application).
  - Memberikan pemahaman lebih mendalam tentang setiap proses komunikasi di jaringan.

---

### **Lapisan-Lapisan Model OSI**

![osi model](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/b5ghKGCVSp6e-fAUC8oo4w_4efb617fe17648559c4a8a0bc0b1abf1_CS_R-043_OSI-Model.png?expiry=1734998400000&hmac=0CGUXiIa4TM3OMZ4_YE5jrmNU-jMSTI2bxTRswMp3So)

1. **Lapisan 7: Application**

   - Proses yang melibatkan interaksi langsung pengguna dengan jaringan.
   - **Contoh protokol**: HTTP, HTTPS, DNS, SMTP.

2. **Lapisan 6: Presentation**

   - Mengurus translasi data, enkripsi, dan kompresi.
   - **Contoh proses**: SSL/TLS untuk enkripsi data web.

3. **Lapisan 5: Session**

   - Mengelola koneksi antar perangkat (session).
   - Tugas: autentikasi, koneksi ulang, dan checkpoint selama transfer data.

4. **Lapisan 4: Transport**

   - Mengatur pengiriman data antar perangkat, termasuk segmentasi dan reassembly.
   - **Contoh protokol**: TCP, UDP.

5. **Lapisan 3: Network**

   - Bertanggung jawab untuk routing paket data antar jaringan.
   - **Contoh protokol**: IP (pengiriman berdasarkan alamat IP).

6. **Lapisan 2: Data Link**

   - Mengelola pengiriman data di dalam satu jaringan lokal (LAN).
   - **Contoh protokol**: HDLC, SDLC.

7. **Lapisan 1: Physical**
   - Berhubungan dengan perangkat keras fisik, seperti kabel, modem, dan hub.
   - Mengubah data menjadi sinyal digital (0 dan 1) untuk transmisi.

---

### **Kesimpulan Utama**

- **TCP/IP** dan **OSI** adalah model penting dalam jaringan:
  - **TCP/IP** sering digunakan karena praktis dan lebih sederhana.
  - **OSI** memberikan detail lebih rinci untuk mendesain dan menganalisis jaringan.
- Profesional keamanan jaringan perlu memahami kedua model ini untuk komunikasi yang efektif tentang lokasi masalah atau ancaman.
