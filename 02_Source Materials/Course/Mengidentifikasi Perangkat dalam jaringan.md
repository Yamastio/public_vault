---
id: Mengidentifikasi Perangkat dalam jaringan
aliases: []
tags:
  - tryhackme
---

## **Mengidentifikasi Perangkat dalam Jaringan**

Untuk menjaga komunikasi yang tertib dan terorganisir di jaringan, perangkat harus dapat **mengidentifikasi** dan **dikenali**. Jika tidak tahu siapa yang sedang diajak berkomunikasi, bagaimana kita bisa berbicara?

Perangkat dalam jaringan memiliki dua cara untuk diidentifikasi, mirip seperti manusia:

- **Nama** (seperti kita punya nama untuk dipanggil)
- **Sidik Jari** (yang unik dan tidak bisa diubah)

Begitu pula dengan perangkat, mereka memiliki dua cara untuk diidentifikasi:

1. **Alamat IP**
2. **Alamat MAC** (Media Access Control)

### **Alamat IP**

Alamat **IP** (Internet Protocol) digunakan untuk mengidentifikasi perangkat di jaringan untuk jangka waktu tertentu. Alamat IP dibagi menjadi empat oktet, dan setiap oktet menunjukkan bagian dari alamat IP perangkat dalam jaringan. Ini dihitung menggunakan teknik yang disebut **IP addressing & subnetting**.

Ada dua jenis alamat IP:

- **Alamat IP Publik**: Digunakan untuk mengidentifikasi perangkat di Internet.
- **Alamat IP Privat**: Digunakan untuk mengidentifikasi perangkat di jaringan lokal (misalnya di rumah atau kantor).

**Contoh** tabel untuk alamat IP:
| Nama Perangkat | Alamat IP | Jenis Alamat IP |
|------------------|---------------|-----------------|
| DESKTOP-KJE57FD | 192.168.1.77 | Privat |
| DESKTOP-KJE57FD | 86.157.52.21 | Publik |
| CMNatic-PC | 192.168.1.74 | Privat |
| CMNatic-PC | 86.157.52.21 | Publik |

Kedua perangkat di atas dapat berkomunikasi menggunakan alamat IP privat mereka, tetapi jika mereka mengirim data ke Internet, alamat IP publik yang akan digunakan.

**IPv4 vs IPv6**
Sistem alamat IP yang sudah lama digunakan adalah **IPv4**, yang memungkinkan 4.29 miliar alamat. Namun, karena semakin banyak perangkat yang terhubung ke Internet, kita membutuhkan lebih banyak alamat, dan itulah mengapa **IPv6** dibuat dengan kapasitas 340 triliun alamat!

### **Alamat MAC**

Setiap perangkat jaringan memiliki **interface fisik jaringan**, yaitu sebuah chip mikro yang diberikan **alamat MAC** unik saat diproduksi. Alamat MAC adalah **nomor heksadesimal 12 karakter**, yang terdiri dari dua bagian yang dipisahkan oleh titik dua (misalnya, `a4:c3:f0:85:ac:2d`).

- **Enam karakter pertama** menunjukkan perusahaan pembuat perangkat jaringan.
- **Enam karakter terakhir** adalah nomor unik untuk perangkat tersebut.

Namun, yang menarik adalah bahwa **alamat MAC dapat dipalsukan** melalui proses yang disebut **spoofing**. Ini terjadi ketika perangkat berpura-pura menggunakan alamat MAC perangkat lain. Misalnya, jika firewall mengizinkan komunikasi hanya dari alamat MAC administrator, seorang peretas bisa **menyamar** dengan menggunakan alamat MAC administrator, sehingga firewall menganggap komunikasi tersebut sah, padahal bukan.

### **Kontrol Alamat MAC di Wi-Fi Publik**

Banyak tempat seperti kafe atau hotel menggunakan kontrol alamat MAC untuk membatasi akses Wi-Fi, memberikan layanan berbeda, misalnya koneksi lebih cepat untuk pelanggan yang membayar. Dengan cara ini, jika seseorang mencoba untuk menggunakan layanan tanpa membayar, mereka bisa **mengubah alamat MAC-nya** agar jaringan mengira perangkat mereka sudah membayar.

### **Praktik Langsung**

Dalam laboratorium interaktif yang disediakan, kamu akan melihat bahwa router tidak mengizinkan **paket dari Bob** (ditandai biru) untuk menuju situs web TryHackMe karena Bob belum membayar. Tetapi **paket Alice** (hijau) berjalan lancar karena Alice telah membayar.

**Cobalah** mengubah alamat MAC Bob menjadi sama seperti milik Alice, dan lihat apa yang terjadi.

---

### **Kesimpulan**

- **Alamat IP** adalah cara untuk mengidentifikasi perangkat dalam jaringan, baik itu jaringan lokal atau jaringan global seperti Internet.
- **Alamat MAC** adalah identifikasi fisik perangkat yang lebih permanen, tetapi bisa dipalsukan.
- Menggunakan keduanya dengan benar adalah dasar komunikasi jaringan yang aman.
