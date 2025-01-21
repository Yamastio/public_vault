---
id: The evolution of wireless security protocols
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Rangkuman: Evolusi Protokol Keamanan Nirkabel

### Latar Belakang

- **Internet Awal**:
  - Awalnya, semua komunikasi internet menggunakan kabel fisik.
  - Pada pertengahan 1980-an, spektrum frekuensi gelombang radio yang dapat digunakan tanpa lisensi mulai digunakan untuk memperluas internet.
- **Era Nirkabel**:
  - Teknologi pengiriman dan penerimaan data melalui gelombang radio berkembang pada akhir 1990-an dan awal 2000-an.
  - Saat ini, berbagai perangkat seperti laptop, smartphone, dan perangkat pintar (misalnya, termostat, kunci pintu, dan kamera keamanan) menggunakan Wi-Fi untuk berkomunikasi.

### Standar Wi-Fi

- **IEEE 802.11**:
  - Basis protokol komunikasi nirkabel yang ditentukan oleh IEEE (Institute of Electrical and Electronics Engineers).
- **Wi-Fi**:
  - Istilah pemasaran yang awalnya diperkenalkan oleh Wireless Ethernet Compatibility Alliance (kini Wi-Fi Alliance).

### Evolusi Protokol Keamanan Wi-Fi

![eovolusi wifi](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xRV4czFOTUeQoV2vrMyMeg_d23346290329425da28d901333b11af1_KRMIlg0NE-hyueu8ieJBVc92c_gZAut6oOyRG0iOjP58SBeS6AojyB3piYq3ZOtOCf1kwrG62COp1ei3Uih_CcoNT2_QdtdaHyEchUsGTcmreFbywK_tUWZJGhMD3Tji9hxIUjH-yQAD8RSKpTbtJDHXD88IOpsqzlu8MCJotlno6JixxiW8pmiYFuzqHZ1bZhfT3cMFIZxI3sPnCh_BnizMW3y21VJuVZcX?expiry=1734998400000&hmac=1GqzZuX1wD6HdTVjnCWm4cD1rnTTAtXINjjo3nPttMw)

1. **Wired Equivalent Privacy (WEP)**

   - **Diperkenalkan**: 1999.
   - **Tujuan**: Memberikan privasi pada jaringan nirkabel setara dengan jaringan kabel.
   - **Kelemahan**:
     - Mudah diretas karena enkripsi lemah.
     - Kini dianggap berisiko tinggi, tetapi masih ditemukan pada perangkat lama atau konfigurasi default.

2. **Wi-Fi Protected Access (WPA)**

   - **Diperkenalkan**: 2003 sebagai pengganti WEP.
   - **Peningkatan**:
     - Menggunakan **Temporal Key Integrity Protocol (TKIP)** untuk meningkatkan enkripsi.
     - Menambahkan pemeriksaan integritas pesan untuk mencegah modifikasi data.
   - **Kelemahan**: Rentan terhadap serangan **Key Reinstallation Attack (KRACK)**, memungkinkan dekripsi data.

3. **WPA2**

   - **Diperkenalkan**: 2004 sebagai pengganti WPA.
   - **Peningkatan**:
     - Menggunakan **Advanced Encryption Standard (AES)** untuk enkripsi yang lebih kuat.
     - Memanfaatkan **CCMP** untuk otentikasi dan integritas pesan.
   - **Mode Personal**: Cocok untuk jaringan rumah dengan konfigurasi sederhana.
   - **Mode Enterprise**: Cocok untuk organisasi dengan kontrol terpusat dan keamanan lebih tinggi.
   - **Kelemahan**: Masih rentan terhadap KRACK.

4. **WPA3**
   - **Diperkenalkan**: 2018 sebagai pengganti WPA2.
   - **Keunggulan**:
     - Mengatasi kerentanan KRACK dengan **Simultaneous Authentication of Equals (SAE)**.
     - Enkripsi lebih kuat dengan 128-bit untuk personal dan opsional 192-bit untuk enterprise.

### Poin Penting bagi Analis Keamanan

- **Pemahaman Protokol**:
  - Mengetahui sejarah dan kelemahan setiap protokol membantu melindungi jaringan nirkabel secara efektif.
- **Pembaruan Teknologi**:
  - Pastikan perangkat menggunakan protokol keamanan terbaru (seperti WPA3) untuk mengurangi risiko serangan.
- **Evaluasi Jaringan**:
  - Periksa apakah ada perangkat lama yang masih menggunakan protokol usang seperti WEP.

Keamanan Wi-Fi terus berkembang seiring waktu untuk menjawab tantangan baru, menjadikannya aspek penting dalam infrastruktur keamanan modern.
