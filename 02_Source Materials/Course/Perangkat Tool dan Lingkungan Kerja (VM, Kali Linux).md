Tags: [[hacking_fundamentals]]

### **1. Hardware**

- **Komputer**:
    - **Spesifikasi**: Prosesor quad-core atau lebih tinggi, minimal 8GB RAM, dan SSD untuk performa optimal.
    - **Sistem Operasi**: Kebanyakan ethical hacker menggunakan distribusi Linux seperti **Kali Linux**, **Parrot OS**, atau **BlackArch Linux**.
- **Jaringan**:
    - **Koneksi Internet**: Stabil untuk mengakses sumber daya online seperti database eksploitasi, forum diskusi, dan layanan cloud.

### **2. Software**

- **Distribusi Linux Khusus Hacking**:
    - **Kali Linux**: Distribusi paling populer, dilengkapi ratusan tool untuk pengujian penetrasi.
    - **Parrot OS**: Fokus pada keamanan dan privasi.
    - **BlackArch Linux**: Distribusi yang sangat dapat disesuaikan dengan banyak pilihan tool.
- **Virtual Machine (VM)**:
    - **VirtualBox, VMware**: Digunakan untuk menciptakan lingkungan virtual yang terisolasi agar bisa menguji eksploitasi tanpa merusak sistem utama.
    - **Manfaat**:
        - **Pengujian eksploitasi**: Menjalankan sistem operasi yang rentan untuk uji eksploitasi.
        - **Isolasi lingkungan**: Menghindari kontaminasi sistem utama.
        - **Pembuatan snapshot**: Memungkinkan pengembalian sistem ke kondisi sebelumnya dengan mudah.
- **Tool Ethical Hacking**:
    - **Nmap**: Untuk pemindaian port dan deteksi layanan.
    - **Metasploit**: Kerangka kerja populer untuk mengeksploitasi kerentanan.
    - **Burp Suite**: Proxy web untuk hacking aplikasi web.
    - **Wireshark**: Menganalisis lalu lintas jaringan.
    - **Aircrack-ng**: Untuk cracking Wi-Fi.
    - **John the Ripper**: Untuk cracking password.
    - **Hydra**: Untuk serangan brute force.
    - **SQLmap**: Untuk injeksi SQL.

### **3. Work Environment**

- **Virtual Lab**:
    - **Platform**: **Hack The Box**, **TryHackMe**, **Vulnhub** menyediakan lingkungan virtual untuk praktik ethical hacking.
    - **Manfaat**:
        - **Pembelajaran langsung**: Tantangan realistis untuk mengasah keterampilan.
        - **Eksplorasi kerentanan**: Berbagai mesin virtual dengan kerentanan berbeda.
- **Physical Lab**:
    - **Membangun lab sendiri**: Membuat lab fisik dengan beberapa komputer yang terhubung untuk mensimulasikan jaringan yang kompleks.
    - **Manfaat**:
        - **Pengalaman lebih realistis**: Lingkungan yang lebih mirip dunia nyata.
        - **Eksperimen bebas**: Melakukan eksperimen yang lebih kompleks.

### **4. Contoh Praktik**

- **Skenario**: Ingin menguji kerentanan aplikasi web.
- **Langkah**:
    - **Buat VM**: Buat VM dengan sistem operasi yang sama dengan aplikasi target.
    - **Install aplikasi web**: Pasang aplikasi pada VM.
    - **Jalankan Burp Suite**: Konfigurasikan sebagai proxy untuk mencegat lalu lintas antara browser dan aplikasi.
    - **Temukan kerentanan**: Gunakan Burp Suite untuk mendeteksi kerentanan seperti SQL injection, XSS, atau CSRF.
    - **Eksploitasi**: Jika ditemukan kerentanan, gunakan Metasploit atau tool lainnya untuk mengeksploitasinya.

### **Kesimpulan**

Dengan perangkat keras, perangkat lunak, dan lingkungan kerja yang tepat, Anda dapat memulai perjalanan sebagai seorang ethical hacker. Ingatlah bahwa ethical hacking bertujuan untuk pembelajaran dan perbaikan, bukan penghancuran. Gunakan pengetahuan dan tool Anda dengan bijak dan bertanggung jawab.