---
id: "Exemplar: Install software in a Linux distribution"
aliases: []
tags: []
---

tags: [[google_cybersecurity]]

## **Rangkuman: Exemplar - Install Software in a Linux Distribution**

### **Gambaran Aktivitas**

- Anda menggunakan **APT (Advanced Package Tool)** dan **sudo** di Bash shell untuk **menginstal** dan **menghapus aplikasi** di Linux.
- APT mempermudah manajemen aplikasi di Linux, bahkan untuk tugas yang kompleks.
- Contoh aplikasi: **Suricata** (deteksi intrusi jaringan) dan **tcpdump** (analisis lalu lintas jaringan).
- Lingkungan virtual digunakan untuk menghindari kerusakan sistem dan memungkinkan rollback.
- Aktivitas ini relevan untuk peran **security analyst** yang perlu mengelola aplikasi Linux.

---

### **Skenario**

Tugas Anda:

1. **Instal**, **hapus**, dan **pasang ulang** aplikasi **Suricata** dan **tcpdump** di Bash shell.
2. **Konfirmasi instalasi** dan tampilkan daftar aplikasi yang terinstal.

---

### **Langkah-Langkah Tugas**

#### **Task 1: Pastikan APT Terinstal**

- Jalankan perintah berikut:
  ```bash
  apt
  ```
- Output menunjukkan **versi APT** dan informasi penggunaan jika terinstal.
- **APT terinstal secara default** di sistem berbasis Debian di lab ini.

---

#### **Task 2: Instal dan Hapus Aplikasi Suricata**

1. **Instal Suricata**:
   ```bash
   sudo apt install suricata
   ```
2. **Verifikasi instalasi**:
   ```bash
   suricata
   ```
   Output menampilkan **versi dan opsi penggunaan Suricata**.
3. **Hapus Suricata**:
   ```bash
   sudo apt remove suricata
   ```
4. **Verifikasi penghapusan**:
   ```bash
   suricata
   ```
   Output: **error** menunjukkan Suricata telah dihapus.

---

#### **Task 3: Instal Aplikasi tcpdump**

- Gunakan perintah berikut untuk menginstal tcpdump:
  ```bash
  sudo apt install tcpdump
  ```

---

#### **Task 4: Tampilkan Aplikasi yang Terinstal**

1. Gunakan perintah untuk **melihat daftar aplikasi**:
   ```bash
   apt list --installed
   ```
2. Cari **tcpdump** dalam daftar, yang menunjukkan aplikasi telah terinstal.

---

#### **Task 5: Pasang Ulang Suricata**

1. **Pasang ulang Suricata**:
   ```bash
   sudo apt install suricata
   ```
2. **Tampilkan daftar aplikasi terinstal**:
   ```bash
   apt list --installed
   ```
3. Cari **Suricata** dan **tcpdump** dalam daftar untuk memastikan keduanya terinstal.

---

### **Kesimpulan**

- Anda telah mempelajari cara menggunakan **APT package manager** untuk:
  - Menginstal aplikasi.
  - Menghapus aplikasi.
  - Melihat daftar aplikasi terinstal.
- Kemampuan ini penting untuk seorang **security analyst** dalam mengelola aplikasi Linux.
