---
id: Netcat
aliases: []
tags: []
---

## Description

### What?

- Netcat adalah sebuah command di linux untuk melakukan koneksi jaringan baik TCP/UDP

```bash
netcat -l -p 12241 -e /bin/bash -v
listening on [any] 12241 ...


```

### Who?

- Digunakan oleh admin, devs untuk networking task

### When?

- Dibuat pada 1996, dan masih digunakan sampai saat ini

### Where?

- Tersedia di linux, dan UNIX

### Why?

- Untuk memfasilitasi koneksi jaringan, dan tugas keamanan

### How?

- CLI, supporting TCP/UDP

## Practice

1. Buka terminal
2. Cek netcat sudah terinstall belum `netcat -h`
3. Jika belum bisa install `sudo apt install netcat -y`

### Banner Grabbing (OSINT)

Banner grabbing adalah proses mengambil banner dari suatu website. Biasanya untuk keamanan, kita akan memberikan informasi seminimal mungkin sehingga ketika ada yang melakukan banner grabbing hanya sedikit informasi yang dapat diambil.

Cara melakukan:

1. Verifikasi ip dari kali, ubuntu, dan pfsense
2. `nc 172.16.1.1 443 -v` , -v untuk verbose
3. `HEAD / HTTP/1.0)`
4. `GET /HTTP/1.1. | nc 172.16.1.1 80`, bisa langsung pakai command ini
5. `ctrl + c`

```bash
└─$ nc 172.16.1.1 443 -v
pfSense.home.arpa [172.16.1.1] 443 (https) open
HEAD /HTTP/1.0)
<html>
<head><title>400 Bad Request</title></head>
<body>
<center><h1>400 Bad Request</h1></center>
<hr><center>nginx</center>
</body>
</html>
```

```bash
└─$ GET / HTTP/1.1. | nc 172.16.1.1 80
HTTP/1.1 400 Bad Request
Server: nginx
Date: Sat, 22 Feb 2025 01:04:02 GMT
Content-Type: text/html
Content-Length: 150
Connection: close

<html>
<head><title>400 Bad Request</title></head>
<body>
<center><h1>400 Bad Request</h1></center>
<hr><center>nginx</center>
</body>
</html>
```

### Chat server: (UBUNTU)

1. Verfikasi IP
2. konfigurasi ubuntu computer sebagai listener dengan command

   ```bash
   nc -l -p 55555 -w 60 -v
   ```

   - -l: listen
   - -p: port
   - -w: wait time
   - -v: verbose

### Chat client: (KALI)

1. Verifikasi IP Ubuntu
2. `nc 172.16.1.100 55555 -v`
3. `hello world`
4. `Hello World again!`
5. `ctrl + c`

### Transfer file (Dead Drop)

1. Di server bisa buat file dulu, `touch netcat.txt`
2. Isi file dengan `vim netcat.txt`, ketik `hello world!`
3. Di server, `nc -v -w 60 -l -p 12241 < netcat.txt`
4. Di client, `nc -v -w 2 172.16.1.103 12241 > netcat.txt`
5. Di client, `nc -v -w 2 172.16.1.103 12241 >> netcat.txt`, untuk append

### cek history command

1. Cek history command `history`
2. Pilih dengan tanda `!` misal `!123`

### Remote Code Execution (RCE)

1. `ifconfig`
2. `whoami`
3. `pwd`
4. `date`
5. `ifconfig eth0 && whoami && pwd && date`
6. Server: `nc -l -p 12241 -e /bin/bash -v`
7. Client: `nc 172.16.1.103 12241 -v`

### Port Scanning

`nc 172.16.1.103 1-13000 -v`

### Help

`man netcat`
`netcat -h`
