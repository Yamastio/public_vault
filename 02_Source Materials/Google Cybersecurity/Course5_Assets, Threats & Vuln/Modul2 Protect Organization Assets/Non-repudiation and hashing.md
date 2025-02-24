---
id: Non-repudiation and hashing
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

**Ringkasan: Mengenal Fungsi Hash dalam Keamanan Data**

### 1. **Apa Itu Fungsi Hash?**
- Fungsi hash adalah algoritma yang menghasilkan **kode unik (hash value)** yang **tidak dapat didekripsi**.
- Berbeda dengan algoritma simetris dan asimetris, fungsi hash adalah proses satu arah yang tidak menghasilkan kunci untuk dekripsi.

### 2. **Manfaat Fungsi Hash**
- Memastikan **integritas data**, yaitu memastikan data tetap akurat dan konsisten.
- Mendukung **non-repudiation**, yaitu memastikan keaslian informasi tidak dapat disangkal.

### 3. **Contoh Penerapan**
- **Validasi aplikasi atau file:**
  - Sebuah program internal perusahaan dihitung hash-nya menggunakan algoritma seperti **MD5** atau **SHA-256**.
  - Jika program diubah oleh penyerang (misalnya disisipkan kode berbahaya), hash value akan berubah, sehingga mudah dikenali.

### 4. **Penggunaan Praktis**
- **Linux Command Line:**
  - Contoh hashing file `newfile.txt` dengan algoritma **SHA-256**:
    ```bash
    sha256sum newfile.txt
    ```
  - Output-nya adalah hash unik dari file tersebut.

- **VirusTotal:**
  - Alat populer untuk membandingkan hash file dengan database virus atau malware online.

### 5. **Keunggulan Fungsi Hash**
- **Perubahan sekecil apa pun pada input menghasilkan hash yang sepenuhnya berbeda.**
- Membantu komputer memvalidasi data dengan cepat melalui perbandingan hash input dan output.

### **Kesimpulan**
Fungsi hash adalah kontrol keamanan yang sangat penting untuk menjaga integritas data. Dengan hashing, keamanan file dan aplikasi dapat dijamin dengan lebih baik, dan serangan seperti modifikasi data dapat terdeteksi dengan mudah.
