Tags: [[hacking_fundamentals]] [[blue_team]]
## Element of Information Security

1. **Confidentiality**  
    Memastikan informasi tertentu hanya dapat diakses oleh orang yang memiliki kepentingan. Contoh: penggunaan enkripsi untuk data sensitif.
    
2. **Integrity**  
    Memastikan data tetap konsisten, dapat dipercaya, dan tidak diubah tanpa izin. Contoh: penggunaan checksum untuk mendeteksi perubahan data.
    
3. **Availability**  
    Memastikan data atau layanan selalu dapat diakses ketika dibutuhkan. Contoh: mitigasi serangan DDoS untuk menjaga layanan tetap aktif.
    
4. **Authenticity**  
    Memastikan keaslian data dan identitas pengirim/penerima. Contoh: penggunaan tanda tangan digital.
    
5. **Non-repudiation**  
    Memberikan bukti bahwa pengirim atau penerima tidak dapat menyangkal telah melakukan transaksi atau komunikasi tertentu. Contoh: log sistem dan sertifikat digital.
    

---

## Motivasi Cyber Attack

`Attack = Motive (Goal) + Method + Vulnerability`

### Motif Dibalik Serangan

- Mengganggu kontinuitas bisnis (e.g., serangan ransomware pada perusahaan besar).
- Mencuri informasi dan memanipulasi data.
- Menyebarkan ketakutan melalui serangan psikologis.
- Menargetkan keuntungan finansial (e.g., pencurian kartu kredit).
- Propaganda untuk kepentingan agama atau politik.
- Spionase negara untuk tujuan intelijen.
- Melukai reputasi target.
- Balas dendam terhadap individu atau organisasi.
- Meminta tebusan (ransomware).

---

## Klasifikasi Serangan

1. **Passive Attack**  
    Serangan pasif bertujuan untuk memantau atau mengumpulkan informasi tanpa mengubah data.  
    Contoh:
    
    - **Sniffing**: Mendengarkan komunikasi data dalam jaringan.
    - **Eavesdropping**: Menguping percakapan tanpa sepengetahuan pihak yang terlibat.
2. **Active Attack**  
    Serangan aktif melibatkan perubahan data atau mengganggu operasi normal.  
    Contoh:
    
    - **DDoS**: Menyebabkan layanan tidak dapat diakses.
    - **Man-in-the-Middle (MITM)**: Memata-matai dan memanipulasi komunikasi antara dua pihak.
3. **Close-in Attack**  
    Serangan yang dilakukan secara fisik atau berada di dekat target.  
    Contoh:
    
    - **Social Engineering**: Memanipulasi korban untuk memberikan informasi.
    - **USB Attack**: Menggunakan perangkat keras untuk menyebarkan malware.
4. **Insider Attack**  
    Serangan yang dilakukan oleh orang dalam organisasi.  
    Contoh:
    
    - **Keylogger**: Memasang perangkat lunak untuk mencatat aktivitas keyboard.
5. **Distribution Attack**  
    Serangan melalui distribusi perangkat lunak atau file yang terinfeksi.  
    Contoh:
    
    - **Phishing Email**: Mengelabui pengguna untuk mengunduh malware.

---

## Information Warfare

**Information Warfare** adalah penggunaan informasi untuk mendapatkan keuntungan dari lawan.

### Jenis Information Warfare

1. **Defensive Information Warfare (Blue Team)**  
    Strategi untuk mencegah, mendeteksi, dan merespons serangan.
    
    - Contoh: Firewall, IDS/IPS, backup data.
2. **Offensive Information Warfare (Red Team)**  
    Strategi untuk menyerang sistem lawan.
    
    - Contoh: Serangan berbasis malware, eksploitasi web aplikasi.

### Taktik Defensive Warfare

