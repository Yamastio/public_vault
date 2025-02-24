---
id: Static Route
aliases: []
tags: []
---

## **1. What (Apa itu Static Route?)**

- **Static route** adalah rute jaringan yang ditentukan secara manual oleh administrator jaringan. Ini adalah cara untuk mengarahkan lalu lintas dari satu jaringan ke jaringan lain melalui gateway tertentu.
- Static route tidak berubah kecuali diubah secara manual oleh administrator, berbeda dengan **dynamic routing** yang menggunakan protokol seperti OSPF atau BGP untuk menentukan rute secara otomatis.

---

## **2. Who (Siapa yang Menggunakan Static Route?)**

- **Administrator Jaringan:** Mereka yang bertanggung jawab atas pengelolaan jaringan menggunakan static route untuk mengontrol aliran lalu lintas antar jaringan.
- **Pengguna Linux/Server:** Pengguna yang mengelola server atau perangkat jaringan (seperti router) sering kali menggunakan static route untuk mengatur komunikasi antar jaringan lokal atau internet.
- **Organisasi Kecil/Menengah:** Static route sering digunakan dalam jaringan kecil karena sederhana dan tidak memerlukan overhead protokol routing dinamis.

---

## **3. When (Kapan Static Route Digunakan?)**

- **Saat Jaringan Statis:** Static route cocok digunakan jika topologi jaringan jarang berubah.
- **Untuk Keamanan:** Saat Anda ingin memblokir akses ke jaringan tertentu atau mengarahkan traffic ke "blackhole" untuk mitigasi serangan DDoS.
- **Dalam Lingkungan Terbatas:** Misalnya, di laboratorium atau lingkungan uji coba untuk simulasi routing.
- **Saat Dynamic Routing Tidak Diperlukan:** Jika tidak ada kebutuhan untuk protokol routing dinamis yang kompleks, static route adalah solusi yang efisien.

---

## **4. Where (Di Mana Static Route Diterapkan?)**

- **Router:** Static route biasanya dikonfigurasi pada router untuk mengarahkan lalu lintas antar jaringan.
- **Server:** Pada server Linux, static route dapat dikonfigurasi menggunakan perintah seperti `route` atau `ip route`.
- **Firewall:** Static route juga dapat diterapkan pada firewall untuk mengontrol arus lalu lintas masuk dan keluar.
- **Perangkat Jaringan Lainnya:** Switch Layer 3, access point, atau perangkat jaringan lain yang mendukung routing statis.

---

## **5. Why (Mengapa Static Route Penting?)**

- **Kontrol Penuh:** Administrator memiliki kontrol penuh atas bagaimana lalu lintas jaringan dialihkan.
- **Efisiensi:** Static route tidak memerlukan overhead protokol routing dinamis, sehingga lebih hemat sumber daya.
- **Keamanan:** Anda dapat memblokir akses ke jaringan tertentu atau mengarahkan traffic ke blackhole untuk mencegah serangan.
- **Sederhana:** Mudah dikonfigurasi dan dipahami, terutama dalam jaringan kecil.
- **Stabilitas:** Karena static route tidak berubah secara otomatis, ini memberikan stabilitas dalam jaringan yang tidak sering berubah.

---

## **6. How (Bagaimana Cara Mengonfigurasi Static Route?)**

### **A. Menggunakan Perintah `route`**

1. **Melihat Routing Table:**

   ```bash
   route -n
   ```

   Output:

   ```
   Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
   192.168.1.0     0.0.0.0         255.255.255.0   U     0      0        0 eth0
   ```

2. **Menambahkan Static Route:**

   ```bash
   sudo route add -net 192.168.2.0 netmask 255.255.255.0 gw 172.16.1.1
   ```

   Penjelasan:

   - Mengarahkan lalu lintas ke jaringan `192.168.2.0/24` melalui gateway `172.16.1.1`.

3. **Menghapus Static Route:**
   ```bash
   sudo route del -net 192.168.2.0 netmask 255.255.255.0 gw 172.16.1.1
   ```

### **B. Menggunakan Perintah `ip route`**

1. **Menampilkan Routing Table:**

   ```bash
   ip route show
   ```

2. **Menambahkan Static Route:**

   ```bash
   sudo ip route add 192.168.2.0/24 via 172.16.1.1
   ```

3. **Menghapus Static Route:**

   ```bash
   sudo ip route del 192.168.2.0/24 via 172.16.1.1
   ```

4. **Mengatur Default Gateway:**
   ```bash
   sudo ip route add default via 192.168.1.1
   ```

---

## **Contoh Kasus**

### **A. Memisahkan Traffic Internal dan Eksternal**

- Misalkan Anda memiliki dua jaringan:
  - **Jaringan internal:** `192.168.1.0/24`
  - **Jaringan eksternal (internet):** Melalui gateway `192.168.1.1`
- Anda dapat menambahkan static route untuk mengarahkan traffic internal ke gateway internal dan traffic eksternal ke gateway publik.

### **B. Mitigasi Serangan DDoS**

- Jika ada IP yang mencurigakan (`192.168.1.100`), Anda dapat mem-blokir traffic ke IP tersebut:
  ```bash
  sudo route add -host 192.168.1.100 reject
  ```

### **C. Blackhole Routing**

- Untuk mencegah traffic mencapai tujuan tertentu (misalnya, IP `192.168.1.103`):
  ```bash
  sudo ip route add blackhole 192.168.1.103
  ```

---

## **Kesimpulan**

- **Static route** adalah alat penting dalam manajemen jaringan yang memberikan kontrol penuh atas aliran lalu lintas.
- Dengan pendekatan **5W + 1H**, kita dapat memahami bahwa static route digunakan oleh administrator jaringan (Who), dalam berbagai skenario (When), di berbagai perangkat (Where), untuk alasan efisiensi dan keamanan (Why), dan dikonfigurasi menggunakan perintah seperti `route` atau `ip route` (How).

Dengan pemahaman ini, Anda dapat mulai mengimplementasikan static route di lingkungan jaringan Anda sendiri! 😊
