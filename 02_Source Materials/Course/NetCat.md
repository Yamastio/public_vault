Tags: [[hacking_intermediate]] [[hacking_tools]]

## Apa itu Netcat?

Netcat adalah utilitas jaringan serbaguna yang sering disebut "pisau Swiss Army untuk jaringan." Fitur utamanya meliputi:

- **Koneksi TCP/UDP**: Menghubungkan ke port tertentu di host target.
- **Transfer data**: Mengirim atau menerima data melalui koneksi jaringan.
- **Port listening**: Mendengarkan koneksi masuk pada port tertentu.

### Contoh Penggunaan Netcat

- **Membuat koneksi ke port 22 (SSH)** pada host target:
    
    ```bash
    nc 192.168.1.1 22
    
    ```
    
- **Mendengarkan koneksi masuk pada port 80 (HTTP)**:
    
    ```bash
    nc -l 80
    
    ```
    
- **Mentransfer file ke host target**: Mengirimkan isi file `file.txt` ke host pada port 1234.
    
    ```bash
    cat file.txt | nc 192.168.1.1 1234
    
    ```
    

---