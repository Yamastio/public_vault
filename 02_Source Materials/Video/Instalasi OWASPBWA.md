Tags: [[hacking_labs]]

## Mengapa Harus Menggunakan OWASPBWA?
Latihan langsung pada aplikasi web nyata tanpa izin adalah **tidak legal**. Untuk menghindari pelanggaran hukum, kita dapat menggunakan **OWASPBWA**.  
**OWASPBWA** adalah proyek yang menyediakan aplikasi web yang sengaja dibuat memiliki celah keamanan, sehingga aman untuk belajar dan menguji keterampilan ethical hacking.  

---

## Langkah Instalasi dan Konfigurasi

### 1. Download dan Ekstrak
1. **Cari dan unduh OWASPBWA:**  
   - Kunjungi: [OWASP Broken Web Applications Project](https://sourceforge.net/projects/owaspbwa/).  
   - Klik **Download** dan tunggu hingga selesai.  
2. **Ekstrak file ZIP:**  
   - Setelah selesai, ekstrak file ZIP menggunakan software seperti WinRAR atau 7-Zip.  
   - Cari file dengan nama **`OWASP Broken Web Apps-cl1.vmdk`** (berukuran 2 KB).  

---

### 2. Instalasi di VirtualBox 

1. **Buka VirtualBox dan Buat Mesin Virtual Baru**:  
   - Klik **New**, kemudian isi:  
     - **Name:** *OWASPBWA1* (atau nama lain sesuai keinginan).  
     - **Type:** *Linux*.  
     - **Version:** *Other Linux (64-bit)* atau *32-bit* sesuai sistem.  
     - Klik **Next**.  

2. **Atur Memori (RAM):**  
   - Pilih kapasitas RAM minimum **512 MB** (atau lebih tinggi jika memungkinkan).  
   - Klik **Next**.  

3. **Gunakan File VMDK yang Sudah Diunduh:**  
   - Pilih opsi **Use an existing virtual hard disk file**.  
   - Klik folder icon, lalu klik **Add** untuk mencari file **`OWASP Broken Web Apps-cl1.vmdk`** yang telah diekstrak sebelumnya.  
   - Pilih file tersebut, lalu klik **Choose**.  

4. **Buat Mesin Virtual:**  
   - Klik **Create** untuk menyelesaikan pembuatan mesin virtual.  

---

### 3. Konfigurasi Jaringan  

1. **Ubah Mode Jaringan ke Bridge Adapter:**  
   - Klik kanan pada mesin virtual **OWASPBWA1** di VirtualBox, lalu pilih **Settings**.  
   - Buka tab **Network**.  
   - Ubah mode jaringan menjadi **Bridge Adapter** agar mesin virtual dapat terhubung langsung ke jaringan lokal.  
   - Klik **OK** untuk menyimpan perubahan.  

---

### 4. Jalankan Mesin Virtual 

1. **Mulai Mesin Virtual:**  
   - Klik mesin **OWASPBWA1**, lalu klik **Start** untuk menjalankannya.  
   - Tunggu hingga proses boot selesai (proses ini mungkin memakan waktu).  

2. **Login ke Sistem:**  
   - Saat diminta login, gunakan:  
     - **Username:** `root`  
     - **Password:** `owaspbwa`  

3. **Periksa Alamat IP:**  
   - Jalankan perintah berikut di terminal mesin virtual untuk mengetahui alamat IP:  
     ```bash
     ifconfig
     ```  
   - Catat alamat IP (biasanya terlihat di bagian **eth0**).  

---

### 5. Akses Aplikasi Web  

1. **Buka Browser di Mesin Host:**  
   - Masukkan alamat IP yang diperoleh dari langkah sebelumnya ke browser Anda (contoh: `http://192.168.1.100`).  
   - Anda akan melihat antarmuka OWASPBWA dengan berbagai aplikasi web rentan yang siap digunakan.  

2. **Mulai Eksperimen:**  
   - Pilih aplikasi web yang ingin diuji, misalnya DVWA, WebGoat, atau Mutillidae.  
   - Uji berbagai teknik pengujian penetrasi, seperti SQL Injection, XSS, atau CSRF, dalam lingkungan yang aman.  

---

## Tips Penting

1. **Gunakan Mode Snapshot di VirtualBox:**  
   - Sebelum mulai eksperimen, buat snapshot mesin virtual agar dapat kembali ke kondisi awal jika terjadi kesalahan.  
   - Pilih mesin virtual, klik **Snapshots** → **Take Snapshot**.  

2. **Jaga Keamanan Jaringan:**  
   - Mesin virtual ini hanya digunakan untuk latihan. Jangan biarkan aplikasi ini terhubung ke internet secara langsung tanpa firewall.  

3. **Pelajari Dokumentasi Aplikasi:**  
   - Setiap aplikasi di OWASPBWA memiliki dokumentasi atau tutorial sendiri. Manfaatkan untuk memahami cara kerja dan celah keamanan yang ada.  
