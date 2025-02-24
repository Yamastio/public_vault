---
id: 01_information_security_overview
aliases: []
tags: []
---

Tags: [[ceh_v12]]

## Deskripsi Keamanan Informasi

- Information Security merujuk pada proteksi informasi terkait sistem yang digunakan, disimpan dan dikirimkan dari akses yang tidak sah
- Informasi adalah aset yang penting dari suatu orgnisasi

## Elemen dari Keamanan Informasi(Information Security)

- `Confidentiality` (Kerahasiaan): Memastikan informasi hanya bisa diakses oleh pihak yang berwenang saja
- `Integrity` (Keutuhan): Mencegah dari perubahan informasi yang tidak sah
- `Availability` (Ketersediaan): Memastikan sistem dapat memanajemen informasi dengan baik sehingga bisa diakses ketika dibutuhkan oleh user yang sah
- `Authenticity` (Autentikasi): Mengkonfirmasi bahwa user itu asli, seperti penggunaan smart card, digital sertifikat, dll
- `Non-repudiation` (Nirsangkal): Membuktikan bahwa pengirim dan penerima informasi saling terlibat, memastikan semua pihak dapat dipercaya. Misalnya dengan tanda tangan digital.

## Motivasi, Tujuan, dan Sasaran dari Keamanan Informasi

> attack = motive(goal) + method + vulnerability

- Suatu serangan bisa terjadi apabila ada motif atau tujuan, ada metode(cara), dan ada kelemahan di suatu sistem
- Motivasi muncul karena ada sesuatu yang berharga tersimpan atau berjalan di suatu sistem
- Alat dan metode yang beragam digunakan untuk melakukan eksploitasi suatu kelemahan di sistem

### Motif dibalik suatu serangan

- Mengganggu kelangsungan bisnis
- Mencuri informasi
- Memanipulasi data
- Membuat keributan
- Membawa kerugian keuangan
- Propaganda keagamaan atau kepercayaan politik
- Kepentingan militer
- Menyerang reputasi target
- Balas dendam
- Meminta uang tebusan

## Klasifikasi Serangan

### Passive Attacks

- Tanpa merusak data, melainkan menangkap dan memonitori network trafic dan data flow
- Penyerang melakukan reconnaissance menggunakan sniffer
- Serangan susah dideteksi, karena tidak memiliki interaksi langsung dengan target
- Contoh:
  - Sniffing dan Eavesdropping
  - Footprinting
  - Network Traffic Analysis
  - Decryption of weakly encrypted traffic

### Active Attacks

- Merusak data saat dalam perjalanan atau mengganggu komunikasi atau layanan antar sistem, untuk membypass atau membobol sistem
- Penyerang melakukan serangan dengan mengirimkan traffic secara aktif yang bisa dideteksi
- Melakukan penetrasi untuk mendapatkan akses ke remote sistem untuk mengambil alih internal network
- Contoh:

  - DOS
  - Bypassing protection mechanism
  - Malware Attack
  - Modification of information
  - Spoofing
  - Replay Attack
  - Password based attack
  - Session hijacking
  - MITM
  - DNS dan ARP poisoning
  - Firewall dan IDS attack
  - Profiling
  - Arbitary code execution
  - Privilege escalation
  - Backdoor Access
  - Cryptographic attack
  - SQL injection
  - XSS
  - Directory traversal
  - Exploitation of app dan OS software

### Close in Attacks

- Dilakukan apabila penyerang sangat dekat dengan target sistem atau jaringan
- Tujuan utama penyerang: Mencuri informasi ataupun menganggu akses
- Contoh: Social Engineering(Eavesdropping, shoulder surfing, dumpster diving, dll)

### Insider Attacks

- Dilakukan oleh orang dalam, yang memilkki akses secara fisik ke asset kritis dari target
- Susah untuk mendeteksi insider attack, karena orang dalam sendiri yang melakukan
- Contoh:
  - Eavesdropping and wiretapping
  - Social engineering
  - Data Theft And Spoliation
  - Pod Slurping
  - Planting keyloggers, backdoors, malware, dll

### Distribution Attacks

- Penyerang merusak hardware atau software sebelum di instal, maupun saat dalam transit
- Contohnya backdoor yang dibuat oleh software atau hardware vendor ketika manufaktur dilakukan
- Modifikasi selama produksi
- Modifikasi selama pengiriman

## Information Warfare

Merujuk pada penggunanaan informasi dan komunikasi teknologi (ICT) untuk mendapatkan keuntungan kompetitif dari lawan, contohnya: virus, worm, trojan, logic bombs, electro jamming, dll

Martin Libiciki membagi menjadi beberapa kategori:

### Comand and Control warfare(C2 Warfare)

- Dampak yang dimiliki penyerang terhadap sistem atau jaringan yang disusupi yang mereka kendalikan

### Intelligence-based warfare

- Teknologi berbasis sensor yang secara langsung merusak sistem
- Terdiri dari perancangan, perlindungan, penolakan sistem untuk mendominasi pertempuran

### Electronic Warfare

- Menggunakan radio elektronik dan teknik kriptografi untuk mengganggu komunikasi
- Radio elekronik menyerang fisiknya, artinya pengiriman informasi, sedangkan kriptografi menggunakan bits dan byte untuk mengganggu pengiriman informasi

### Psychological Warfare

- Menggunakan beberapa teknik seperti propaganda dan teror untuk mengacaukan musuh

### Hacker Warfare

- Tujuanya seperti: mematikan sistem, mencuri informasi, data error, dll
- Secara umum menggunakan virus, logic bombs, trojan horse, dan sniffer untuk melakukan seragan ini

### Economic Warfare

- Mempengaruhi ekonomi dari suatu negara atau bisnis dengan memblokir arus informasi
- Merusak suatu organisasi yang melakukan banyak bisnis di dunia digital

### Cyberwarfare

- Penggunanaan informasi terhadap individu atau kelompok
- Termasuk informasi terosisme, semantic attacks, yang bisa mengambil alih sistem, juga simula-warfare(simulated war, contoh menyediakan senjata untuk demonstran)

---

Setiap Information Warfare yang disebutkan diatas, terdiri dari sisi penyerang dan bertahan:

- Defensif Information Warfare: semua strategi dan aksi untuk mempertahankan ICT(Information and Communication Technology)
- Offensif Information Warfare: serangan ke ICT aset dari musuh

![[ceh1.png]]
