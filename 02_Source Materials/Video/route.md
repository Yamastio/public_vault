---
id: route
aliases: []
tags: []
---

## Deskripsi

What: Fungsi jaringan untuk IP Routing
Who: SysAdmin dan Network Engineer
When: Ketika digunakan untuk routing di Linux
Where: Di Linux terminal atau shell
Why: Mengontrol paket yang dikirim antara network
How: Via terminal dengan beberapa Opsi

## Praktik

1. Buka terminal, ketikan `route`
2. Observasi output: Destination,. Gateway, Genmask, Flags, Metric, Ref, Use, Iface, dan Scope

### Menambahkan static route baru

Mengatur rute secara statis, agar apabila ada trafic ke IP 192.168.1.0/24 lewat gateway pfsense(172.16.1.1.) terlebih dahulu tanpa langsung ke ip kita.

1. Untuk menambahkan static route baru, gunakan opsi `add` diikuti dengan network destinasi dan gateway. Contoh, kita akan tambahkan route network 192.168.1.0 via gateway 172.16.1.1, menggunakan command:

```bash
sudo route add -net 192.168.1.0 netmask 255.255.255.0 gw 172.16.1.1
```

### Menambahkan metric ke static route

Metric adalah nilai yang menunjukkan "biaya" atau "prioritas" suatu rute. Semakin rendah nilai metric, semakin tinggi prioritas rute tersebut. Maka apabila ada rute lain ke jaringan 192.16.1.0/24 dengan metric yang lebih rendah,maka akan dipilih terlebih dahulu.

1. Untuk menambahkan metric ke route, gunakan opsi `metric`. Contoh kita akan menambahkan metic 1000 ke 192.168.1.0

```bash
route add 192.168.1.0 gw 172.16.1.1 metric 1000
```

### Delete static route

1. Gunakan opsi `del`, contoh kita akan menghapus route diatas

```bash
sudo route del -net 192.168.1.0 netmask 255.255.255.0 gw 172.16.1.1
```

### Block Traffic ke Malicious IP:

1. `ping example.com`
2. `route -n`
3. `sudo route add -host example.com reject`
4. `route -n`
5. `ping example.com`
6. `sudo route del -host example.com reject`
7. `route -n`
8. `ping example.com`

### Mitigasi DDoS Attack(Implementasi "blackhole)

1. `sudo route add 172.16.1.103 gw 127.0.0.1 loc`

### Clearing/Flushing route table

1. `sudo ip route flush cache`

### Getting Help

1. `route --help`
2. `man route`

## Catatan Penting

1. `route` sudah deprecated, saat ini menggunakan `ip route` sebagai gantinya
2. Jika pakai `route`, harus install net-tools
