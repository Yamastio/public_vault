---
id: Security monitoring with detection tools
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan Materi

1. **Deteksi Memerlukan Data**
   - Data untuk deteksi diperoleh dari berbagai sumber, termasuk log yang dihasilkan oleh perangkat.
   - Telemetri adalah pengumpulan dan transmisi data untuk dianalisis. Contohnya:
     - Log merekam kejadian pada sistem.
     - Telemetri seperti packet capture menggambarkan data jaringan itu sendiri.

2. **Log dan Telemetri Sebagai Bukti**
   - Log dan telemetri adalah sumber bukti penting dalam investigasi keamanan.

3. **Intrusion Detection System (IDS)**
   - IDS adalah aplikasi yang memonitor aktivitas dan memberikan peringatan atas potensi intrusi.
   - IDS dapat memonitor berbagai bagian sistem atau jaringan.

4. **Endpoint dan Host**
   - **Endpoint**: Perangkat yang terhubung ke jaringan, seperti laptop, tablet, atau smartphone.
   - **Host**: Perangkat apa pun yang berkomunikasi di jaringan. Dalam konteks ini, host sering kali adalah endpoint.

5. **Host-Based Intrusion Detection System (HIDS)**
   - HIDS dipasang sebagai agen di host tertentu (misalnya laptop atau server).
   - Fungsi:
     - Memantau aktivitas host.
     - Mendeteksi aktivitas mencurigakan.
     - Menghasilkan log dan peringatan.

6. **Network-Based Intrusion Detection System (NIDS)**
   - NIDS memonitor lalu lintas jaringan dan data di titik tertentu dalam jaringan.
   - Karakteristik:
     - Bekerja mirip dengan packet sniffer.
     - Menggunakan beberapa sensor IDS di berbagai titik jaringan untuk visibilitas yang optimal.
     - Menghasilkan log dan peringatan jika mendeteksi aktivitas jaringan yang mencurigakan.

7. **Metode Deteksi pada IDS**
   - **Signature Analysis**:
     - Metode deteksi berdasarkan aturan tertentu (signature).
     - Jika aktivitas sesuai dengan aturan, IDS akan mencatatnya sebagai log dan mengirimkan peringatan.
     - Contoh: Peringatan untuk tiga kali gagal login berturut-turut yang mengindikasikan serangan password.

8. **Log IDS**
   - Informasi yang dicatat oleh IDS dapat dikirim, disimpan, dan dianalisis menggunakan sistem terpusat seperti SIEM.

### Penutup
Setelah memahami konsep IDS, kita akan belajar cara membaca dan mengonfigurasi signature untuk mendeteksi aktivitas yang mencurigakan.

