---
id: Examine signatures with Suricata
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Menggunakan Suricata untuk Menganalisis Signature IDS

### Pendahuluan
- **Suricata** adalah **IDS** sumber terbuka yang menggunakan pendekatan berbasis signature untuk mendeteksi ancaman.
- Anda dapat menggunakan **signature** yang telah disediakan atau menulis dan menambahkan signature kustom di Suricata.

---

### 1. **Navigasi ke Direktori Suricata**
- Pada mesin Linux Ubuntu yang sudah terinstal Suricata, navigasikan ke direktori **/etc/suricata** untuk menemukan file konfigurasi.
- Gunakan perintah `ls` untuk melihat daftar file, fokus pada folder **rules**, tempat penyimpanan signature yang sudah ditulis.

---

### 2. **Mengeksplorasi File custom.rules**
- File **custom.rules** berisi template aturan kustom untuk berbagai protokol dan layanan.
- Gunakan perintah `less` untuk membuka file dan melihat isinya. Dengan `less`, Anda dapat menggulir file satu halaman pada satu waktu, memudahkan navigasi.

---

### 3. **Struktur Signature**
- Setiap signature terdiri dari tiga komponen utama:
  - **Action**: Tindakan yang diambil jika kondisi signature terpenuhi. Pada contoh ini, action-nya adalah `alert`, yang berarti akan ada peringatan jika aturan cocok.
  - **Header**: Mendefinisikan detail lalu lintas jaringan yang dianalisis, seperti protokol, alamat IP sumber dan tujuan, serta port.
  - **Rule Options**: Menambahkan parameter untuk memodifikasi cara signature bekerja, seperti mencocokkan konten paket atau arah lalu lintas.

#### Contoh Signature:
```
alert http HOME_NET any -> EXTERNAL_NET any (msg:"GET on wire"; flow: established; content:"GET";)
```
- **Action**: `alert` – Menghasilkan peringatan jika kondisi sesuai.
- **Header**:
  - Protokol: `http`
  - Sumber: `HOME_NET` (jaringan internal), port: `any`
  - Tujuan: `EXTERNAL_NET` (jaringan eksternal), port: `any`
- **Rule Options**:
  - **msg**: Menampilkan pesan "GET on wire" saat alert.
  - **flow**: `established` – Menandakan bahwa koneksi sudah berhasil.
  - **content**: Mencari teks "GET", yang merupakan permintaan HTTP untuk mengambil data dari server.

---

### 4. **Penyesuaian dan Pengujian Signature**
- Setiap lingkungan memiliki kebutuhan yang berbeda. Oleh karena itu, signature harus **dapat disesuaikan dan diuji** untuk memastikan deteksi ancaman yang tepat dan meminimalkan **false positives**.
- Sebagai **security analyst**, Anda mungkin perlu mengubah atau membuat signature untuk meningkatkan deteksi dan menyesuaikan dengan kebutuhan jaringan Anda.

---

### Kesimpulan
- **Suricata** menyediakan cara yang efektif untuk menulis, menyesuaikan, dan menguji **signature-based detection**.
- Signature kustom memungkinkan deteksi yang lebih tepat dan lebih efisien terhadap ancaman yang spesifik untuk lingkungan jaringan Anda.
