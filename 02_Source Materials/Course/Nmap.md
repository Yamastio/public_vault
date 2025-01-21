Tags: [[hacking_intermediate]] [[hacking_tools]]

## Nmap (Network Mapper)

### Deskripsi

Nmap adalah tool yang fleksibel dan kuat untuk memetakan jaringan dan melakukan auditing keamanan. Beberapa fungsi Nmap meliputi:

- **Mendeteksi host**: Menemukan perangkat yang aktif di jaringan.
- **Identifikasi layanan**: Menentukan jenis layanan yang aktif pada host tertentu (contoh: HTTP, FTP, SSH).
- **Fingerprinting sistem operasi**: Mencoba menebak sistem operasi yang digunakan pada host target.
- **Analisis topologi jaringan**: Memahami struktur dan hubungan antar perangkat di jaringan.

### Contoh Penggunaan Nmap

- **Scan dasar untuk IP tertentu**:
    
    ```bash
    nmap -v 192.168.1.1
    
    ```
    
    Menampilkan detail seperti status host dan layanan yang terbuka. Opsi `-v` meningkatkan tingkat detail output.
    
- **Scan seluruh subnet**:
    
    ```bash
    nmap -v 192.168.1.0/24
    
    ```
    
    Memindai semua perangkat dalam subnet tersebut.
    
- **Fingerprinting sistem operasi**:
    
    ```bash
    nmap -O 192.168.1.1
    
    ```
    
    Opsi `-O` digunakan untuk menebak sistem operasi yang digunakan oleh host.
    
- **Scan untuk menemukan layanan yang terbuka dan versinya**:
    
    ```bash
    nmap -sV 192.168.1.1
    
    ```
    
    Opsi `-sV` digunakan untuk menentukan versi layanan yang aktif.