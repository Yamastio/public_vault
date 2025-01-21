Tags: [[hacking_fundamentals]]

## Digital Forensics and Incident Response (DFIR)

DFIR berfokus pada investigasi bukti serangan dan tanggapan terhadap insiden.

### Digital Forensics

Digital forensics adalah cabang forensik yang menyelidiki kejahatan yang melibatkan sistem digital, seperti:

1. **File System**: Menganalisis image digital untuk mempelajari program terinstal, file yang dibuat, atau file yang dihapus.
2. **System Memory**: Menyalin memori sistem untuk mempelajari malware yang hanya dijalankan di memori.
3. **System Logs**: Melacak aktivitas sistem melalui log meskipun penyerang mencoba menghapus jejak.
4. **Network Logs**: Menganalisis lalu lintas jaringan untuk memahami detail serangan.

### Incident Response

Respons terhadap insiden bertujuan untuk mengurangi kerusakan dan memulihkan sistem. Empat fase utamanya:

1. **Preparation**: Melatih tim dan memasang langkah pencegahan.
2. **Detection and Analysis**: Mendeteksi dan menganalisis insiden untuk menentukan tingkat keparahan.
3. **Containment, Eradication, and Recovery**: Menghentikan penyebaran, menghapus ancaman, dan memulihkan sistem.
4. **Post-Incident Activity**: Membuat laporan dan pembelajaran untuk mencegah insiden serupa.

### Malware Analysis

Malware adalah perangkat lunak berbahaya seperti:

- **Virus**: Menginfeksi program untuk menyebar, mengubah, atau merusak file.
- **Trojan Horse**: Menyamar sebagai program bermanfaat tetapi memiliki fungsi jahat.
- **Ransomware**: Mengenkripsi file pengguna dan meminta tebusan untuk kunci enkripsi.

**Metode analisis malware**:

1. **Static Analysis**: Menganalisis malware tanpa menjalankannya, biasanya membutuhkan pemahaman bahasa assembly.
2. **Dynamic Analysis**: Menjalankan malware dalam lingkungan terkendali untuk mempelajari perilakunya.