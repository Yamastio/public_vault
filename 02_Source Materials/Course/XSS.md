Tags: [[tipe_serangan]]

## Apa itu XSS (Cross-Site Scripting)?

**XSS (Cross-Site Scripting)** adalah jenis kerentanan keamanan pada aplikasi web di mana penyerang menyisipkan kode berbahaya (biasanya berupa script JavaScript) ke dalam halaman web yang kemudian dijalankan oleh browser korban. Tujuannya adalah untuk mencuri informasi sensitif, seperti cookies atau sesi pengguna, yang bisa digunakan untuk login secara tidak sah atau mengambil alih akun pengguna.

## Urutan Serangan XSS:

1. **Penyisipan Script**: Penyerang menyisipkan script berbahaya ke dalam situs web atau aplikasi yang memiliki kerentanannya.
2. **Pengaksesan oleh Korban**: Korban mengakses formulir atau halaman web yang telah disusupi script berbahaya.
3. **Pengambilan Data Sensitif**: Script yang disisipkan mengakses data sensitif, seperti cookies atau informasi sesi pengguna.
4. **Penyalahgunaan Data**: Penyerang kemudian dapat menggunakan data tersebut untuk login ke akun korban atau melakukan aksi lain yang merugikan.

## Jenis-Jenis XSS

1. **Reflected XSS**:
    - Penyerang menyisipkan kode berbahaya langsung di dalam URL.
    - Kode tersebut diteruskan ke server dan ditampilkan kembali pada halaman web.
    - Korban yang mengklik tautan berbahaya akan mengeksekusi kode berbahaya tersebut dalam browser mereka.
2. **Stored XSS**:
    - Penyerang menyisipkan kode berbahaya ke dalam situs web atau aplikasi dan kode tersebut disimpan di server.
    - Setiap kali korban mengunjungi halaman yang mengandung script berbahaya, kode tersebut akan dijalankan oleh browser korban.
    - Stored XSS lebih berbahaya karena dapat menyerang lebih banyak korban setiap kali halaman tersebut diakses.

---

## Demo XSS

Untuk mempelajari lebih lanjut tentang XSS, Anda bisa menggunakan **DVWA (Damn Vulnerable Web Application)**, aplikasi web yang dirancang untuk menguji dan mempraktikkan kerentanannya.

### Cara Instalasi DVWA dengan Docker:

1. **Install Docker** terlebih dahulu jika belum terpasang.
2. **Clone repository DVWA**:
    
    ```
    git clone https://github.com/digininja/DVWA.git
    ```
    
3. **Masuk ke folder DVWA**:
    
    ```
    cd DVWA
    ```
    
4. **Jalankan DVWA dengan Docker Compose**:
    
    ```
    docker compose up -d
    ```
    
5. **Akses DVWA** melalui browser di port yang disediakan (misalnya, `http://localhost`).
6. **Login** menggunakan username `admin` dan password `password`.
7. **Pastikan minimal setup check** sudah berhasil dan berwarna hijau, lalu klik **"Create"** atau **"Reset Database"**.
8. Setelah berhasil, Anda akan diarahkan ke halaman admin.

### Melakukan Tes XSS di DVWA:

1. **Atur Security Level** ke **Low** di menu **DVWA Security**.
    
2. **Reflected XSS**:
    
    - Masuk ke menu **XSS (Reflected)**.
    - Coba masukkan script berikut di form input:
        
        ```html
        <script>alert(1)</script>
        ```
        
    - Jika muncul **alert(1)** di browser Anda, maka aplikasi tersebut rentan terhadap Reflected XSS.
    - Penyerang bisa mengirimkan link yang berisi script tersebut, dan ketika korban mengkliknya, kode JavaScript akan dijalankan di browser korban.
3. **Stored XSS**:
    
    - Masuk ke menu **XSS (Stored)**.
    - Masukkan script berikut di form input:
        
        ```html
        <script>alert("sured")</script>
        ```
        
    - Script ini akan disimpan di database. Ketika pengguna lain mengunjungi halaman yang berisi data tersebut, script yang disimpan akan dieksekusi di browser mereka.
    - Stored XSS lebih berbahaya karena script dapat menargetkan banyak korban.

### Mengeksplorasi Kesalahan dan Menyempurnakan Keamanan:

- Anda bisa memeriksa **source code** dari tiap menu untuk memahami kesalahan yang menyebabkan kerentanannya.
- Setelah itu, Anda bisa mencoba meningkatkan tingkat keamanan aplikasi dengan mengubah pengaturan **DVWA Security**.

---

XSS adalah salah satu serangan yang paling sering terjadi pada aplikasi web. Memahami jenis dan cara kerja XSS dapat membantu Anda lebih waspada dan lebih siap dalam melindungi aplikasi Anda dari kerentanannya.