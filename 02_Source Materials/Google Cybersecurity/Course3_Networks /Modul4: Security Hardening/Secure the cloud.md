---
id: Secure the cloud
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan: Keamanan Cloud

### Apa itu Cloud Computing

- Cloud computing memungkinkan akses jaringan on-demand ke sumber daya komputasi yang dapat dikonfigurasi dan dirilis dengan usaha minimal.
- Seperti infrastruktur TI lainnya, infrastruktur cloud juga membutuhkan langkah-langkah keamanan.

### Pertimbangan Keamanan Cloud

1. **Identity Access Management (IAM):**

   - Mengelola identitas digital dan otorisasi penggunaan sumber daya cloud.
   - **Risiko:** Konfigurasi peran pengguna yang longgar dapat memberikan akses tidak sah ke operasi penting.

2. **Konfigurasi:**

   - Kompleksitas bertambah dengan banyaknya layanan cloud.
   - **Risiko:** Misconfigurations sering menjadi penyebab utama masalah keamanan cloud.

3. **Attack Surface:**

   - Setiap aplikasi atau layanan menambah risiko dan kerentanan.
   - **Solusi:** Desain jaringan yang benar dapat mengurangi titik masuk ke jaringan.

4. **Zero-Day Attacks:**

   - Eksploitasi kerentanan yang sebelumnya tidak diketahui.
   - CSP memiliki kemampuan untuk mendeteksi dan memperbaiki serangan ini lebih cepat dibandingkan organisasi TI tradisional.

5. **Visibilitas dan Pelacakan:**

   - Cloud menyediakan fitur seperti flow logs dan packet mirroring untuk memantau jaringan.
   - **Tantangan:** Organisasi tidak memiliki akses penuh ke server CSP tetapi bisa memanfaatkan audit pihak ketiga untuk menilai keamanan.

6. **Perubahan Cepat:**
   - CSP sering memperbarui teknologi, yang dapat memengaruhi konfigurasi keamanan pengguna.
   - Organisasi perlu menyesuaikan proses TI mereka agar sesuai dengan perubahan CSP.

### Model Tanggung Jawab Bersama (Shared Responsibility Model)

- **Tanggung Jawab CSP:**
  - Menjaga keamanan infrastruktur cloud, termasuk pusat data fisik, hypervisors, dan sistem operasi host.
- **Tanggung Jawab Organisasi:**
  - Menjaga keamanan aset dan proses yang disimpan atau dioperasikan dalam cloud.
  - Memastikan konfigurasi layanan sesuai dengan persyaratan keamanan organisasi.

### Poin Penting

- **Keamanan unik:** Organisasi perlu memahami tantangan keamanan unik yang ada di cloud.
- **Model tanggung jawab bersama:** Kedua belah pihak, CSP dan pengguna, memiliki peran masing-masing dalam menjaga keamanan cloud.
- Organisasi bertanggung jawab atas konfigurasi dan penerapan praktik keamanan terbaik pada layanan cloud mereka.
