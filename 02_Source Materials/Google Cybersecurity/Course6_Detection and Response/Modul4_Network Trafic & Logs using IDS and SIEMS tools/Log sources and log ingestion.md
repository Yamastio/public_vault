---
id: Log sources and log ingestion
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Pentingnya Log Ingestion

- **Log ingestion** adalah proses pengumpulan dan impor data dari sumber log ke dalam alat SIEM (Security Information and Event Management).
- Data log berasal dari berbagai sumber seperti server, mencakup aktivitas seperti autentikasi dan aktivitas jaringan.

### Proses SIEM (Tiga Langkah)

1. **Collect and Aggregate Data**
   - Mengumpulkan data peristiwa dari berbagai sumber.
2. **Normalize Data**
   - Mengonversi data ke format standar agar konsisten, mudah dibaca, dan dicari.
3. **Analyze Data**
   - Menganalisis dan menghubungkan data untuk mengidentifikasi pola yang mencurigakan.

### Proses Log Ingestion

- SIEM membuat salinan data peristiwa untuk dianalisis tanpa mengubah log asli.
- Data yang terkumpul menjadi platform terpusat bagi analis keamanan untuk menganalisis dan merespons insiden.

### Log Forwarders

- **Log forwarders** adalah perangkat lunak yang mengotomatisasi pengumpulan dan pengiriman data log ke alat SIEM.
- Beberapa sistem operasi memiliki log forwarder bawaan, sementara lainnya membutuhkan perangkat lunak pihak ketiga.
- Konfigurasi log forwarder melibatkan:
  - Spesifikasi log yang akan diteruskan.
  - Lokasi tujuan pengiriman (misalnya, alat SIEM).

### Pemilihan Log Forwarder

- Faktor yang perlu dipertimbangkan:
  - Kebutuhan sistem atau organisasi.
  - Kompatibilitas dengan infrastruktur yang ada.
  - Dukungan untuk forwarder bawaan, pihak ketiga, atau open-source.

### Poin Penting

- **Data adalah inti dari alat SIEM.**
  - Analis keamanan menggunakan SIEM untuk mengakses dan menganalisis log selama investigasi insiden.
  - Memahami proses log ingestion penting untuk melacak sumber insiden keamanan.

### Sumber Referensi

- Panduan:
  - **Cara mengintegrasikan data ke Splunk**
  - **Proses data ingestion di Chronicle**
- **Pro tip**: Ikuti langkah-langkah untuk mendaftar Splunk Cloud dan mulai eksplorasi menggunakan data log Anda sendiri.
