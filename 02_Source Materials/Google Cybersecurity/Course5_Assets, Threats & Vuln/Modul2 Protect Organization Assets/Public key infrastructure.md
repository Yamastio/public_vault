---
id: Public key infrastructure
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan: Public Key Infrastructure (PKI)

### Apa Itu PKI?
- **Public Key Infrastructure (PKI)**:
  - Kerangka kerja enkripsi untuk mengamankan pertukaran informasi online.
  - Membuat akses data menjadi cepat, mudah, dan aman.

### Proses PKI
PKI memiliki dua langkah utama:
1. **Pertukaran Informasi yang Dienkripsi**:
   - **Asymmetric Encryption**:
     - Menggunakan sepasang kunci: **public key** dan **private key**.
     - Public key:
       - Digunakan untuk mengenkripsi informasi.
       - Bisa dibagikan secara luas.
     - Private key:
       - Digunakan untuk mendekripsi informasi.
       - Hanya pemiliknya yang memiliki akses.
     - Kelebihan: Sangat aman.
     - Kekurangan: Lambat.
   - **Symmetric Encryption**:
     - Menggunakan satu kunci rahasia untuk mengenkripsi dan mendekripsi informasi.
     - Kelebihan: Cepat.
     - Kekurangan: Kurang aman karena kunci harus dibagikan.
   - PKI sering menggabungkan keduanya:
     - **Asymmetric encryption** untuk memulai koneksi (fokus pada keamanan).
     - **Symmetric encryption** untuk komunikasi lanjutan (fokus pada kecepatan).

2. **Membangun Kepercayaan**:
   - Tantangan utama: Membagikan kunci dengan aman tanpa risiko penyalahgunaan, kehilangan, atau pencurian.
   - Solusi: **Digital Certificates**.

### Apa Itu Digital Certificate?
- **Digital Certificate**:
  - File yang memverifikasi identitas pemegang public key.
  - Digunakan untuk menunjukkan kepercayaan antar komputer dan jaringan.
- **Proses Pembuatan Digital Certificate**:
  1. Bisnis mendaftarkan domain dan mengirim informasi (seperti nama perusahaan, lokasi, dan public key) ke **Certificate Authority (CA)**.
  2. CA memverifikasi identitas perusahaan.
  3. Jika terkonfirmasi, CA mengenkripsi data perusahaan dengan **private key** miliknya dan membuat digital certificate.
  4. Sertifikat ini mencakup data terenkripsi dan **digital signature** CA untuk memastikan keasliannya.

### Keunggulan PKI
- Mengatasi kelemahan dalam berbagi kunci dengan:
  - Kombinasi **asymmetric dan symmetric encryption**.
  - Sistem **digital certificates** untuk membangun kepercayaan.
- Menjadikan PKI sebagai kontrol keamanan yang andal untuk melindungi informasi online.
