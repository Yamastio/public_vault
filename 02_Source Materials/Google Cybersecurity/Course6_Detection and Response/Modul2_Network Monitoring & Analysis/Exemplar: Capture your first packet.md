---
id: "Exemplar: Capture your first packet"
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Rangkuman Aktivitas: Menangkap Paket Pertama Menggunakan `tcpdump`

### **Tujuan Aktivitas**
Sebagai analis keamanan jaringan, Anda akan:
- Mengidentifikasi antarmuka jaringan untuk menangkap data paket.
- Menggunakan **tcpdump** untuk memfilter lalu lintas jaringan secara langsung.
- Menyimpan lalu lintas jaringan ke file **.pcap** untuk dianalisis lebih lanjut.
- Memfilter data yang telah ditangkap untuk memahami detail lalu lintas jaringan.

---

### **Langkah-langkah**

#### **Tugas 1: Mengidentifikasi Antarmuka Jaringan**
1. **Gunakan perintah `ifconfig`** untuk melihat antarmuka yang tersedia:
   ```bash
   sudo ifconfig
   ```
   - Contoh output: Menampilkan antarmuka seperti `eth0` dan `lo`.
   - Anda akan menggunakan `eth0` untuk menangkap paket dalam lab ini.

2. **Gunakan perintah `tcpdump -D`** untuk daftar antarmuka yang dapat digunakan:
   ```bash
   sudo tcpdump -D
   ```

---

#### **Tugas 2: Memfilter Lalu Lintas Jaringan Langsung**
1. **Jalankan `tcpdump` untuk menangkap paket langsung dari antarmuka `eth0`:**
   ```bash
   sudo tcpdump -i eth0 -v -c5
   ```
   - **Opsi:**
     - `-i eth0`: Antarmuka jaringan yang digunakan.
     - `-v`: Menampilkan data paket secara rinci.
     - `-c5`: Hentikan setelah menangkap 5 paket.
   - **Output**: Menampilkan data paket termasuk timestamp, tipe protokol, dan IP sumber/destinasi.

2. **Detail yang ditampilkan:**
   - Informasi seperti **timestamp**, **TTL**, **flags**, dan **checksum**.
   - Contoh: `7acb26dc1f44.5000 > nginx-us-east1-c.c.qwiklabs-terminal-vms-prod-00.internal.59788`.

---

#### **Tugas 3: Menyimpan Lalu Lintas Jaringan ke File**
1. **Simpan data ke file bernama `capture.pcap`:**
   ```bash
   sudo tcpdump -i eth0 -nn -c9 port 80 -w capture.pcap &
   ```
   - **Opsi:**
     - `-nn`: Nonaktifkan lookup nama IP dan port.
     - `-c9`: Tangkap 9 paket saja.
     - `port 80`: Filter lalu lintas HTTP.
     - `-w capture.pcap`: Simpan data ke file.
     - `&`: Jalankan perintah di latar belakang.

2. **Hasilkan lalu lintas HTTP dengan `curl`:**
   ```bash
   curl opensource.google.com
   ```
   - Mengirimkan permintaan HTTP untuk menghasilkan lalu lintas yang dapat ditangkap.

3. **Verifikasi file `capture.pcap`:**
   ```bash
   ls -l capture.pcap
   ```

---

#### **Tugas 4: Memfilter Data dari File yang Tersimpan**
1. **Analisis file `capture.pcap`:**
   ```bash
   sudo tcpdump -nn -r capture.pcap -v
   ```
   - **Opsi:**
     - `-nn`: Nonaktifkan lookup nama IP dan port.
     - `-r`: Baca data dari file.
     - `-v`: Tampilkan data paket secara rinci.

2. **Output**:
   - Informasi seperti:
     - **IP sumber/destinasi**.
     - **Protokol**: TCP/UDP.
     - **Flags**: Misalnya `[S]` untuk SYN, `[P.]` untuk Push dan ACK.

---

### **Kesimpulan**
- Anda telah belajar menangkap lalu lintas jaringan langsung menggunakan **tcpdump**, menyimpannya ke file, dan menganalisis isinya.
- **tcpdump** adalah alat penting untuk menganalisis lalu lintas jaringan dalam lingkungan Linux, terutama untuk investigasi keamanan jaringan.

#### **Tips Tambahan**
- Selalu gunakan opsi seperti `-nn` untuk menghindari pengungkapan data sensitif selama investigasi.
- Latih keterampilan Anda dengan berbagai skenario lalu lintas jaringan untuk memahami pola data yang berbeda.
