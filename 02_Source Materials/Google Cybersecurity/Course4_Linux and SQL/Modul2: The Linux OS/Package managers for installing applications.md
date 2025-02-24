---
id: Package managers for installing applications
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Rangkuman Package Managers untuk Linux**

### **1. Pengertian Package dan Package Manager**

- **Package**: Komponen perangkat lunak yang dapat digabungkan untuk membentuk aplikasi.
  - Berisi file yang diperlukan untuk instalasi aplikasi, termasuk **dependencies** (file tambahan yang dibutuhkan aplikasi).
- **Package Manager**: Alat untuk menginstal, mengelola, dan menghapus package atau aplikasi.
  - Membantu menyelesaikan masalah dependencies secara otomatis.
  - Penting untuk menggunakan **versi terbaru** dari package karena berisi pembaruan keamanan dan perbaikan bug.

### **2. Jenis Package Managers Berdasarkan Distribusi Linux**

- **Debian-derived**:
  - Contoh: KALI LINUX™, Ubuntu, Parrot.
  - **Package Manager**: `dpkg` dengan file berekstensi **.deb** (contoh: `Package_Version-Release_Architecture.deb`).
- **Red Hat-derived**:
  - Contoh: CentOS.
  - **Package Manager**: Red Hat Package Manager (**RPM**) dengan file berekstensi **.rpm** (contoh: `Package-Version-Release_Architecture.rpm`).

### **3. Alat Manajemen Paket Tambahan (Package Management Tools)**

- Mempermudah tugas dasar seperti instalasi package melalui **command-line interface**.
  - **Advanced Package Tool (APT)**:
    - Digunakan pada distribusi berbasis **Debian**.
    - Memungkinkan pencarian dan instalasi package secara efisien.
  - **Yellowdog Updater Modified (YUM)**:
    - Digunakan pada distribusi berbasis **Red Hat**.
    - Berfungsi untuk mengelola file **.rpm**.

### **4. Poin Penting**

- **Debian-derived distributions**: Gunakan package manager seperti `dpkg` atau alat seperti **APT**.
- **Red Hat-derived distributions**: Gunakan package manager **RPM** atau alat seperti **YUM**.
- **Package Management Tools** menyederhanakan pengelolaan package melalui terminal.
