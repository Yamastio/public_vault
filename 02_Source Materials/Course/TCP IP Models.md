---
id: TCP IP Models
aliases: []
tags: []
---

Tags: [[networking_fundamentals]]

# 📡 Model TCP/IP vs OSI: Ringkasan & Penjelasan Praktis

---

## 🌐 **Pengenalan Model TCP/IP**

Model TCP/IP adalah dasar jaringan internet modern. Terdiri dari **4 lapisan** utama:

1. **Application** (Aplikasi)
2. **Transport** (Transport)
3. **Internet**
4. **Network Interface** (Antarmuka Jaringan)

🔍 **Catatan:**
Beberapa sumber membagi **Network Interface** menjadi **Data Link** dan **Physical Layer** (total 5 lapisan), tetapi versi resmi tetap 4 lapisan _(RFC1122)_.

---

## 🆚 **Perbandingan Model TCP/IP dan OSI**

### **Tabel Mapping Lapisan**

| **TCP/IP Model**      | **OSI Model**                      | Contoh Protokol      |
| --------------------- | ---------------------------------- | -------------------- |
| **Application**       | Application, Presentation, Session | HTTP, FTP, DNS       |
| **Transport**         | Transport                          | TCP, UDP             |
| **Internet**          | Network                            | IP, ICMP             |
| **Network Interface** | Data Link, Physical                | Ethernet, Wi-Fi, PPP |

### **Perbedaan Utama**

- **TCP/IP Lebih Praktis**: Digunakan di dunia nyata (misal: internet).
- **OSI Lebih Teoritis**: Cocok untuk pembelajaran konsep jaringan.

---

## 🔄 **Encapsulation & De-Encapsulation**

Proses ini **sama** di kedua model:

1. **Encapsulation**:
   Setiap lapisan menambahkan **header** (misal: alamat IP di lapisan Internet, port di Transport).

   - Contoh: Data → Segment (TCP) → Packet (IP) → Frame (Ethernet) → Bit.

2. **De-Encapsulation**:
   Penerima membuka header lapisan demi lapisan untuk membaca data asli.

---

## 🤝 **Three-Way Handshake (TCP)**

Protokol TCP memastikan koneksi **andal** sebelum pengiriman data. Prosesnya seperti jabat tangan 3 langkah:

### **Langkah-Langkah**

1. **SYN** (Synchronize):
   - Komputer A mengirim pesan: _"Mau connect, ya?"_
2. **SYN-ACK** (Synchronize-Acknowledge):
   - Server B menjawab: _"Oke, siap! Aku juga mau connect."_
3. **ACK** (Acknowledge):
   - Komputer A konfirmasi: _"Sip, kita connected!"_

🎯 **Tujuan**:

- Memastikan kedua pihak siap berkomunikasi.
- Jika data hilang/rusak, TCP mengirim ulang _(reliable connection)_.

---

## 📜 **Sejarah Singkat**

- **1982**: Departemen Pertahanan AS (DoD) memperkenalkan TCP/IP untuk **standarisasi jaringan**, mengatasi masalah _inkompatibilitas_ antar perangkat.
- **OSI Model**: Dikenalkan ISO sebagai panduan belajar, tetapi TCP/IP tetap jadi standar praktis.

---

## 💡 **Mengapa Ini Penting?**

- **Kompatibilitas**: Perangkat dari vendor berbeda bisa "berbicara" satu sama lain.
- **Keandalan**: TCP memastikan data sampai utuh _(lossless)_.
- **Skalabilitas**: Struktur lapisan memisahkan tugas (contoh: IP urus alamat, Ethernet urus pengiriman fisik).

---

## 🛠️ **Contoh Praktis**

Saat Anda buka website:

1. **Application Layer**: Browser kirim permintaan HTTP.
2. **Transport Layer**: TCP memecah data jadi _segment_.
3. **Internet Layer**: IP tambahkan alamat tujuan (misal: 142.250.189.206 untuk Google).
4. **Network Interface**: Router ubah jadi _frame_ Ethernet dan kirim via kabel/Wi-Fi.

---

📌 **Tips**:

- Gunakan **Wireshark** atau **tcpdump** untuk melihat proses encapsulation di jaringan nyata!
