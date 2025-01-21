---
id: Additional network protocols
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## 1. Network Address Translation (NAT)

- **Fungsi**: Mengonversi alamat IP privat menjadi alamat IP publik untuk komunikasi dengan internet.
- **Proses**: Router menggantikan alamat sumber privat dengan alamat publik, lalu melakukan operasi sebaliknya untuk tanggapan.
- **Lapisan TCP/IP**: Internet (Layer 2) & Transport (Layer 3).
- **IP Privat**: Digunakan dalam jaringan lokal (gratis).
- **IP Publik**: Digunakan di internet global (berbiaya, unik secara global).

## 2. Dynamic Host Configuration Protocol (DHCP)

- **Fungsi**: Mengatur konfigurasi alamat IP perangkat di jaringan, termasuk alamat DNS dan gateway.
- **Lapisan TCP/IP**: Application Layer.
- **Port**:
  - UDP 67 (server).
  - UDP 68 (klien).

## 3. Address Resolution Protocol (ARP)

- **Fungsi**: Mengonversi alamat IP menjadi alamat MAC untuk komunikasi dalam jaringan lokal.
- **Lapisan TCP/IP**: Network Access (Layer 2).
- **Port**: Tidak ada (karena Layer 2).

## 4. Telnet

- **Fungsi**: Menghubungkan perangkat jarak jauh menggunakan command line (informasi dikirimkan dalam teks biasa, tidak aman).
- **Lapisan TCP/IP**: Application Layer.
- **Port**: TCP 23.

## 5. Secure Shell (SSH)

- **Fungsi**: Menghubungkan perangkat jarak jauh dengan autentikasi dan komunikasi terenkripsi.
- **Lapisan TCP/IP**: Application Layer.
- **Port**: TCP 22.

## 6. Post Office Protocol (POP3)

- **Fungsi**: Mengunduh email dari server ke perangkat lokal.
- **Lapisan TCP/IP**: Application Layer.
- **Port**:
  - TCP/UDP 110 (unencrypted).
  - TCP/UDP 995 (encrypted, SSL/TLS).

## 7. Internet Message Access Protocol (IMAP)

- **Fungsi**: Mengunduh header email dan menyimpan konten di server, memungkinkan sinkronisasi di banyak perangkat.
- **Lapisan TCP/IP**: Application Layer.
- **Port**:
  - TCP 143 (unencrypted).
  - TCP 993 (encrypted, SSL/TLS).

## 8. Simple Mail Transfer Protocol (SMTP)

- **Fungsi**: Mengirim dan merutekan email dari pengirim ke penerima menggunakan Message Transfer Agent (MTA).
- **Lapisan TCP/IP**: Application Layer.
- **Port**:
  - TCP/UDP 25 (unencrypted, sering digunakan spam).
  - TCP/UDP 587 (encrypted, TLS).

## 9. Protokol dan Port Penting untuk Dihafal

| **Protokol** | **Port**                                            |
| ------------ | --------------------------------------------------- |
| **DHCP**     | UDP 67 (server), UDP 68 (klien).                    |
| **ARP**      | Tidak ada.                                          |
| **Telnet**   | TCP 23.                                             |
| **SSH**      | TCP 22.                                             |
| **POP3**     | TCP/UDP 110 (unencrypted), TCP/UDP 995 (encrypted). |
| **IMAP**     | TCP 143 (unencrypted), TCP 993 (encrypted).         |
| **SMTP**     | TCP/UDP 25 (unencrypted), TCP/UDP 587 (encrypted).  |

## Catatan Penting

- Firewall dapat memfilter lalu lintas berdasarkan nomor port untuk mencegah akses yang tidak diinginkan.
- Penting untuk memahami di mana protokol ini berada dalam model TCP/IP dan fungsinya.
