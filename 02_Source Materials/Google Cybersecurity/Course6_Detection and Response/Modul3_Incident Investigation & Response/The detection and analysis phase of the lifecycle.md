---
id: The detection and analysis phase of the lifecycle
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Detection and Analysis Phase**:
1. **Pendeteksian Insiden**:
   - Tujuannya adalah menemukan *security events* secara cepat.
   - **Event vs. Incident**:
     - *Events*: Aktivitas rutin, seperti kunjungan situs web atau permintaan reset password.
     - *Incidents*: *Events* yang mengancam keamanan, misalnya akses tidak sah.
   - Alat bantu seperti **IDS (Intrusion Detection Systems)** dan **SIEM (Security Information and Event Management)** digunakan untuk menganalisis data *events* dan mendeteksi aktivitas mencurigakan.

2. **Proses Analisis**:
   - Dimulai saat *alert* dikirim setelah pendeteksian insiden.
   - **Tujuan**:
     - Investigasi dan validasi *alerts*.
     - Memeriksa *indicators of compromise* untuk memastikan adanya insiden.
   - **Keterampilan Kritis**:
     - Berpikir kritis dan analisis mendalam untuk memvalidasi setiap *alert*.

## **Tantangan Dalam Detection dan Analysis**:
1. **Deteksi Tidak Sempurna**:
   - Tidak semua insiden dapat terdeteksi.
   - Alat deteksi terbaik sekalipun memiliki keterbatasan, dan implementasi alat otomatis terkadang belum merata.

2. **Volume Alerts Tinggi**:
   - Bisa mencapai ribuan per shift, dengan penyebab:
     - **False Positives**: Akibat pengaturan *alert* yang terlalu luas dan tidak sesuai dengan lingkungan organisasi.
     - **Alerts Valid**: Misalnya serangan nyata akibat eksploitasi kerentanan baru.

3. **Kebutuhan Perencanaan**:
   - Insiden tak terhindarkan, sehingga organisasi memerlukan **incident response plan** yang kuat.

## **Poin Penting untuk Security Analyst**:
- Harus mampu menganalisis *alerts* secara efektif.
- Mengutamakan validasi dan investigasi mendalam untuk membedakan *false positives* dari ancaman nyata.

Selanjutnya, Anda akan belajar bagaimana menangani analisis *alerts* secara langsung. Bersiaplah untuk tantangan berikutnya!
