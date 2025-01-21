---
id: The four layers of the TCP/IP model
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Model TCP/IP dan Empat Lapisan

**TCP/IP model** adalah kerangka kerja yang digunakan untuk memvisualisasikan cara data diorganisasi dan dikirimkan melalui jaringan. Model ini sangat penting bagi profesional keamanan untuk memantau dan melindungi jaringan dari potensi risiko. Model TCP/IP terdiri dari empat lapisan, masing-masing memiliki peran spesifik dalam proses komunikasi data.

---

#### **1. Network Access Layer (Lapisan Akses Jaringan)**

- **Fungsi Utama**:
  - Membuat paket data dan mengirimkannya melalui jaringan.
  - Mengatur perangkat keras seperti kabel fisik, switch, dan perangkat jaringan lainnya untuk memastikan data mencapai tujuan.
- **Tugas**:
  - Menangani komunikasi pada tingkat fisik, termasuk pengaturan perangkat yang terhubung.
  - Mengatur alur data dari perangkat melalui media fisik seperti Ethernet atau Wi-Fi.

---

#### **2. Internet Layer (Lapisan Internet)**

- **Fungsi Utama**:
  - Menambahkan alamat IP ke paket data untuk menunjukkan lokasi pengirim dan penerima.
  - Menentukan apakah data akan tetap di jaringan lokal (**LAN**) atau dikirim ke jaringan jarak jauh seperti internet.
- **Tugas**:
  - Menangani **routing** dan pengalamatan data.
  - Mengatur bagaimana jaringan lokal terhubung dengan jaringan global.
  - Membantu dalam proses fragmentasi dan reassembly paket data untuk efisiensi pengiriman.

---

#### **3. Transport Layer (Lapisan Transportasi)**

- **Fungsi Utama**:
  - Mengontrol aliran data di seluruh jaringan.
  - Memastikan data diterima secara utuh dan dalam urutan yang benar.
- **Tugas**:
  - Menyediakan **error control** untuk memastikan pengiriman data yang lancar.
  - Memungkinkan atau menolak komunikasi dengan perangkat lain berdasarkan protokol tertentu.
  - Mengelola status koneksi antara pengirim dan penerima.

---

#### **4. Application Layer (Lapisan Aplikasi)**

- **Fungsi Utama**:
  - Menentukan bagaimana data berinteraksi dengan perangkat penerima.
  - Menyediakan antarmuka untuk layanan jaringan seperti transfer file, email, atau browsing.
- **Tugas**:
  - Menangani protokol seperti HTTP, FTP, dan SMTP.
  - Mengatur fungsi-fungsi yang berguna bagi pengguna akhir, misalnya akses aplikasi berbasis web atau layanan email.

---

### **Catatan Tambahan**

1. **Pentingnya Model TCP/IP dalam Keamanan Jaringan**:

   - Model ini membantu profesional keamanan untuk memahami bagaimana data mengalir di jaringan sehingga potensi risiko dapat diidentifikasi pada lapisan yang relevan.
   - Setiap lapisan dapat menjadi target serangan tertentu:
     - Lapisan Akses Jaringan rentan terhadap serangan perangkat keras.
     - Lapisan Internet sering menghadapi serangan IP spoofing.
     - Lapisan Transport rentan terhadap serangan seperti **Denial of Service (DoS)**.
     - Lapisan Aplikasi dapat diserang melalui eksploitasi layanan aplikasi seperti HTTP.

2. **Protokol Utama di Setiap Lapisan**:
   - **Network Access Layer**: Ethernet, Wi-Fi.
   - **Internet Layer**: IPv4, IPv6.
   - **Transport Layer**: TCP, UDP.
   - **Application Layer**: HTTP, FTP, SMTP, DNS.
