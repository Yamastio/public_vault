---
id: Indicators of compromise
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Ringkasan tentang Indicators of Compromise (IoC)**

### **Apa itu Indicators of Compromise (IoC)?**
- **Definisi**: Bukti yang dapat diamati dan menunjukkan potensi insiden keamanan, seperti nama file terkait malware.
- **Tujuan**: Menunjukkan *siapa* dan *apa* yang terlibat dalam serangan setelah terjadi.
- **Contoh**: Nama file malware atau IP address yang terhubung ke proses mencurigakan.
- **Catatan**: Tidak selalu berarti serangan telah terjadi; IoC juga bisa disebabkan oleh kesalahan manusia atau masalah sistem.

---

### **Perbedaan IoC dan Indicators of Attack (IoA)**
- **IoC**: Fokus pada kejadian yang sudah terjadi (pasca-serangan).
- **IoA**: Fokus pada serangan yang sedang berlangsung (real-time) dan perilaku penyerang.
- **Contoh IoA**: Proses yang melakukan koneksi jaringan (mengindikasikan aktivitas mencurigakan).
- **Contoh IoC**: Nama file proses atau alamat IP yang dihubungi oleh proses tersebut.

---

### **Pyramid of Pain**
Konsep yang dibuat oleh David J. Bianco untuk membantu memahami nilai IoC berdasarkan tingkat kesulitan yang dihadapi penyerang ketika IoC diblokir.

#### **Struktur Pyramid of Pain (dari bawah ke atas)**

![pyramid of pain](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5wpDfG3dRQyt3j7I9Vem3Q_31d63be045bc492e9b94aaeeb809a2f1_b5ndsAVFpYfEQSnQvmCly3Ws1dMEo2js79jF_lmAHf6cke-2RsAJfd2JrQ4GoFZdLOIdxxGx-AyNc-cnn4dolkvJLj1dydB1g0JmArLZWeZy7VJLFagiJ0xcq1oz7oirJA4dN8qjz6CI87yrOt-QSvGE7J28YVbPtj59GiU35sLHgGU8RIqqEkRI-JAk5w?expiry=1736294400000&hmac=4pB_ZXpqxxICqY5FaFYxXYqTePJ2R9zt3ItNcZxi4j0)

1. **Hash Values**: Hash unik untuk file malware tertentu (termudah untuk diganti oleh penyerang).
2. **IP Addresses**: Alamat IP yang digunakan penyerang (mudah diubah).
3. **Domain Names**: Nama domain yang terkait serangan (mudah dibuat baru).
4. **Network Artifacts**: Bukti dari protokol jaringan, seperti User-Agent string.
5. **Host Artifacts**: Bukti di perangkat seperti nama file malware yang dibuat.
6. **Tools**: Perangkat lunak seperti *password crackers* yang digunakan penyerang.
7. **Tactics, Techniques, and Procedures (TTPs)**: Perilaku, taktik, teknik, dan prosedur penyerang (*paling sulit* diidentifikasi).

---

### **Mengapa Pyramid of Pain Penting?**
- Membantu tim keamanan memahami efektivitas IoC untuk mendeteksi dan menghentikan aktivitas berbahaya.
- Semakin ke atas piramida, semakin sulit bagi penyerang untuk melanjutkan serangan.

---

### **Kesimpulan Penting**
- **IoC dan IoA**: Alat penting untuk mendeteksi insiden dan memahami perilaku serangan.
- **Pyramid of Pain**: Membantu menentukan prioritas dalam membatasi ruang gerak penyerang.
- **Fokus Tim Keamanan**: Investasi pada tingkat IoC yang lebih sulit akan memberikan efek yang lebih signifikan dalam menghentikan serangan.
