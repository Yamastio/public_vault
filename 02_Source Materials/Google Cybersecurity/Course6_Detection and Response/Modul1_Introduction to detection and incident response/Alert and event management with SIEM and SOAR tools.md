---
id: Alert and event management with SIEM and SOAR tools
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan Mengenai Detection Tools, SIEM, dan SOAR

### **Detection Tools**
Detection tools membantu organisasi mendeteksi aktivitas mencurigakan di jaringan dan sistem mereka. Berikut perbandingan antara **IDS**, **IPS**, dan **EDR**:

| **Fitur**                 | **IDS** | **IPS** | **EDR** |
|---------------------------|---------|---------|---------|
| Mendeteksi aktivitas jahat | ✓       | ✓       | ✓       |
| Mencegah intrusi          | N/A     | ✓       | ✓       |
| Mencatat aktivitas        | ✓       | ✓       | ✓       |
| Menghasilkan alert        | ✓       | ✓       | ✓       |
| Analisis perilaku         | N/A     | N/A     | ✓       |

- **IDS (Intrusion Detection System)**
  - Mendeteksi aktivitas mencurigakan dan mengirimkan alert.
  - Tidak dapat mencegah atau menghentikan aktivitas.
  - Contoh tools: Zeek, Suricata, Snort, Sagan.

- **IPS (Intrusion Prevention System)**
  - Mendeteksi dan menghentikan aktivitas jahat dengan mengubah aturan pada sistem (misalnya memblokir IP).
  - Banyak tools IDS juga dapat berfungsi sebagai IPS.

- **EDR (Endpoint Detection and Response)**
  - Dipasang di perangkat endpoint (laptop, ponsel, dll).
  - Melakukan analisis perilaku untuk mendeteksi pola ancaman menggunakan **machine learning**.
  - Dapat menghentikan serangan secara otomatis.
  - Contoh tools: Open EDR, Bitdefender EDR, FortiEDR.

### **SIEM (Security Information and Event Management)**
SIEM adalah alat untuk:
1. **Mengumpulkan dan Mengagregasi Log Data**:
   - Data dikumpulkan dari IDS/IPS, firewall, aplikasi, dll.
   - Log adalah catatan aktivitas dari sumber tertentu.

2. **Normalisasi Data**:
   - Membersihkan data mentah agar hanya atribut yang relevan disimpan.
   - Membuat konsistensi dalam format log.

3. **Menganalisis Data**:
   - Data yang sudah dinormalisasi dianalisis berdasarkan aturan yang dikonfigurasi untuk mendeteksi ancaman.
   - Hasil analisis berupa alert yang dapat diakses oleh analis keamanan.

SIEM diibaratkan seperti **dashboard mobil** yang memberi gambaran real-time mengenai kondisi komponen jaringan.

### **SOAR (Security Orchestration, Automation, and Response)**
- **Tujuan**:
  - Mengotomatiskan respons terhadap insiden keamanan.
  - Mengelola kasus insiden secara terpusat.

- **Perbedaan dari SIEM**:
  - SIEM fokus pada pengumpulan, analisis, dan pelaporan.
  - SOAR melibatkan otomatisasi analisis dan respons terhadap insiden.

#### **Kesimpulan**
- **IDS, IPS, dan EDR** berperan dalam mendeteksi ancaman.
- **SIEM** menyediakan visibilitas dan analisis terpusat untuk log data.
- **SOAR** mengotomatiskan proses respons, membantu keamanan menjadi lebih efisien.
