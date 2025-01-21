---
id: 09-More About OWASP
aliases: []
tags: []
---

**Prinsip Keamanan OWASP untuk Analis Keamanan Pemula**

Sebagai analis keamanan, Anda akan terus menggunakan berbagai **framework keamanan**, **kontrol keamanan**, dan **prinsip keamanan** dalam pekerjaan sehari-hari untuk menjaga data tetap aman dan mengurangi risiko bagi organisasi. Berikut adalah **prinsip-prinsip OWASP** yang sudah dibahas sebelumnya serta prinsip tambahan yang perlu Anda ketahui:

---

### **Prinsip OWASP yang Sudah Dikenal**

1. **Minimize Attack Surface Area**

   - **Attack surface**: Semua potensi kerentanan yang dapat dimanfaatkan oleh pelaku ancaman.
   - **Tujuan**: Kurangi area yang bisa dieksploitasi, misalnya dengan menonaktifkan fitur perangkat lunak yang tidak digunakan atau membatasi akses pengguna.

2. **Principle of Least Privilege**

   - Pengguna hanya diberikan akses minimum yang diperlukan untuk menyelesaikan tugas mereka.
   - **Manfaat**: Membatasi dampak jika kredensial pengguna disusupi.

3. **Defense in Depth**

   - Gunakan berbagai **kontrol keamanan** seperti **firewall**, **MFA**, atau pengaturan izin, sehingga pelaku ancaman harus melewati banyak lapisan pertahanan untuk berhasil menyerang.

4. **Separation of Duties**

   - **Tujuan**: Mencegah individu memiliki akses yang cukup untuk melakukan aktivitas ilegal atau curang.
   - Misalnya, orang yang memproses gaji tidak boleh menjadi orang yang menandatangani cek gaji.

5. **Keep Security Simple**

   - Hindari solusi keamanan yang terlalu rumit agar lebih mudah dikelola dan efektif.

6. **Fix Security Issues Correctly**
   - Perbaiki kerentanan secara menyeluruh, uji hasil perbaikan, dan pastikan kerentanan tidak muncul kembali.

---

### **Prinsip Tambahan OWASP**

#### **1. Establish Secure Defaults**

- Aplikasi harus dalam kondisi keamanan optimal secara **default**.
- Contoh: Pengaturan default harus aman sehingga pengguna harus mengambil langkah ekstra untuk membuat aplikasi menjadi tidak aman.

#### **2. Fail Securely**

- Ketika kontrol keamanan gagal, aplikasi atau sistem harus kembali ke kondisi yang paling aman.
- Contoh: Jika **firewall** gagal, koneksi seharusnya ditutup secara otomatis, bukan malah menerima semua lalu lintas.

#### **3. Don’t Trust Services**

- Jangan menganggap sistem pihak ketiga sudah aman, meskipun itu adalah mitra organisasi.
- Contoh: Jika vendor pihak ketiga menangani poin reward pelanggan maskapai, maskapai harus memverifikasi keakuratan saldo sebelum membagikannya ke pelanggan.

#### **4. Avoid Security by Obscurity**

- Keamanan tidak boleh hanya bergantung pada menjaga detail sistem tetap tersembunyi.
- **Contoh dari OWASP (2016)**:
  - Jangan mengandalkan kerahasiaan kode sumber untuk melindungi aplikasi.
  - Terapkan kebijakan kata sandi yang masuk akal, **defense in depth**, batasan transaksi bisnis, arsitektur jaringan yang kokoh, serta kontrol penipuan dan audit.

---

### **Kesimpulan Utama**

Sebagai analis keamanan pemula, Anda akan sering menerapkan prinsip-prinsip OWASP ini untuk membantu organisasi:

- **Mengurangi risiko keamanan**.
- **Mempromosikan praktik pengembangan yang aman**.
- **Melindungi data, aset, dan orang-orang yang dilayani organisasi**.

Memahami prinsip seperti **establish secure defaults** dan **fail securely** akan membantu Anda memastikan bahwa aplikasi dan sistem organisasi tetap aman bahkan dalam kondisi yang tidak terduga.
