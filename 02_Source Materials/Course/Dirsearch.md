Tags: [[hacking_tools]] [[hacking_intermediate]]

## Apa itu Dirsearch?
**Dirsearch** adalah alat pentest berbasis **Python** yang digunakan untuk **brute force** direktori atau file tersembunyi di sebuah aplikasi web. Dirsearch membantu mengidentifikasi direktori atau file yang tidak terdokumentasi, sehingga dapat digunakan untuk analisis lebih lanjut terhadap potensi kerentanan.

---

## Fitur Utama Dirsearch
1. **Pencarian Direktori dan File Tersembunyi**:
   - Mendeteksi file atau folder yang tidak terlihat pada tampilan publik.
2. **Filter Ekstensi File**:
   - Membatasi pencarian hanya pada jenis file tertentu (contoh: `.php`, `.zip`, `.sql`).
3. **Mendukung Berbagai Protokol**:
   - **HTTP**, **HTTPS**, dan penggunaan proxy.
4. **Custom Headers dan Authentication**:
   - Mendukung pengaturan **headers** dan autentikasi dasar (Basic Authentication).
5. **Parallel Scanning**:
   - Meningkatkan kecepatan pencarian dengan **multithreading**.

---

## Cara Instalasi Dirsearch
1. **Clone Repository Dirsearch**:
   - Buka terminal Anda, kemudian jalankan perintah berikut:
     ```bash
     git clone https://github.com/maurosoria/dirsearch.git
     cd dirsearch
     ```
2. **Install Requirements**:
   - Pastikan Anda sudah menginstal Python (minimal versi 3.6) dan `pip`.
   - Install semua dependensi menggunakan `pip`:
     ```bash
     pip install -r requirements.txt
     ```

3. **Periksa Instalasi**:
   - Jalankan Dirsearch untuk memastikan berhasil diinstal:
     ```bash
     python3 dirsearch.py --help
     ```
   - Ini akan menampilkan semua opsi yang tersedia dalam Dirsearch.

---

## Contoh Penggunaan
### 1. Perintah Dasar
- Target: `http://testphp.vulnweb.com/`
- Eksekusi Dirsearch:
  ```bash
  python3 dirsearch.py -u http://testphp.vulnweb.com/ -e php,sql,rar,zip
  ```
  **Penjelasan:**
  - `-u`: URL target yang akan discan.
  - `-e`: Filter ekstensi file yang akan dicari.

### 2. Output Kode Status
- **200**: Resource ditemukan (accessible).
- **404**: Tidak ditemukan.
- **403**: Forbidden (akses ditolak).
- **302**: Resource ditemukan tetapi dialihkan ke URL lain.

### 3. Custom Headers
- Jika perlu menambahkan header khusus, seperti **User-Agent**:
  ```bash
  python3 dirsearch.py -u http://example.com -H "User-Agent: CustomUserAgent"
  ```

### 4. Menggunakan Wordlist Khusus
- Dirsearch menggunakan wordlist untuk memindai direktori dan file.
- Anda dapat menggunakan wordlist bawaan Dirsearch atau wordlist kustom:
  ```bash
  python3 dirsearch.py -u http://example.com -w /path/to/wordlist.txt
  ```

### 5. Menggunakan Proxy
- Untuk mengarahkan traffic melalui proxy (misalnya proxy Burp Suite):
  ```bash
  python3 dirsearch.py -u http://example.com --proxy 127.0.0.1:8080
  ```

### 6. Threading untuk Performa Lebih Cepat
- Untuk mempercepat scanning:
  ```bash
  python3 dirsearch.py -u http://example.com -t 10
  ```
  **Penjelasan**:
  - `-t`: Jumlah thread yang digunakan (default: 10).

---

## Best Practices
1. **Gunakan Wordlist yang Relevan**:
   - Pilih wordlist sesuai dengan jenis target (misalnya aplikasi PHP, WordPress, dll.).
   - Contoh wordlist populer: `SecLists` (tersedia di GitHub).
2. **Hati-hati dengan Penggunaan**:
   - Jangan gunakan Dirsearch tanpa izin eksplisit dari pemilik server karena ini dapat melanggar hukum.
3. **Catat Hasil Scan**:
   - Simpan output ke file untuk analisis lebih lanjut:
     ```bash
     python3 dirsearch.py -u http://example.com -e php -o result.txt
     ```

---

## Kesimpulan
Dirsearch adalah alat yang efektif untuk mencari direktori dan file tersembunyi, sangat berguna dalam pengujian keamanan aplikasi web. Dengan kemampuan untuk menyesuaikan wordlist, filter ekstensi, dan proxy, Dirsearch menjadi salah satu alat penting dalam toolkit seorang pentester.
