---
id: IP addresses and network communication
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan tentang IP Address dan MAC Address

#### **Pengertian IP Address**

- **IP Address (Internet Protocol Address)**:
  - Identifikasi unik untuk perangkat di internet.
  - Ibarat alamat rumah, setiap perangkat memiliki alamat yang berbeda di internet.
- **Tipe IP Address**:

  1. **IPv4 (Internet Protocol Version 4)**:
     - Ditulis dalam format 4 angka (1-3 digit), dipisahkan dengan tanda titik (contoh: `192.168.1.1`).
     - Merupakan format awal, tetapi alamatnya hampir habis karena banyaknya perangkat yang terkoneksi.
  2. **IPv6 (Internet Protocol Version 6)**:

     - Terdiri dari 32 karakter alfanumerik.
     - Dikembangkan untuk mendukung lebih banyak perangkat di internet.

  3. Contoh:
     Berikut adalah contoh format dan alamat **IPv6**:

### **Format IPv6**

- Terdiri dari 8 kelompok angka heksadesimal (0-9, a-f), dipisahkan oleh tanda titik dua `:`.
- Setiap kelompok terdiri dari 4 digit (16-bit), sehingga total panjangnya adalah 128-bit.

### **Contoh Alamat IPv6**

1. **Alamat penuh (full address):**
   `2001:0db8:85a3:0000:0000:8a2e:0370:7334`

2. **Alamat yang dipersingkat:**
   - IPv6 memungkinkan penghapusan angka nol di awal setiap kelompok:
     `2001:db8:85a3:0:0:8a2e:370:7334`
   - Jika ada beberapa kelompok yang hanya berisi nol, dapat disingkat menjadi `::` (hanya boleh satu kali dalam satu alamat):
     `2001:db8:85a3::8a2e:370:7334`

---

#### **Jenis IP Address**

1. **Public IP Address**:

   - Diberikan oleh penyedia layanan internet (ISP).
   - Bersifat global dan terhubung dengan lokasi geografis Anda.
   - Semua perangkat dalam satu jaringan berbagi alamat IP publik yang sama (contoh: rumah dengan beberapa penghuni berbagi alamat surat yang sama).

2. **Private IP Address**:
   - Hanya terlihat di dalam jaringan lokal.
   - Digunakan untuk komunikasi antar perangkat dalam jaringan yang sama (contoh: komputer, ponsel, atau printer di jaringan rumah).

---

#### **MAC Address (Media Access Control)**

- Alamat unik yang diberikan pada perangkat keras jaringan (misalnya kartu jaringan).
- **Fungsi**:
  - Digunakan oleh switch untuk mengarahkan data ke perangkat tujuan.
  - Switch menyimpan alamat ini dalam **MAC Address Table**, seperti buku alamat untuk memastikan data dikirim ke perangkat yang benar.

---

### **Kesimpulan Utama**

- **IPv4** dan **IPv6** adalah tipe utama alamat IP. IPv6 memungkinkan lebih banyak perangkat terkoneksi karena panjang alamatnya.
- **IP Address** dibagi menjadi **publik** (terlihat oleh internet) dan **privat** (digunakan dalam jaringan lokal).
- **MAC Address** berfungsi di tingkat perangkat keras untuk mengarahkan komunikasi dalam jaringan.
