---
id: The evolution of hash functions
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Evolusi Fungsi Hash dalam Keamanan Data**

### **1. Apa Itu Fungsi Hash?**

![hash](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qISzBqG7RmukCvKmeU83mg_e0d4d256b3bb41be8504685b3338fcf1_CS_R-094_Hashing-algorithm.png?expiry=1736035200000&hmac=ZUW0SrqVN-XRi1C7MlIgqZd6CW8sAARejO850xvr564)

- Fungsi hash adalah algoritma yang menghasilkan nilai unik (**hash value**) untuk memvalidasi integritas data.
- Hashing sering digunakan untuk **autentikasi** dan **non-repudiation** (keaslian informasi tidak dapat disangkal).

---

### **2. Awal Mula Hashing**

![hash2](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4XExarUSRWuWRaIX64HrVw_2cb75b41a08b4817b5789ad39e861ff1_CS_R-094_Orgins-of-Hashing.png?expiry=1736035200000&hmac=qzVq-Wfuo5Y9kbr0i6qieNlSGVvYNItP-dW_imsFB8s)

- Fungsi hash pertama kali dibuat untuk mempermudah pencarian data.
- **Hash table**: Struktur data yang digunakan untuk menyimpan dan mereferensikan nilai hash.
- **MD5 (Message Digest 5)**: Dikembangkan oleh Ronald Rivest pada 1990-an untuk memverifikasi integritas file.
  - Menghasilkan nilai hash 128-bit (32 karakter).
  - **Masalah:** Rentan terhadap **hash collision** (dua input berbeda menghasilkan hash yang sama).

---

### **3. Masalah pada Hash Collision**
- Hash collision terjadi karena jumlah input tidak terbatas, tetapi output hash bersifat tetap.
- Contoh serangan: **Collision attack** yang memungkinkan penyerang memalsukan data otentik.

---

### **4. Hashing Generasi Berikutnya: SHA (Secure Hashing Algorithm)**
- SHA dikembangkan untuk mengatasi kelemahan MD5 dengan menghasilkan hash lebih panjang dan lebih aman.
- **Lima algoritma SHA yang disetujui NIST:**
  - SHA-1: 160-bit (sudah tidak direkomendasikan).
  - SHA-224
  - SHA-256
  - SHA-384
  - SHA-512

---

### **5. Hashing untuk Keamanan Password**
- **Mekanisme umum:**
  - Password disimpan dalam database sebagai hash.
  - Ketika login, password yang dimasukkan di-hash lalu dibandingkan dengan hash di database.
- **Masalah:** Jika database dicuri, hash dapat digunakan untuk membongkar password melalui **rainbow table** (daftar hash yang dipetakan dengan plaintext).

---

### **6. Menambahkan “Salt” untuk Pengamanan Tambahan**

![hash3](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/VJFA9qhuRvan1_hRvGhSpg_70858cdbe6d94ad29538d1915f0e05f1_CS_R-094_Salting.png?expiry=1736035200000&hmac=xWWzsfxD5giYTd89RiUgIwVx5DpZPNs_GiSrk1rd414)

- **Salt:** String acak yang ditambahkan sebelum data di-hash.
  - Menghasilkan hash unik, meskipun passwordnya sama.
  - Membuat serangan rainbow table tidak efektif.
- **Keamanan tambahan:** Salt yang lebih panjang dan kompleks membuat data lebih sulit diretas.

---

### **7. Rangkuman Penting**
- **Fungsi hash** memvalidasi integritas data dan melindungi dari pelanggaran keamanan.
- **Masalah MD5:** Rentan terhadap hash collision dan rainbow table attacks.
- **SHA dan salting** menawarkan solusi yang lebih aman.
- Keamanan optimal memerlukan pemilihan algoritma hashing yang tepat dan penggunaan salt yang kuat.

Dengan memahami evolusi fungsi hash, Anda lebih siap membuat rekomendasi keamanan yang relevan dan efektif.
