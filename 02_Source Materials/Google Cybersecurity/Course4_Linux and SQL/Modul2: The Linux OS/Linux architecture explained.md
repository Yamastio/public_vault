---
id: Linux architecture explained
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## **Penjelasan Arsitektur Linux**

Memahami arsitektur Linux penting bagi seorang analis keamanan, karena pemahaman tentang bagaimana sistem diorganisasi memudahkan untuk memahami cara kerjanya. Berikut adalah komponen-komponen utama dalam arsitektur Linux:

### **1. User (Pengguna)**

- **Definisi**: Pengguna adalah individu yang berinteraksi dengan komputer dan memulai tugas.
- **Ciri Utama**:
  - Linux adalah sistem **multi-user**, memungkinkan beberapa pengguna mengakses sumber daya secara bersamaan.

### **2. Applications (Aplikasi)**

- **Definisi**: Program yang melakukan tugas tertentu, seperti kalkulator atau kalender.
- **Fitur Utama**:
  - Aplikasi bisa berupa bawaan sistem atau diinstal melalui **package manager**.
  - **Package Manager**: Alat untuk menginstal, mengelola, dan menghapus aplikasi.
  - **Package**: Potongan perangkat lunak yang bisa digabungkan untuk membentuk aplikasi lengkap.

### **3. Shell**

- **Definisi**: Interpreter baris perintah (CLI) yang menerjemahkan perintah pengguna untuk dikirim ke kernel.
- **Fungsi**:
  - Berperan sebagai "penerjemah" antara pengguna dan komputer.
  - Input dan output berbasis teks.

### **4. Filesystem Hierarchy Standard (FHS)**

- **Definisi**: Komponen yang mengorganisasi data dalam sistem Linux.
- **Fitur Utama**:
  - Data disusun dalam direktori (folder), yang dapat berisi file atau sub-direktori.
  - FHS menentukan lokasi penyimpanan data untuk memudahkan pengaksesan.

### **5. Kernel**

- **Definisi**: Inti dari OS Linux yang mengelola proses dan memori.
- **Fungsi Utama**:
  - Berkomunikasi dengan aplikasi untuk menjalankan perintah.
  - Mengalokasikan sumber daya sistem secara efisien.
  - Mengontrol fungsi utama perangkat keras.

### **6. Hardware (Perangkat Keras)**

- **Definisi**: Komponen fisik komputer yang terdiri dari perangkat keras internal dan periferal.

#### **Perangkat Keras Periferal**

- **Contoh**: Monitor, printer, keyboard, mouse.
- **Ciri**: Bisa ditambahkan atau dihapus tanpa memengaruhi fungsi utama sistem.

#### **Perangkat Keras Internal**

- **Ciri Utama**: Dibutuhkan untuk menjalankan sistem.
- **Komponen Utama**:
  - **Motherboard**: Papan sirkuit utama tempat komponen terpasang.
  - **CPU**: Prosesor utama yang menjalankan instruksi program.
  - **RAM**: Penyimpanan sementara untuk data saat program berjalan.
  - **Hard Drive**: Penyimpanan jangka panjang untuk data dan program.

### **Key Takeaways**

- Arsitektur Linux terdiri dari enam komponen utama: **User, Applications, Shell, Filesystem Hierarchy Standard (FHS), Kernel, dan Hardware**.
- Pemahaman tentang komponen-komponen ini membantu menganalisis fungsi dan keamanan sistem Linux dengan lebih efektif.