- **Prevention**: Mencegah serangan sebelum terjadi.
- **Deterrence**: Memberikan ancaman kepada calon penyerang.
- **Alerts**: Memantau dan memberikan peringatan dini.
- **Emergency Preparedness**: Membuat rencana tanggap darurat.
- **Response**: Menangani serangan yang sedang berlangsung.

### Taktik Offensive Warfare

- Serangan aplikasi web.
- Serangan server.
- Malware attacks.
- MITM attacks.
- Eksploitasi sistem.

---

## Metodologi Hacking (CEH Hacking Methodology - CHM)

1. **Footprinting**  
    Mengumpulkan informasi tentang target.
    
    - Contoh: whois, dns enumeration.
2. **Scanning**  
    Mencari celah yang dapat dimanfaatkan.
    
    - Contoh: port scanning, vulnerability scanning.
3. **Enumeration**  
    Mengidentifikasi layanan atau sistem yang rentan.
    
    - Contoh: enumerasi user account.
4. **Vulnerability Analysis**  
    Menganalisis kerentanan untuk serangan lebih lanjut.
    

### System Hacking

1. **Gaining Access**  
    Mendapatkan akses awal ke sistem.
    
    - Teknik: password cracking, vulnerability exploitation.
2. **Privilege Escalation**  
    Meningkatkan hak akses ke level admin/root.
    
3. **Maintaining Access**  
    Memastikan akses tetap ada.
    
    - Teknik: backdoor, file hiding.
4. **Clearing Logs**  
    Menghapus jejak aktivitas untuk menghindari deteksi.
    

---

## Cyber Kill Chain Methodology
![[Pasted image 20241123211135.png]]
1. **Reconnaissance**  
    Pengumpulan informasi tentang target.
2. **Weaponization**  
    Menyiapkan senjata atau exploit.
3. **Delivery**  
    Mengirimkan exploit kepada target.
4. **Installation**  
    Menginstal malware pada sistem target.
5. **Command & Control (C2)**  
    Mengontrol perangkat yang sudah terinfeksi.
6. **Action on Objective**  
    Melakukan tindakan sesuai tujuan serangan.

---

## Mitre ATT&CK Framework

1. **MITRE ATT&CK**  
    Framework yang digunakan untuk menganalisis dan memahami pola serangan.
    
    - Digunakan untuk pengembangan pertahanan dan serangan.
2. **14 Taktik dalam Mitre ATT&CK**  
    Contoh:
    
    - Reconnaissance.
    - Initial Access.
    - Persistence.
    - Privilege Escalation.
    - Defense Evasion.
    - Execution.

---

## Hacker Classes

1. **Black Hats**: Hacker untuk tujuan jahat.
2. **White Hats**: Hacker etis untuk tujuan kebaikan.
3. **Gray Hats**: Gabungan antara black dan white hat.
4. **Suicide Hackers**: Tidak peduli konsekuensi hukum.
5. **Script Kiddies**: Hacker pemula menggunakan tools orang lain.
6. **Cyber Terrorists**: Melakukan serangan untuk terorisme.
7. **State-Sponsored Hackers**: Didanai oleh negara untuk spionase.
8. **Hacktivists**: Hacker dengan motivasi politik atau ideologi.
9. **Hacker Teams**: Kelompok hacker yang bekerja bersama.
10. **Industrial Spies**: Mata-mata industri untuk mencuri rahasia dagang.
11. **Insiders**: Serangan dari dalam organisasi.
12. **Criminal Syndicates**: Kelompok kriminal yang menggunakan hacking.
13. **Organized Hackers**: Hacker yang bekerja dengan tujuan spesifik seperti keuntungan finansial.

---

## Ethical Hacking

1. **Tujuan**  
    Mengidentifikasi celah keamanan dalam sistem dengan izin resmi.
2. **Proses**
    - Simulasi serangan.
    - Menganalisis hasil.
    - Membuat laporan.
3. **Prinsip**
    - Harus dengan izin.
    - Tidak boleh merusak data.