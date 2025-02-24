---
id: Denial of Service (DoS) attacks
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Pengertian Dasar

- **DoS Attack:**

  - Serangan yang bertujuan membanjiri jaringan atau server dengan lalu lintas data hingga tidak dapat merespons pengguna yang sah.
  - Dampak:
    - Gangguan operasional bisnis.
    - Kerugian waktu dan uang.
    - Jaringan yang lumpuh lebih rentan terhadap ancaman keamanan lainnya.

- **DDoS Attack:**

  - Serangan DoS yang dilakukan dengan banyak perangkat dari lokasi berbeda.
  - Lebih sulit dilawan karena lalu lintas yang sangat besar.

- **Prinsip Utama:** Jika bagian mana pun dari jaringan berhasil dilumpuhkan, maka serangan dianggap berhasil.

## Contoh Serangan DoS/DDoS

1. **Serangan Berbasis Bandwidth:**

   - Membanjiri bandwidth jaringan untuk memperlambat atau menghentikan lalu lintas.

2. **Kasus Unik:**
   - Penyerang mengirim paket yang dirancang khusus untuk memaksa router bekerja lebih keras memproses permintaan, sehingga sistem terganggu meskipun volume lalu lintas tidak tinggi.

## Jenis Serangan DoS Umum

### 1. SYN Flood Attack

- **Cara Kerja:**
  1.  Penyerang mengirim banyak **SYN requests** ke server.
  2.  Server membalas dengan **SYN/ACK** dan membuka port.
  3.  Penyerang tidak pernah menyelesaikan langkah terakhir (mengirim **ACK**) untuk membentuk koneksi.
- **Hasil:**
  - Jika jumlah **SYN requests** melebihi jumlah port yang tersedia, server menjadi tidak responsif.

### 2. ICMP Flood Attack

- **Cara Kerja:**
  - Penyerang mengirim banyak paket **ICMP** ke server.
  - Server merespons dengan **ICMP replies**.
- **Hasil:**
  - Bandwidth habis untuk lalu lintas masuk dan keluar, menyebabkan server crash.

### 3. Ping of Death

- **Cara Kerja:**
  - Penyerang mengirimkan paket ICMP yang ukurannya melebihi batas maksimum (64 KB).
  - Paket ini membuat server rentan menjadi crash.
- **Analogi:**
  - Seperti menjatuhkan batu besar ke sarang semut kecil, sehingga aktivitas semut berhenti.

## Ringkasan

- **SYN Flood** dan **ICMP Flood** memanfaatkan protokol komunikasi dengan membanjiri server menggunakan permintaan yang sangat banyak.
- **Ping of Death** menggunakan satu permintaan besar yang tidak sesuai dengan spesifikasi untuk melumpuhkan server.
- **Inti DoS/DDoS:** Menggunakan kelebihan lalu lintas atau manipulasi protokol untuk mengganggu operasional jaringan atau server.
