---
id: OSI Model
aliases: []
tags: []
---

Tags: [[networking_fundamentals]]

## **Mengenal Model OSI: Cara Komputer Berkomunikasi dalam Jaringan**

Model OSI (Open Systems Interconnection) adalah sebuah **model standar** yang menjelaskan bagaimana komputer **berkomunikasi** dalam jaringan.

Model ini terdiri dari **7 lapisan** yang masing-masing punya tugasnya sendiri.

---

## **Kenapa Model OSI Penting?**

Bayangkan kamu ingin mengirim pesan ke teman lewat WhatsApp. Saat kamu mengetik pesan dan menekan **kirim**, ada banyak hal yang terjadi di balik layar sebelum pesan itu sampai ke HP temanmu.

Nah, model OSI membantu kita memahami **bagaimana data bergerak** dari satu perangkat ke perangkat lain!

---

## **7 Lapisan dalam Model OSI (Dari Atas ke Bawah)**

[ApPreSeTraNeDaPhy]

### **Layer 7 - Application (Aplikasi)**

Ini adalah bagian yang langsung **berhubungan dengan pengguna**. Contohnya adalah **WhatsApp, YouTube, atau browser** seperti Google Chrome.

> **Tugasnya:**
>
> - Memberikan antarmuka agar pengguna bisa mengirim dan menerima data (misalnya mengirim chat di WhatsApp atau membuka situs web).

### **Layer 6 - Presentation (Presentasi)**

Di sini, data dikonversi supaya bisa **dipahami oleh komputer lain**. Jika data dikirim dalam bentuk terenkripsi (seperti pesan di WhatsApp), lapisan ini juga yang akan **mengenkripsi dan mendekripsi** data tersebut.

> **Tugasnya:**
>
> - Mengubah data ke format yang bisa dipahami oleh komputer lain.
> - Mengenkripsi atau mengompresi data supaya lebih aman dan ringan.

### **Layer 5 - Session (Sesi)**

Lapisan ini bertanggung jawab untuk **membuka dan mengelola koneksi** antara dua perangkat.

Misalnya, ketika kamu membuka **dua tab browser sekaligus**, lapisan ini memastikan agar datanya **tidak tertukar** antara tab yang satu dengan yang lain.

> **Tugasnya:**
>
> - Menjalin dan mengatur koneksi antara dua perangkat.
> - Memastikan komunikasi tetap stabil dan tidak tercampur dengan koneksi lain.

### **Layer 4 - Transport (Transportasi)**

Lapisan ini mengatur **bagaimana data dikirim**: apakah dengan cara **yang lebih aman dan akurat** (TCP) atau **lebih cepat tapi bisa ada yang hilang** (UDP).

> **Tugasnya:**
>
> - Memilih cara pengiriman data:
>   - **TCP (Aman & Akurat)** → Cocok untuk mengirim file, email, atau membuka website.
>   - **UDP (Cepat, tapi bisa ada data hilang)** → Cocok untuk video call, streaming, atau game online.
> - Membagi data besar menjadi **potongan kecil** agar lebih mudah dikirim.

### **Layer 3 - Network (Jaringan)**

Di sinilah komputer menentukan **rute terbaik** agar data bisa sampai ke tujuannya. Lapisan ini **menggunakan IP Address** untuk menemukan lokasi tujuan.

Misalnya, kalau kamu mengunjungi **www.google.com**, lapisan ini akan mencari alamat IP-nya (contoh: **142.250.190.78**) dan menghubungkannya ke server Google.

- Logical Addresses

> **Tugasnya:**
>
> - Menentukan jalur terbaik untuk mengirim data ke tujuannya.
> - Menggunakan alamat IP untuk mengidentifikasi komputer yang dituju.

### **Layer 2 - Data Link (Tautan Data)**

Lapisan ini menggunakan **alamat fisik** (MAC Address) untuk memastikan bahwa data sampai ke perangkat yang benar.

Setiap komputer atau HP memiliki **MAC Address** unik, seperti **nomor plat kendaraan** yang membedakan satu dengan yang lain.

> **Tugasnya:**
>
> - Menambahkan **MAC Address** ke data sebelum dikirim.
> - Menyajikan data dalam format yang sesuai untuk dikirim
> - Mengecek apakah data yang diterima rusak atau tidak.

### **Layer 1 - Physical (Fisik)**

Ini adalah lapisan **paling dasar**, di mana data diubah menjadi **sinyal listrik, gelombang radio, atau cahaya** agar bisa dikirim melalui kabel atau WiFi.

> **Tugasnya:**
>
> - Mengubah data menjadi **sinyal listrik** (di kabel) atau **sinyal WiFi** (di udara).
> - Mengirimkan sinyal ke perangkat lain.

---

## **Kesimpulan**

🔥 **Model OSI menjelaskan bagaimana komputer mengirim dan menerima data melalui jaringan.**
🔥 **Setiap lapisan punya tugas sendiri, mulai dari aplikasi (WhatsApp/Chrome) hingga ke sinyal listrik/WiFi.**

Jadi, saat kamu **mengirim pesan WhatsApp** atau **menonton video YouTube**, sebenarnya ada **proses panjang** yang terjadi dalam 7 lapisan ini.
