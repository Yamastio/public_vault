---
id: Domain Names & Whois
aliases: []
tags: []
---

Tags: [[networking_fundamentals]]

# 🌐 **Domain Names & Whois: Penjelasan Sederhana**

---

## 🏷️ **Apa Itu Domain Name?**

Domain adalah **"nama alias"** untuk alamat IP yang sulit diingat.

- **Contoh**:
  - `tryhackme.com` → Lebih mudah daripada mengingat `172.67.209.124`!
- **Fungsi**: Memungkinkan kita mengakses website dengan nama yang manusiawi.

---

## 🔑 **Mengapa Domain Penting?**

Bayangkan harus menghafal **ribuan alamat IP** untuk membuka website favorit!

- **Solusi**: Domain bertindak seperti **buku telepon internet** yang menerjemahkan nama ke IP.

---

## 📝 **Registrasi Domain**

Domain "disewa" dari perusahaan bernama **Domain Registrar** (Contoh: GoDaddy, Namecheap).

- **Proses**:
  1. Cek ketersediaan nama domain.
  2. Bayar biaya sewa (biasanya per tahun).
  3. Domain aktif selama masa sewa.

---

## 🕵️ **Perintah `whois`: Pelacak Pemilik Domain**

`whois` adalah alat untuk **melihat informasi registrasi domain**.

- **Data yang Didapat**:
  - Pemilik domain (_registrant_).
  - Tanggal pendaftaran & kedaluwarsa.
  - Kontak admin/teknis.
  - Nameserver yang digunakan.

⚠️ **Catatan**:

- Di Eropa, data pribadi sering **disensor** (GDPR).
- Di wilayah lain, info mungkin lebih lengkap.

---

## 🛠️ **Cara Menggunakan `whois`**

### **Instalasi (Jika Belum Ada)**

```bash
sudo apt update && sudo apt install whois  # Untuk Debian/Ubuntu
```

### **Sintaks Dasar**

```bash
whois <nama-domain>
```

### **Contoh**

```bash
whois bbc.co.uk
```

**Output**:

```
Domain name: bbc.co.uk
Registrant: British Broadcasting Corporation
Registered on: 1996-08-01
Expiry date: 2024-08-01
Nameservers: ns1.bbc.co.uk, ns2.bbc.co.uk
...
```

---

## 📌 **Apa yang Bisa Dipelajari dari `whois`?**

1. **Kepemilikan Domain**: Siapa/organisasi di balik website.
2. **Masa Aktif**: Apakah domain akan segera kedaluwarsa.
3. **Nameserver**: Server DNS yang mengelola domain (penting untuk investigasi _hosting_).

---

## 🚨 **Batasan `whois`**

- **Data Privasi**: Banyak registrar menyembunyikan info pribadi (gunakan _privacy protection_).
- **Ketidakakuratan**: Data bisa saja tidak diupdate.

---

## 💡 **Contoh Kasus Praktis**

- **Investigasi Website Mencurigakan**: Cek siapa pemilik domain dengan `whois`.
- **Beli Domain**: Pastikan domain tidak sudah terdaftar.

🔍 **Tips**:
Gunakan [web whois](https://whois.domaintools.com/) jika alat CLI tidak tersedia!
