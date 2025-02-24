---
id: The TCP/IP model
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Model TCP/IP

**TCP/IP** (Transmission Control Protocol dan Internet Protocol) adalah model standar untuk komunikasi jaringan. Berikut penjelasan lebih lanjut tentang masing-masing protokol:

#### 1. **TCP (Transmission Control Protocol)**

- **Fungsi**: Memungkinkan dua perangkat untuk membentuk koneksi dan mentransfer data secara berkelanjutan.
- **Tugas**:
  - Mengorganisir data ke dalam **paket** agar dapat dikirimkan melalui jaringan.
  - Memastikan data mencapai tujuan yang tepat dan dalam urutan yang benar.

#### 2. **IP (Internet Protocol)**

- **Fungsi**: Menangani pengalamatan dan routing paket data antar perangkat di jaringan.
- **Tugas**:
  - Menyediakan **alamat IP** yang berfungsi sebagai identifikasi setiap perangkat di jaringan.
  - Mengatur rute data agar dapat sampai ke perangkat yang tepat.

### **Port dalam Jaringan**

- **Port** adalah lokasi berbasis perangkat lunak dalam sistem operasi perangkat yang berfungsi untuk mengatur dan memprioritaskan pengiriman serta penerimaan data antara perangkat.
- **Fungsi**:
  - Membagi lalu lintas jaringan berdasarkan jenis layanan yang akan dijalankan antara dua perangkat.
  - Menentukan bagaimana data diproses berdasarkan nomor port yang ditugaskan.
  - **Contoh**: Bayangkan mengirim surat ke teman di gedung apartemen—port menentukan di mana surat itu harus dikirimkan di dalam gedung tersebut.

### **Port Umum**

- **Port 25**: Digunakan untuk email (SMTP).
- **Port 443**: Digunakan untuk komunikasi internet yang aman (HTTPS).
- **Port 20**: Digunakan untuk transfer file (FTP).

### Catatan Tambahan

- Data yang dikirimkan melalui jaringan terdiri dari paket yang berisi instruksi, seperti alamat tujuan dan port tujuan. Paket data tersebut membantu perangkat penerima mengetahui cara memproses informasi yang ada di dalamnya.
- Dalam TCP/IP, port berperan penting untuk membedakan dan memprioritaskan layanan yang berbeda pada perangkat jaringan, sehingga setiap layanan dapat berjalan dengan lancar tanpa saling mengganggu.
