---
id: Cybersecurity incident detection methods
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Metode Deteksi Insiden Keamanan Siber

Berikut adalah berbagai metode deteksi yang digunakan organisasi untuk menemukan ancaman keamanan siber:

## **1. Intrusion Detection System (IDS) dan SIEM Tools**
- **IDS**: Mendeteksi potensi intrusi dan mengirimkan *alerts* untuk aktivitas mencurigakan.
- **SIEM**: Mengumpulkan dan menganalisis data keamanan dari berbagai sumber untuk mendeteksi aktivitas abnormal.
- **Tantangan**:
  - Alat hanya mendeteksi apa yang dikonfigurasi untuk dipantau.
  - Konfigurasi yang tidak tepat dapat menyebabkan ancaman lolos deteksi.

---

## **2. Threat Hunting**
- **Definisi**: Pencarian proaktif ancaman di jaringan untuk menemukan aktivitas jahat yang tidak terdeteksi oleh alat otomatis.
- **Contoh**: *Fileless malware* yang menggunakan memori, bukan file tradisional, sehingga sulit dideteksi oleh analisis berbasis tanda tangan.
- **Proses**:
  - Kombinasi analisis manusia dan teknologi.
  - Digunakan untuk mendeteksi ancaman sebelum merusak sistem.
- **Threat Hunters**:
  - Meneliti ancaman baru, menggunakan intelijen ancaman, indikator kompromi (*indicators of compromise*), dan pembelajaran mesin untuk mendeteksi ancaman.

---

## **3. Threat Intelligence**
- **Definisi**: Informasi berbasis bukti tentang ancaman yang memberikan konteks untuk ancaman yang ada atau baru muncul.
- **Sumber Intelijen Ancaman**:
  - **Laporan Industri**: Berisi taktik, teknik, dan prosedur (TTP) penyerang.
  - **Peringatan Pemerintah**: Mirip dengan laporan industri.
  - **Threat Data Feeds**: Menyediakan data seperti alamat IP, domain, dan hash file.
- **Threat Intelligence Platform (TIP)**:
  - Mengumpulkan, menganalisis, dan menyentralisasi intelijen ancaman dari berbagai sumber.
  - Membantu organisasi mengidentifikasi dan memprioritaskan ancaman yang relevan.
- **Catatan Penting**:
  - Data ancaman tidak boleh sepenuhnya mendasari deteksi, tetapi digunakan untuk menambah konteks.

---

## **4. Cyber Deception**
- **Definisi**: Teknik yang sengaja menipu aktor jahat untuk mendeteksi serangan dan meningkatkan strategi pertahanan.
- **Contoh: Honeypots**:
  - Sistem atau file palsu yang dirancang untuk menarik perhatian penyerang.
  - Misal, file palsu seperti "Client Credit Card Information - 2022" dapat memancing penyerang untuk mencoba mengaksesnya. Ketika diakses, tim keamanan mendapat *alert*.

---

### **Poin Utama**
- Menggunakan berbagai metode deteksi (IDS, SIEM, Threat Hunting, Threat Intelligence, Cyber Deception) sangat penting untuk menghadapi lanskap ancaman yang terus berkembang.
- Kombinasi alat, teknologi, dan analisis manusia meningkatkan keakuratan deteksi dan perlindungan terhadap aset organisasi.

Untuk mempelajari lebih lanjut:
- [ThreatHunting Project](https://threathunting.net)
- [TAG: State-Sponsored Hackers](https://blog.google/threat-analysis-group/)
