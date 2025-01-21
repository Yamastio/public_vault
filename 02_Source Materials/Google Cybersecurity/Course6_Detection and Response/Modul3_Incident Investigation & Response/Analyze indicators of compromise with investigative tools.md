---
id: Analyze indicators of compromise with investigative tools
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Rangkuman: Investigasi dan Alat untuk Menganalisis IoCs**

### **Menambahkan Konteks pada Investigasi**
- **IoC (Indicators of Compromise)**: Bukti yang menunjukkan kemungkinan insiden keamanan. Penting untuk menambahkan konteks agar dapat melihat gambaran yang lebih besar dan memahami serangan secara menyeluruh.
- **Threat Intelligence**: Informasi berbasis bukti yang memberikan konteks tentang ancaman. Contohnya:
  - Menemukan artefak terkait, seperti komunikasi jaringan mencurigakan atau proses yang tidak biasa.
  - Membantu tim keamanan mendeteksi insiden lebih cepat dan membuat respons yang lebih tepat.

### **Crowdsourcing dalam Deteksi Ancaman**
- **Crowdsourcing**: Melibatkan komunitas global untuk berbagi data intelijen ancaman guna meningkatkan deteksi ancaman.
  - Organisasi kini dapat memanfaatkan pengalaman global, bukan bekerja secara isolasi.
  - Contoh: **ISACs (Information Sharing and Analysis Centers)** mengumpulkan intelijen untuk sektor tertentu, seperti energi atau kesehatan.

### **Contoh Tools untuk Investigasi IoCs**
1. **VirusTotal**:
![virustotal](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/OGF9XULpS4yRE9XWp0_5Ww_28f373819aa5487080f345ee10ed36e1_2UzPkWUVrcbKDLApq0CPB33OaJOORTO260rs4umcRJK6f09s9wrvwlEyczfwmAjHJp34gLdnvhGcz3WYmdSFzV5BRUscBCjBtePStKAA3S_481ILEM_X1AmmoLNi97lkerAtOcFrOuP2K5PT-QGGJ3Q?expiry=1736294400000&hmac=L7MqvZFbujwVvvvnI-Als99iA7QcWG5O3OWpRC-Rvas)
   - Menganalisis file, domain, URL, dan IP untuk mendeteksi ancaman seperti malware.
   - Tab utama:
     - **Detection**: Pandangan vendor tentang artefak (malicious, suspicious, dll).
     - **Details**: Informasi teknis, seperti hash, ukuran file, dan waktu pembuatan.
     - **Relations**: IoC yang terhubung, misalnya URL atau domain terkait.
     - **Behavior**: Perilaku artefak di lingkungan sandbox.
     - **Community**: Masukan dari komunitas VirusTotal.
   - **Catatan Penting**: Data yang diunggah akan dibagikan secara publik, jadi hindari mengunggah informasi pribadi.

2. **Alat Lainnya**:
   - **Jotti Malware Scan**: Layanan gratis untuk memindai file dengan beberapa antivirus.
   - **Urlscan.io**: Analisis URL secara mendalam.
   - **MalwareBazaar**: Repositori gratis untuk sampel malware, digunakan untuk riset ancaman.

### **Kesimpulan**
- Menambahkan konteks pada IoCs memperluas kemampuan deteksi dan memungkinkan pengambilan keputusan yang lebih efektif.
- Penggunaan crowdsourcing dan alat investigasi, seperti VirusTotal, meningkatkan respons terhadap ancaman keamanan.
