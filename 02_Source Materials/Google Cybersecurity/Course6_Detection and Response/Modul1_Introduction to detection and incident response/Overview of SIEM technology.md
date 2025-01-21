---
id: Overview of SIEM technology
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan Mengenai Teknologi SIEM

### **Apa itu SIEM?**
SIEM (Security Information and Event Management) adalah alat yang mengumpulkan dan menganalisis data log untuk memantau aktivitas penting dalam sebuah organisasi. SIEM membantu analis keamanan melakukan analisis log, yang merupakan proses memeriksa log untuk mengidentifikasi peristiwa yang relevan.

### **Keuntungan SIEM**
SIEM menawarkan berbagai keuntungan yang penting dalam deteksi dan respons insiden:

1. **Akses ke Data Event**
   SIEM memberikan akses ke data aktivitas yang terjadi di jaringan secara real-time. SIEM dapat mengakses data dari berbagai sistem dan perangkat di jaringan yang besar.

2. **Pemantauan, Deteksi, dan Pemberitahuan**
   SIEM memantau sistem dan jaringan secara terus-menerus. Data yang terkumpul dianalisis menggunakan aturan deteksi untuk mendeteksi aktivitas berbahaya. Jika suatu aktivitas sesuai dengan aturan, pemberitahuan akan dikirim untuk ditindaklanjuti.

3. **Penyimpanan Log**
   SIEM berfungsi sebagai sistem penyimpanan data yang memungkinkan akses ke data historis. Data dapat disimpan atau dihapus sesuai dengan kebijakan organisasi.

### **Proses SIEM**
Proses SIEM terdiri dari tiga langkah kritikal:

1. **Mengumpulkan dan Mengagregasi Data**

![Agegate](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/S4RVzsQNTH62x3KYJ85Uxg_95172ee75d1c4665927dcb44cc168ff1_S35G010.png?expiry=1736121600000&hmac=Ft8YKkVsMObTT0-xxyFl1N8Mbjre-mxU6s5C32Gba0s)

   SIEM mengumpulkan data event dari berbagai sumber (firewall, server, router, dll.) dan mengagregasikannya di satu lokasi. Data tersebut berupa log yang mencatat peristiwa di dalam sistem organisasi.

2. **Normalisasi Data**

![normalize](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sO_SKjBLQ624WVuvgg9p_w_22b55ac3196c4b508dd1df3572065ff1_S35G009.png?expiry=1736121600000&hmac=SNwdpKyn6PGxovo7U3gANajwBTtwsw7WOWMOWbe-VZs)

   Setelah dikumpulkan, data dari berbagai sumber yang berbeda perlu dinormalisasi ke dalam format yang seragam untuk mempermudah pemrosesan. Normalisasi ini memastikan data dapat diproses dengan mudah oleh SIEM.

3. **Analisis Data**
   Setelah data dikumpulkan, diatur, dan dinormalisasi, SIEM akan menganalisis data menggunakan logika deteksi. Proses ini melibatkan penerapan aturan untuk mendeteksi aktivitas yang sesuai dan mengirimkan alert jika ditemukan potensi ancaman.

#### **Proses Parsing Data**
Parsing adalah langkah yang terjadi selama pengumpulan data. Parsing mencocokkan data ke dalam kolom-kolom tertentu agar lebih mudah dipahami. Misalnya, log berikut:

```
April 3 11:01:21 server sshd[1088]: Failed password for user nuhara from 218.124.14.105 port 5023
```

Akan diparsing menjadi:

```
host = server
process = sshd
source_user = nuhara
source_ip = 218.124.14.105
source_port = 5023
```

### **Alat SIEM Populer**
Berikut adalah beberapa alat SIEM yang umum digunakan dalam industri keamanan siber:

- **AlienVault® OSSIM™**
- **Chronicle**
- **Elastic**
- **Exabeam**
- **IBM QRadar® Security Intelligence Platform**
- **LogRhythm**
- **Splunk**

### **Poin Penting**
- SIEM mengumpulkan dan mengorganisir data dalam jumlah besar untuk memberikan wawasan yang berarti bagi tim keamanan.
- Dengan memahami cara kerja SIEM, proses yang terlibat, dan bagaimana organisasi memanfaatkannya, Anda dapat membantu dalam mendeteksi dan merespons insiden keamanan secara efektif.
- Pengetahuan ini membantu dalam menganalisis data log, mengidentifikasi ancaman, dan mendukung kegiatan respons insiden untuk meningkatkan posisi keamanan dan melindungi aset organisasi.
