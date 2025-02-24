---
id: Cryptography and cloud security
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Penguatan Keamanan Cloud (Cloud Security Hardening)

Berikut adalah teknik utama untuk meningkatkan keamanan infrastruktur cloud:

1. **Identity Access Management (IAM):**

   - Mengelola identitas digital dan otorisasi akses ke sumber daya cloud.

2. **Hypervisors:**

   - Mengabstraksi perangkat keras host dari lingkungan perangkat lunak.
   - **Tipe:**
     - **Tipe 1:** Berjalan langsung pada perangkat keras (contoh: VMware ESXi).
     - **Tipe 2:** Berjalan pada perangkat lunak host (contoh: VirtualBox).
   - **Risiko:** Kerentanan dapat menyebabkan "VM escape," di mana aktor jahat mengakses hypervisor dan lingkungan lain.

3. **Baselining:**

   - Menetapkan titik referensi tetap untuk konfigurasi cloud, seperti:
     - Membatasi akses ke portal admin.
     - Mengaktifkan manajemen kata sandi dan enkripsi file.
     - Mengaktifkan deteksi ancaman untuk database.

4. **Kriptografi dalam Cloud:**

   - Digunakan untuk menjaga **integritas** dan **kerahasiaan data.**
   - **Proses utama:**
     - **Enkripsi:** Mengubah data menjadi ciphertext yang hanya dapat dibaca dengan kunci enkripsi.
     - **Keamanan Kunci:** Menjaga kerahasiaan kunci enkripsi adalah kunci utama.

5. **Penghapusan Kriptografis (Cryptographic Erasure):**
   - Metode menghancurkan kunci enkripsi untuk membuat data tidak dapat diakses.
   - Teknik seperti **crypto-shredding** digunakan untuk memastikan data terenkripsi tidak dapat didekripsi lagi.

## Manajemen Kunci (Key Management)

Langkah-langkah untuk menjaga keamanan kunci enkripsi:

- **Trusted Platform Module (TPM):** Chip untuk menyimpan kata sandi, sertifikat, dan kunci enkripsi secara aman.
- **Cloud Hardware Security Module (CloudHSM):** Perangkat untuk menyimpan kunci secara aman dan menjalankan operasi kriptografi.

Organisasi bertanggung jawab atas kunci enkripsi mereka sendiri jika menggunakan kunci pribadi. Jika kunci ini hilang atau disusupi, CSP hanya memiliki keterbatasan dalam membantu. Namun, CSP biasanya menyediakan audit keamanan yang dapat ditinjau oleh pelanggan untuk menilai risiko.

## Poin Penting

- **Metode penguatan keamanan:** IAM, baseline konfigurasi, pengamanan hypervisor, kriptografi, dan penghapusan kriptografis adalah langkah penting.
- **Tanggung jawab bersama:** CSP menangani infrastruktur kriptografi, tetapi pelanggan bertanggung jawab atas kunci enkripsi pribadi mereka.
- Keamanan cloud membutuhkan kolaborasi antara organisasi dan CSP untuk memastikan perlindungan data.
