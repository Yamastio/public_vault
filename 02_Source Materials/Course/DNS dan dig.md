---
id: DNS dan dig
aliases:
  - dig
  - DNS
tags: []
---

Tags: [[networking_fundamentals]]

# 🌐 **DNS & Perintah `dig`: Cara Kerja Penerjemah Internet**

## 📞 **Apa Itu DNS?**

DNS (_Domain Name System_) adalah **"buku telepon internet"** yang mengubah nama domain (seperti `google.com`) menjadi alamat IP (seperti `172.217.16.206`).

- **Tanpa DNS**: Kita harus hafal deretan angka IP untuk setiap website!

---

## 🔍 **Proses DNS Lookup (Langkah demi Langkah)**

### **1. Cek Hosts File & Cache Lokal**

- **Hosts File**: File di komputer Anda yang bisa memetakan domain ke IP secara manual _(jarang digunakan sekarang)_.
- **Cache DNS**: Penyimpanan sementara IP domain yang pernah diakses.
  → Jika domain sudah ada di sini, proses berhenti.

### **2. Tanya Recursive DNS Server**

- **Recursive DNS**: Server yang dikelola ISP/penyedia (contoh: Google DNS `8.8.8.8`).
- Jika domain tidak ada di cache-nya, server ini akan **meneruskan permintaan ke root DNS**.

### **3. Root DNS Server**

- **13 IP Root DNS**: Server paling atas yang tahu alamat **TLD DNS** (server untuk ekstensi seperti `.com`, `.id`).

### **4. TLD DNS Server**

- **TLD (_Top-Level Domain_)**:
  - `.com`, `.org`, `.co.id`, dll.
  - Server ini tahu **Authoritative DNS** untuk domain tertentu.

### **5. Authoritative DNS Server**

- **Pemilik Domain**: Menyimpan rekaman DNS asli (IP, MX record, dll).
- **Contoh**: Authoritative DNS untuk `tryhackme.com` akan memberikan IP sebenarnya.

---

## 🕵️ **Perintah `dig`: Detektif DNS**

`dig` adalah alat untuk **menanyakan DNS server secara manual**.

### **Sintaks Dasar**

```bash
dig <domain> @<dns-server>
# Contoh:
dig google.com @8.8.8.8
```

### **Output Penting**

```bash
;; ANSWER SECTION:
google.com.      157    IN    A    172.217.16.206
```

- **TTL (_Time To Live_)**: `157` detik → Waktu sampai data DNS di-cache harus diperbarui.
- **A Record**: Alamat IPv4 domain.

---

## 🧩 **Mengapa TTL Penting?**

- **Cache**: Komputer/router menyimpan DNS untuk mempercepat akses.
- **TTL Habis?** Permintaan baru akan dikirim ke DNS server.

---

## 📊 **Jenis-Jenis DNS Server**

| **Tipe DNS Server** | **Peran**                                      | **Contoh**                   |
| ------------------- | ---------------------------------------------- | ---------------------------- |
| **Recursive**       | Mencari jawaban dari root sampai authoritative | `8.8.8.8` (Google)           |
| **Root**            | Mengarahkan ke TLD DNS                         | 13 server global             |
| **TLD**             | Mengarahkan ke authoritative DNS               | Server untuk `.com`          |
| **Authoritative**   | Menyimpan data DNS asli domain                 | Server milik pemilik website |

---

## 💡 **Kapan Menggunakan `dig`?**

1. **Troubleshooting**: Cek apakah DNS server merespons dengan benar.
2. **Cek TTL**: Pastikan perubahan DNS sudah berlaku (setelah TTL habis).
3. **Cek Record Lain**: MX (email), CNAME (alias), TXT (verifikasi).

---

🔍 **Contoh Kasus**:

```bash
dig tryhackme.com +short  # Langsung tampilkan IP
dig mx gmail.com          # Cek server email Gmail
```

**Tips**:

- Gunakan `+trace` untuk melihat seluruh proses DNS lookup:
  ```bash
  dig google.com +trace
  ```

---

_"DNS ibarat penerjemah yang mengubah nama domain jadi alamat IP. Dengan `dig`, kita bisa jadi detektif yang melacak proses ini!"_ 🕵️♂️
