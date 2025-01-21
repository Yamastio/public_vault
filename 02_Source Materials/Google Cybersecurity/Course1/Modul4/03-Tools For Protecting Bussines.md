---
id: 03-Tools For Protecting Bussines
aliases: []
tags: []
---

## Rangkuman

Analis keamanan pemula memiliki berbagai alat dalam toolkit mereka yang dirancang untuk membantu mengidentifikasi, menilai, dan mengurangi risiko keamanan. Alat-alat ini, seperti SIEM, playbooks, dan network protocol analyzers, membantu meringankan beban kerja dengan mengorganisasi data, memberikan panduan prosedur, dan memantau lalu lintas jaringan. Artikel ini juga menjelaskan dua jenis playbooks yang penting dalam investigasi forensik: **chain of custody** dan **protecting and preserving evidence**, yang memastikan bukti digital dikelola dan dilindungi dengan benar.


## **Poin-Poin Penting**

1. **Toolkit Analis Keamanan Pemula**:

   - Setiap organisasi menyediakan alat yang berbeda sesuai dengan kebutuhan keamanannya.
   - Penting untuk memahami alat standar industri dan menunjukkan kemampuan belajar menggunakan alat serupa.

2. **Security Information and Event Management (SIEM) Tools**:

   - **Fungsi**: Mengumpulkan dan menganalisis data log untuk memonitor aktivitas kritis organisasi.
   - **Manfaat**:
     - Mengurangi waktu analisis log.
     - Memberikan dasbor visual untuk menyusun data ke dalam kategori yang mudah diakses.
   - **Hosting**:
     - On-premise: Memerlukan pengaturan dan perawatan manual, cocok untuk tim yang lebih berpengalaman.
     - Cloud-hosted: Mudah diatur dan dikelola, cocok untuk tim yang kurang berpengalaman.

3. **Network Protocol Analyzers (Packet Sniffers)**:

   - **Fungsi**: Menangkap dan menganalisis lalu lintas data di jaringan.
   - Contoh alat: **tcpdump** dan **Wireshark**.
   - Digunakan untuk memonitor data jaringan dan mengidentifikasi ancaman.

4. **Playbooks**:

   - **Definisi**: Panduan manual untuk tindakan operasional, seperti respons insiden.
   - **Jenis Playbooks**:
     - **Chain of Custody Playbook**:
       - Mencatat kepemilikan dan pengendalian bukti selama siklus hidup insiden.
       - Menyimpan catatan siapa yang mengakses bukti dan untuk apa.
     - **Protecting and Preserving Evidence Playbook**:
       - Memastikan bukti digital yang rapuh dan volatil dikelola dengan benar.
       - Mengikuti **order of volatility** untuk memprioritaskan data yang harus diselamatkan terlebih dahulu.
       - Menghindari pengelolaan yang salah agar bukti tetap valid.

5. **Tips untuk Karier di Investigasi Forensik**:

   - Jika tertarik pada investigasi forensik, eksplorasi lebih lanjut tentang alat dan konsep forensik sangat dianjurkan.
   - Dalam investigasi, menjaga keutuhan bukti digital adalah prioritas utama.

6. **Sumber Informasi Tambahan**:
   - **Google Cybersecurity Action Team's Threat Horizon Report**: Memberikan wawasan strategis untuk ancaman keamanan cloud.
   - **CISA (Cybersecurity & Infrastructure Security Agency)**: Menyediakan daftar alat keamanan siber gratis yang dapat dijadikan referensi.

### **Kesimpulan**

Pemahaman tentang alat seperti SIEM, playbooks, dan packet sniffers sangat penting untuk analis keamanan. Playbooks memastikan prosedur investigasi forensik dijalankan dengan benar, sedangkan alat-alat lain membantu dalam analisis data dan pemantauan ancaman. Eksplorasi lebih lanjut dalam keamanan forensik dapat membuka peluang karier yang lebih spesifik di bidang ini.
