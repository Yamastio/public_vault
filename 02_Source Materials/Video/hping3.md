---
id: hping3
aliases: []
tags: []
---

## Deskripsi

What: hping3 adalah linux tool untuk membuat custom paket
Who: Developed oleh Salvatore Sanfilippo, open source
When: First released in 1998, aktif didevelop
Where: Linux terminal / shell
Why: Network testing, firewall testing, port scanning, security auditing
How: Membuat dan mengirim paket dengan protocol berbeda dan opsi.

## Praktik

### Buka terminal

`ctrl + alt + t`

### Kirim paket TCP ke host

[ ] Ketik `sudo hping3 172.16.1.120`
[ ] Enter
[ ] `Ctrl + C` untuk stop

### Spesifikan nilai dari paket

[ ] Ketik `sudo hping3 172.16.1.120 -c 4`, mengirimkan 4 paket

### Observasi dari output hping3

[ ] len: Panjang dari paket
[ ] IP: IP dari target
[ ] ttl: Time to live, maksimal angka dari hops paket yang bisa diambil sebelum di buang
[ ] DF: "Don't Fragment" flag, mengindikasikan paket tidak bisa dibagi
[ ] id: Nomor identitas dari suatu paket
[ ] sport: Source port(port sumber)
[ ] flags: TCP flag, mengindikasikan flag-flag yang digunakan dalam paket
[ ] seq: sequence number, nomor urutan paket
[ ] win: window size, ukuran window dari suatu paket
[ ] rtt: Round Trip Time, waktu terjadinya paket

### Mengirim ICMP paket ke host

[ ] `sudo hping3 --icmp 172.16.1.120`
[ ] TCP flags:
[ ] `CWR`: Congestion Window Reduced
[ ] `ECE`: Explicit Congestion Notification
[ ] `URG`: Urgent Pointer
[ ] `ACK`: Acknowledgement
[ ] `PSH`: Push
[ ] `RST`: Reset
[ ] `SYN`: Synchronize sequence numbers
[ ] `FIN`: Finish

### TCP 3-way handshake

[ ] SYN
[ ] SYN+ACK
[ ] ACK

### Mengirim syn paket ke target(half open)

[ ] `sudo hping3 --syn 172.16.1.120`
[ ] hping3 bisa digunakan untuk mengecek sikap dari firewall, begitu juga untuk tes IPS. Dengan mengirimkan syn paket ke port yang berbeda, security analist, biasanya menganalisis mana port yang berhasil di blok, dan yang tetap di acc.

### Syn flood, dengan hping3

[ ] `sudo hping3 --flood 172.16.1.120`

### Distributed Denial of Service (DDoS)

`sudo hping3 -c 10000 -d 120 -S -w 64 -p 80 --flood --rand-source 172.16.1.120`

[ ] Penyerang membanjiri permintaan atau mengirim ICMP pesan berupa ping ke target. Penerima membalas IP korban, membanjiri dengan respons. Dinamakan Distributed, karena penyerang menyerang dengan menyamar dengan IP yang lain

[ ] Analogi seperti sekumpulan anak yang iseng, dengan menekan bel suatu rumah lalu ketika pemilik rumah membuka, mereka sembunyi, dilakukan berkali-kali tapi dengan anak yang berbeda.

#### Break down Command:

- -c 10000: mengirim 10,000 paket
- -d 120
- -S: Menggunakan syn packet
- -w 64L: Mengatur windwos size ke 64(flow control mekanisme)
- -p 80: Menyerang port 80 --flood, berarti dengan continue ke target
- --rand-source: Randomize the Source IP Address, melakukan spoofing source IP, jadi tidak dari satu IP saja yang membanjiri

### Help

[ ] hping3 --help

## Kesimpulan

- Diperlukan perhatian ketika menggunakan alat hping3 untuk mengetes jaringan tanpa izin itu adalah tindakan yang ilegal dan tidak etis. Spoofing IP Address di network packet bisa dianggap sebagai perilaku berbahaya dan bisa menerima beberapa tuntutan hukum

[ ] Cyber Kill Chain
[ ] man hping3
