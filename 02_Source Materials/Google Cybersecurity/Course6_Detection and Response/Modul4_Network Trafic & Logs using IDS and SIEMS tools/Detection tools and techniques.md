---
id: Detection tools and techniques
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan Materi: Detection Tools and Techniques

1. **IDS: Pengertian dan Fungsi**
   - IDS (Intrusion Detection System) adalah aplikasi yang memonitor aktivitas sistem dan memberikan peringatan atas potensi intrusi.
   - Membantu organisasi memantau sistem dan jaringan untuk mendeteksi aktivitas berbahaya.
   - Berdasarkan lokasi instalasinya, IDS terbagi menjadi:
     - **Host-Based IDS (HIDS)**: Memantau aktivitas di perangkat tertentu (host).
     - **Network-Based IDS (NIDS)**: Memantau lalu lintas jaringan di seluruh jaringan.

2. **Host-Based Intrusion Detection System (HIDS)**
![HIDS](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/r9hBQHsQSv-hult8KB1V8g_17a68a6257c143738588e048ca8d26f1_FhxPKoFNfXgXc6ReM_Srb2o974QJ0U-ULsPViUoB-bhM_iCgEJA4kCxBBaXg8V_I8OgPIpF5g77EffByf9aub_pTG33UzSLum4eyKCK7YZPXGvZjqG1jLW-bJ4yozWlzoOSJ7i99ZiyAfKfNBe0DyFMKE3UyQv--RRTEACIegsbPdyqlv4gHQAGRdIyMMQ?expiry=1736294400000&hmac=5Gs4ZhPJ8q4glUl25NaoVLUZ5BZ2xSPZmualxNtYd04)
   - **Definisi**: Aplikasi yang dipasang sebagai agen di perangkat untuk memonitor aktivitas lokal.
   - **Karakteristik**:
     - Memonitor file system, penggunaan sumber daya, aktivitas pengguna, dan lainnya.
     - Mengidentifikasi aktivitas tidak sah, seperti instalasi aplikasi yang tidak diotorisasi.
     - Fokus pada aktivitas internal perangkat.
   - **Keunggulan**:
     - Memberikan visibilitas mendalam atas aktivitas perangkat.
   - **Keterbatasan**:
     - Hanya memonitor perangkat tempat HIDS dipasang.

3. **Network-Based Intrusion Detection System (NIDS)**
![NIDS](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/m2NQ9waXQzm_kmnrpieaAQ_081c3ddbccb64cf8aa0ad09806fdf8f1_CS_R-137_NIDS.png?expiry=1736294400000&hmac=Vhk5g_tm_tRboLGHK6pz9J8UTjBR23m-jDCwGFBn72s)
   - **Definisi**: Aplikasi yang memonitor lalu lintas jaringan pada titik tertentu di jaringan.
   - **Karakteristik**:
     - Menginspeksi data dari berbagai perangkat yang terhubung ke jaringan.
     - Mengidentifikasi lalu lintas jaringan yang mencurigakan.
   - **Keunggulan**:
     - Memberikan visibilitas atas aktivitas di seluruh jaringan.
   - **Keterbatasan**:
     - Tidak dapat melihat aktivitas internal perangkat.

4. **Penggunaan Kombinasi HIDS dan NIDS**
   - Kombinasi HIDS dan NIDS memberikan pendekatan multi-layered untuk deteksi intrusi.
   - HIDS dan NIDS memberikan perspektif berbeda, menghasilkan pandangan yang komprehensif atas aktivitas lingkungan.

5. **Teknik Deteksi pada IDS**
   IDS menggunakan dua metode utama untuk mendeteksi ancaman:

   - **Signature-Based Analysis**:
     - **Definisi**: Deteksi berdasarkan pola (signature) yang dikenal terkait dengan aktivitas berbahaya.
     - **Proses**:
       - Membandingkan aktivitas dengan pola yang didefinisikan dalam database signature.
       - Contoh: Menditeksi malware berdasarkan script berbahaya yang dikenal.
     - **Keunggulan**:
       - Tingkat false positive rendah.
       - Efektif untuk mendeteksi ancaman yang dikenal.
     - **Keterbatasan**:
       - Tidak dapat mendeteksi ancaman baru (zero-day attack).
       - Memerlukan pembaruan database signature secara berkala.
       - Pola dapat dimodifikasi oleh penyerang untuk menghindari deteksi.

   - **Anomaly-Based Analysis**:
     - **Definisi**: Deteksi berdasarkan perilaku yang menyimpang dari baseline normal.
     - **Proses**:
       - **Fase Pelatihan**: Mengumpulkan data untuk membangun baseline perilaku normal.
       - **Fase Deteksi**: Membandingkan aktivitas saat ini dengan baseline.
       - Aktivitas yang menyimpang dari baseline dicatat dan menghasilkan peringatan.
     - **Keunggulan**:
       - Dapat mendeteksi ancaman baru yang belum dikenal.
     - **Keterbatasan**:
       - Tingkat false positive tinggi, karena perilaku normal yang menyimpang juga dapat terdeteksi.
       - Baseline yang tercemar oleh aktivitas penyerang akan menyebabkan gagal mendeteksi ancaman yang sudah ada.

6. **Takeaways**
   - IDS adalah alat penting dalam keamanan untuk memantau dan mendeteksi aktivitas berbahaya.
   - **HIDS**: Fokus pada perangkat individu; **NIDS**: Fokus pada jaringan secara keseluruhan.
   - Teknik deteksi:
     - **Signature-Based**: Akurat untuk ancaman yang dikenal.
     - **Anomaly-Based**: Fleksibel untuk ancaman baru tetapi rawan false positive.

### Catatan
Pemahaman akan keunggulan dan keterbatasan setiap metode sangat penting untuk menginterpretasikan data IDS dan merespons insiden keamanan dengan tepat.
