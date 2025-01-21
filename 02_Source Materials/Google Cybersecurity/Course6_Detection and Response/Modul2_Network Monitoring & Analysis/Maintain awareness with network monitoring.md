---
id: Maintain awareness with network monitoring
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan: Pemantauan dan Perlindungan Jaringan

**Pemantauan Jaringan**:
- **Jaringan Komunikasi** menghasilkan berbagai aktivitas seperti mengirim email atau streaming video, yang membentuk **lalu lintas jaringan**.
- Pemantauan jaringan adalah kunci untuk mengetahui aktivitas yang terjadi di jaringan dan mendeteksi aktivitas mencurigakan.

**Mengenal Jaringan Anda**:
- Jaringan menghubungkan perangkat dan menggunakan **protokol jaringan** untuk bertukar data. Informasi seperti **alamat IP sumber dan tujuan** dan jumlah data yang ditransfer sangat berharga untuk **membangun baseline**.
- **Baseline** membantu Anda memahami perilaku jaringan yang normal, sehingga memudahkan untuk mengidentifikasi **perilaku abnormal** yang perlu diselidiki.

**Cara Memantau Jaringan**:
- Setelah menetapkan baseline, Anda dapat memantau jaringan untuk mendeteksi **deviasi** dari baseline tersebut.
- Beberapa komponen jaringan yang bisa dipantau:
  - **Analisis Aliran**: Memantau **protokol** dan **port** untuk menemukan pola yang tidak biasa, seperti penggunaan port yang tidak umum untuk komunikasi yang mencurigakan.
  - **Informasi Payload Paket**: Memeriksa data yang ditransmisikan dalam paket untuk mendeteksi aktivitas yang mencurigakan, seperti data sensitif yang diekstrak.
  - **Pola Temporal**: Memantau waktu trafik jaringan untuk mengetahui apakah ada aktivitas yang terjadi di luar jam normal yang dapat menunjukkan potensi ancaman.

**Melindungi Jaringan Anda**:
- **SOC (Security Operations Center)** dan **NOC (Network Operations Center)** adalah unit yang berfokus pada pemantauan keamanan dan kinerja jaringan, masing-masing.
- Profesional keamanan menggunakan alat untuk mendeteksi dan melindungi jaringan dari ancaman, termasuk:
  - **Sistem Deteksi Intrusi (IDS)**: Memantau aktivitas sistem dan memberi peringatan tentang potensi intrusi.
  - **Alat Penganalisis Protokol Jaringan (Packet Sniffers)**: Seperti **tcpdump** dan **Wireshark**, untuk menangkap dan menganalisis data lalu lintas jaringan.

**Poin Penting**:
- Pemantauan dan perlindungan jaringan adalah tugas utama profesional keamanan. Mengetahui apa yang terjadi di jaringan memungkinkan Anda melindunginya dengan lebih baik.
- **Baseline** membantu mengenali pola lalu lintas jaringan yang biasa dan mendeteksi deviasi yang mencurigakan.
- Alat seperti **IDS** dan **packet sniffers** sangat penting dalam mendeteksi ancaman dan memantau aktivitas jaringan.

**Sumber Daya**:
- Untuk mempelajari lebih lanjut tentang teknik **eksfiltrasi data** dan **komponen jaringan** yang dapat dipantau, cek referensi dari **MITRE ATT&CK®**.
