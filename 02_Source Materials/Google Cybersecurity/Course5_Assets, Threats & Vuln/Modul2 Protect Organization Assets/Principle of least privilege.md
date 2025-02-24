---
id: Principle of least privilege
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Rangkuman: Principle of Least Privilege (PoLP)**

### **Apa Itu Principle of Least Privilege (PoLP)?**
- PoLP membatasi akses pengguna hanya pada **level minimum yang diperlukan** untuk menyelesaikan tugas.
- Mendukung triad keamanan informasi: **Confidentiality, Integrity, dan Availability (CIA)**.
- Kontrol keamanan ini efektif untuk mengurangi risiko seperti pencurian data dan penyalahgunaan.

---

### **Manfaat Utama PoLP**
1. **Mengurangi Risiko:**
   - Membatasi akses ke informasi sensitif.
   - Mengurangi kemungkinan perubahan data yang tidak disengaja.
   - Mendukung pengawasan dan administrasi sistem.

2. **Mengurangi Peluang Serangan:**
   - Membatasi akses hanya untuk pengguna tertentu dengan batasan yang jelas.

---

### **Implementasi PoLP**
1. **Menentukan Akses dan Otorisasi:**
   - **Siapa pengguna?** Bisa berupa orang, perangkat, atau software.
   - **Seberapa besar akses yang dibutuhkan?**

2. **Jenis Akun Pengguna Umum:**
   - **Guest accounts**: Untuk pengguna eksternal seperti pelanggan atau mitra.
   - **User accounts**: Untuk karyawan berdasarkan tugas kerja.
   - **Service accounts**: Untuk aplikasi/software di jaringan.
   - **Privileged accounts**: Dengan izin atau akses administratif.

3. **Best Practices:**
   - Tetapkan baseline akses untuk setiap jenis akun.
   - Pantau dan revisi akses pengguna secara rutin.

---

### **Audit Privilege**
- Audit rutin memastikan sistem tetap aman. Ada tiga pendekatan utama:

1. **Usage Audit**:
   - Mengawasi sumber daya yang diakses pengguna dan tindakan mereka.
   - Mengidentifikasi akses yang tidak lagi diperlukan.

2. **Privilege Audit**:
   - Mengatasi **privilege creep**, yaitu akumulasi hak akses berlebih.
   - Memastikan hak akses selaras dengan peran pengguna.

3. **Account Change Audit**:
   - Meninjau perubahan akun untuk mendeteksi aktivitas mencurigakan.
   - Memastikan semua perubahan dilakukan oleh pengguna yang berwenang.

---

### **Tips Tambahan**
- **Kata sandi**: Pastikan kata sandi aman untuk menghindari kompromi sistem.
- **Pemantauan sistem**: Directory services dapat diatur untuk mengirim peringatan jika ada aktivitas mencurigakan.

---

### **Kesimpulan**
- PoLP adalah kontrol penting untuk mencegah akses tidak sah.
- Implementasi melibatkan konfigurasi akun dengan akses yang tepat dan audit rutin.
- Mengelola akses dengan PoLP membantu melindungi **kerahasiaan, integritas, dan ketersediaan** informasi.
