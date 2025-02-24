---
id: The rise of SSO and MFA
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

### Rangkuman: Peningkatan SSO dan MFA dalam Keamanan

**Pendekatan yang Lebih Baik untuk Authentication:**
- **Single Sign-On (SSO):**
  - **Manfaat:**
    1. **Peningkatan Pengalaman Pengguna:** Mengurangi jumlah username dan password yang harus diingat.
    2. **Pengurangan Biaya:** Mengoptimalkan pengelolaan layanan yang terhubung.
    3. **Keamanan yang Lebih Baik:** Mengurangi titik akses yang dapat diserang oleh penyerang.
  - **Masalah yang Dihadapi:** Password yang digunakan berulang-ulang dapat menimbulkan risiko keamanan, dan SSO mengurangi masalah ini dengan memindahkan beban autentikasi kepada pihak ketiga yang terpercaya.

- **Cara Kerja SSO:**
![sso1](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/IaWbLEaURvGv7k6ZSOjbRg_c43ff4ecdca147cca2f5351aaaa917f1_image2.png?expiry=1736035200000&hmac=7Sf11Lk1rib40iNYk3I06KVVodNvtExYzRBicOieR9Y)
  - Menggunakan token akses terenkripsi antara penyedia identitas dan penyedia layanan untuk membuktikan identitas pengguna.
  - Umumnya menggunakan dua protokol:
    1. **LDAP (Lightweight Directory Access Protocol):** Digunakan untuk transmisi data di dalam organisasi.
    2. **SAML (Security Assertion Markup Language):** Digunakan untuk transmisi data di luar organisasi, seperti di cloud.
  - **Kelemahan SSO:** Mengandalkan satu bentuk autentikasi membuatnya rentan, seperti jika password hilang atau dicuri.

**MFA (Multi-Factor Authentication):**
![MFA1](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/hNHsmtDZRI28CtisHKRAew_cedbe22c98dc4ef095d8b8884cf689f1_CS_R-095_mfa-equation.png?expiry=1736035200000&hmac=BwVzKbi_4IAH0oBIK-3-dWsSmR4vvc2H18QmuhO1tCo)
- **Definisi:** Memerlukan dua atau lebih faktor untuk memverifikasi identitas pengguna.
  - **Contoh Analogi:** Seperti mengambil uang dari ATM, yang memerlukan kartu debit (sesuatu yang dimiliki) dan PIN (sesuatu yang diketahui).
  - **Cara Kerja MFA:**
    - **Faktor yang Digunakan:**
      1. **Yang Diketahui Pengguna:** Username dan password.
      2. **Yang Dimiliki Pengguna:** OTP yang dikirim via SMS.
      3. **Yang Dimiliki Pengguna (Fisik):** Biometrik, seperti sidik jari atau pemindaian wajah.
  - **Keuntungan MFA:**
    - Menambah lapisan keamanan, terutama untuk lingkungan cloud.
    - Menurunkan risiko salah autentikasi dengan memerlukan identifikasi yang sulit ditiru atau dipecahkan.

**Poin Utama:**
- Menggabungkan SSO dan MFA memberikan pengalaman pengguna yang lebih cepat dan aman.
- Mengandalkan hanya pada password adalah kelemahan yang besar, sementara SSO mengurangi titik masuk tetapi tetap perlu dipadukan dengan MFA untuk menghindari akses oleh pihak yang tidak sah.
