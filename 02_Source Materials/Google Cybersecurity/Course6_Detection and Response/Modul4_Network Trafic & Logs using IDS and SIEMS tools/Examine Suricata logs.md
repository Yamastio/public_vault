---
id: Examine Suricata logs
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Memahami Log yang Dihasilkan oleh Suricata

### Jenis Log di Suricata
Suricata menghasilkan dua jenis log utama:
1. **Alert Logs**:
   - Berisi informasi yang relevan untuk investigasi keamanan.
   - Dihasilkan oleh signature yang memicu alert.
   - Contoh: Log yang mendeteksi lalu lintas mencurigakan di jaringan.

2. **Network Telemetry Logs**:
   - Merekam aliran lalu lintas jaringan, tetapi tidak selalu relevan untuk keamanan.
   - Contoh: Informasi tentang koneksi ke port tertentu.

---

### Format Log: EVE JSON
- **EVE JSON** adalah format output log Suricata yang:
  - Menggunakan **key-value pairs**, memudahkan pencarian dan ekstraksi teks.
  - Memberikan struktur yang konsisten untuk berbagai tipe log.

---

### Contoh Log

#### 1. **Alert Log**
- **Ciri Utama**: Field `event_type` bernilai **alert**.
- **Informasi yang Dicatat**:
  - **IP Address**: Alamat sumber dan tujuan.
  - **Protocol**: Protokol yang digunakan (contoh: HTTP).
  - **Signature Details**:
    - **Message**: Menjelaskan alasan alert (contoh: deteksi malware).
    - **ID**: Identifier signature.

#### 2. **Network Telemetry Log**
- **Ciri Utama**: Field `event_type` bernilai **http**.
- **Informasi yang Dicatat**:
  - **Hostname**: Nama situs web yang diakses.
  - **User Agent**: Nama perangkat lunak yang digunakan (contoh: Mozilla 5.0).
  - **Content Type**: Jenis data yang dikembalikan oleh HTTP request (contoh: HTML text).

---

### Penggunaan Log
- **Alert Logs**: Fokus pada ancaman dan aktivitas mencurigakan untuk investigasi keamanan.
- **Network Telemetry Logs**: Memberikan konteks tambahan tentang lalu lintas jaringan untuk membangun cerita selama investigasi.

---

### Aktivitas Selanjutnya
Anda akan mendapatkan pengalaman langsung dengan Suricata untuk menganalisis log dan mengaplikasikan teori ini dalam praktik. **Selamat mencoba!** 🎉
