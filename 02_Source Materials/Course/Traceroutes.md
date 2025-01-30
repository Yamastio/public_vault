---
id: Traceroutes
aliases: []
tags: []
---

Tags: [[networking_fundamentals]]

# 🗺️ **Perintah `traceroute`: Pemetaan Jalan Data ke Server Target**

---

## 🌍 **Apa Itu `traceroute`?**

`traceroute` adalah alat untuk **melacak rute yang dilewati data** dari komputer Anda ke server tujuan.

- 🚗 **Analoginya**: Seperti mengecek pos-pos pemeriksaan dalam perjalanan darat.
- 🎯 **Fungsi Utama**:
  - Tampilkan semua "pemberhentian" (_hop_) yang dilalui data.
  - Identifikasi di mana koneksi terhambat/terputus.

---

## 🔧 **Cara Kerja `traceroute`**

### **Konsep TTL (_Time to Live_)**

Setiap paket data memiliki "nomor TTL" yang berkurang 1 di setiap _hop_.

- Saat TTL = 0, server di _hop_ itu mengirim balasan ke Anda.
- `traceroute` menggunakan ini untuk **mengetahui alamat setiap perantara**.

### **Protokol yang Digunakan**

- **Windows**: `tracert` pakai **ICMP** (sama seperti `ping`).
- **Linux/macOS**: `traceroute` pakai **UDP** (bisa diubah dengan opsi).

---

## 📝 **Contoh Penggunaan**

```bash
traceroute google.com
```

**Output**:

```
 1  _gateway (192.168.1.1)  1.234 ms  1.456 ms  1.789 ms
 2  10.10.10.1              5.678 ms  6.123 ms  6.789 ms
 ...
13  mia07s54-in-f14.1e100.net (216.58.205.46)  15.4 ms  15.6 ms  16.1 ms
```

- **Keterangan**:
  - **Kolom 1**: Nomor _hop_ (langkah ke-1, ke-2, dst.).
  - **Kolom 2**: Alamat IP/server di _hop_ tersebut.
  - **Kolom 3-5**: Waktu tempuh paket (dalam milidetik) ke server itu.

---

## 🆚 **Bedanya `ping` dan `traceroute`**

| **Fitur**            | **`ping`**                | **`traceroute`**                     |
| -------------------- | ------------------------- | ------------------------------------ |
| **Tujuan**           | Cek koneksi langsung      | Lacak _semua_ langkah perjalanan     |
| **Detail**           | Hanya tahu "sampai/tidak" | Tahu rute lengkap + latency tiap hop |
| **Kasus Penggunaan** | Troubleshooting dasar     | Analisis jaringan kompleks           |

---

## 💡 **Tips & Trik**

- **Batasi Jumlah Hop**:
  ```bash
  traceroute -m 10 google.com  # Hanya tampilkan 10 hop pertama
  ```
- **Ganti Protokol di Linux**:
  ```bash
  traceroute -I google.com  # Pakai ICMP (seperti Windows)
  ```
- **Baca Manual**:
  ```bash
  man traceroute  # Lihat opsi lengkap (Linux/macOS)
  ```

---

## 🧠 **Kenapa Ada Banyak Hop?**

- Internet adalah jaringan global yang terhubung via **router**, **ISP**, dan **data center**.
- Contoh rute:
  `Komputer Anda → Router Rumah → ISP → Server Google`
  _(Tiap "→" adalah 1 hop!)_

---

## 🚨 **Batasan `traceroute`**

- **Server Diam**: Beberapa hop tidak merespons (tampil sebagai `* * *`).
- **Firewall**: Blokir protokol ICMP/UDP, sehingga hop "hilang".
- **Rute Berubah**: Jalur bisa berbeda tiap waktu, tergantung beban jaringan.

---

🔍 **Gunakan `traceroute` saat:**

- Website lambat → cari di hop mana latency tinggi.
- Koneksi putus-putus → identifikasi hop yang bermasalah.

_"Seperti detective yang melacak jejak paket data!"_ 🕵️♂️
