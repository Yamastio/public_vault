---
id: ping
aliases: []
tags: []
---

tags: [[hacking_fundamentals]]

## Description

What: Untuk mengetes apakah jaringan dapat dijangkau atau tidak
Who: Network Admin dan User
When: Saat network perlu ditest
Where: Di semua perangkat yang terhubung atau jaringan
Why: Untuk diagnostik, troubleshooting, mengukur latensi, dan verifikasi dapat dijangkau tidak
How: Bekerja dengan mengirim ICMP Echo Request, lalu menunggu ICMP Echo Reply

## Praktik:

1. Open Terminal
2. Type `ping google.com`, atau `ping 8.8.8.8`
3. Klik Enter
4. `Ctrl + z` untuk menghentikan
5. `clear` untuk menghapus output
6. Untuk membatasi packet yang dikirim, gunakan `-c`

   ```bash
   ping -c 5 google.com
   ```

   Output:

   ```bash
   PING google.com (216.239.38.120) 56(84) bytes of data.
   64 bytes from any-in-2678.1e100.net (216.239.38.120): icmp_seq=1 ttl=115 time=32.1 ms
   64 bytes from any-in-2678.1e100.net (216.239.38.120): icmp_seq=2 ttl=115 time=32.7 ms
   64 bytes from any-in-2678.1e100.net (216.239.38.120): icmp_seq=3 ttl=115 time=29.8 ms
   64 bytes from any-in-2678.1e100.net (216.239.38.120): icmp_seq=4 ttl=115 time=30.9 ms
   64 bytes from any-in-2678.1e100.net (216.239.38.120): icmp_seq=5 ttl=115 time=29.7 ms

   --- google.com ping statistics ---
   5 packets transmitted, 5 received, 0% packet loss, time 4006ms
   rtt min/avg/max/mdev = 29.650/31.021/32.690/1.214 ms
   ```

   - Hanya akan mengirim 5 packet

7. Setting timeout, dengan opsi `-w`

   ```bash
   ping -w 3000 google.com

   ```

   - Hanya akan mengirim 5 packet, dan hanya akan mengirim ketika ada respon dalam waktu 2 detik

## Ping di Windows

1. Secara default, windows hanya mengirim 4 paket
2. Untuk ping lebih, gunakan `ping -t` dan `ping a google.com`

## Sekaligus melihat paket size

```bash
ping -s 64 google.com
```

## Time To Live

```bash
ping -t google.com
```

## Legalitas

- Ingat apabila ping ke HOST atau IP yang tidak familiar, bisa dianggap mengganggu dan bertentangan dengan kebijakan
