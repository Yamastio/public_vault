---
id: traceroute
aliases: []
tags: []
---

tags: [[hacking_fundamentals]]

## Description

What: Network diagnosis untuk menentukan rute paket
Who: Network Admin dan User
When: Setiap saat apabila ada masalah di jaringan
Where: Support di Windows, MacOs, Linux
Why: Mengidentifikasi bottleneck, troubleshooting, dan analisis routing
How: Mengirim paket dengan meningkatkan TTL (Time To Live), lalu merekam respon dari router

## Praktik:

1.Buka terminal 2. Type `traceroute google.com` 3. Klik Enter 4. Observasi Output

```bash
traceroute to 8.8.8.8 (8.8.8.8), 30 hops max, 60 byte packets
 1  172.30.0.1 (172.30.0.1)  0.501 ms  0.481 ms  0.472 ms
 2  192.168.1.1 (192.168.1.1)  3.689 ms  7.240 ms  7.233 ms
 3  * * *
 4  125.160.0.29 (125.160.0.29)  7.327 ms *  7.840 ms
 5  * 180.240.190.101 (180.240.190.101)  28.428 ms *
 6  * * *
 7  180.240.205.80 (180.240.205.80)  28.656 ms * *
 8  * * *
 9  * * *
10  * * *
11  * * dns.google (8.8.8.8)  35.466 ms
```

- Otuput berisi list dari network hops, dan round trip time(RTT)
  | Scenario | Good RTT Range |
  | --------------------- | -------------- |
  | Local Network | < 1ms |
  | Regional Network | 1-50 ms |
  | National Network | 50-100 ms |
  | International Network | 100-250 ms |
  | Online gaming | < 50 ms |

### Menampilkan hanya output ip address

```bash
traceroute -n google.com
```

### Coba akses web internasional

Coba `ping indiatimes.com`

### Limit hops

`ping google.com -m 5`

### Setting probes and timeout period

- defaultnya 3 probes
- berguna karena lebih banyak data lebih baik

```bash
traceroute -q 4 google.com

```

### Save

```bash
traceroute -w google.com > traceroute.txt
```

## Windows vs Linux

- Tracert di windows
- Tracerout di Linux
