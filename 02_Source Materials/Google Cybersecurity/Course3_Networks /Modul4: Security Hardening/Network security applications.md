---
id: Network security applications
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Pendekatan Layered Security (Defense in Depth)

![network](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4ENRXSswQSOsOrKt9KyG6A_06fe04a8d10846ba811fe89a969642f1_CS_R-055_Firewall-IDS-and-IPS.png?expiry=1735084800000&hmac=cuq9P8xy1dOPdDytYyNz_sUZFRDtwiyfNqCDzDB-vBY)

- Layered security menambahkan lapisan keamanan secara bertahap untuk memperkuat jaringan hingga mencapai tingkat keamanan yang diinginkan.
- Kombinasi perangkat dan alat keamanan mencakup **firewall**, **Intrusion Detection System (IDS)**, **Intrusion Prevention System (IPS)**, dan **Security Information and Event Management (SIEM)**.

## Perangkat dan Fungsinya

1. **Firewall**

![firewall](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dSLcIcXBSw-kw-9kzEwhAw_284c8540dab14a9e911296471c71d2f1_CS_R-055_Firewall.png?expiry=1735084800000&hmac=aP4t2gYHwlxd4EdmfGHrQKmaCdh5l0bsAPpFtt5lrp8)

- **Fungsi**: Memblokir atau mengizinkan lalu lintas berdasarkan aturan tertentu.
- **Keunggulan**:
  - Menggunakan port filtering untuk mengontrol lalu lintas.
  - NGFW (Next-Generation Firewall) dapat memeriksa payload paket.
- **Keterbatasan**: Hanya memfilter berdasarkan informasi header paket.

2. **Intrusion Detection System (IDS)**

![IDS](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5hPelJ74TwaKusUY4ZEkkQ_bcd56306ce904397a352cfe37e28b6f1_CS_R-055_IDS.png?expiry=1735084800000&hmac=xIFePLR2s9kJSlSB7nh0UAjmx9IxPQ_LCbLmNRDfr7o)

- **Fungsi**: Mendeteksi dan memberikan peringatan tentang lalu lintas mencurigakan.
- **Keunggulan**:
  - Menganalisis data paket untuk tanda serangan yang dikenal.
  - Mengurangi false positives dengan ditempatkan di belakang firewall.
- **Keterbatasan**:
  - Tidak dapat menangkap serangan baru atau canggih.
  - Tidak menghentikan serangan, hanya memberikan laporan.

3. **Intrusion Prevention System (IPS)**

![IPS](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sp1NiS2HR3KoLCBP36lq3g_f612a9b5e6cc47b2a9341208200b3ff1_CS_R-055_IPS.png?expiry=1735084800000&hmac=61qwd-xYTnQL-pm37kbgOxDtNEzVOzuwLCe0UZXsmhI)

- **Fungsi**: Mendeteksi dan menghentikan aktivitas mencurigakan.
- **Keunggulan**:
  - Dapat memblokir pengirim tertentu atau paket yang mencurigakan.
- **Keterbatasan**:
  - Inline device—jika gagal, koneksi internet ke jaringan internal bisa terputus.
  - Berisiko menghasilkan false positives, yang dapat memblokir lalu lintas sah.

4. **Security Information and Event Management (SIEM)**

![SIEM](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sTtz1jL8QzCTVyhfvICu1A_ee623d56206843d6823598a8f0e70ef1_eyi2ksdTfw4mJcwZ6NvBKQBg-7CVFr-2tq8qNBLlVbloMUlJsvGdPwkSGEk-5VnBU3eXxe9dF7mGPjvyN2T3nWNKtXtu19K2Ycnbt_rEE5FAE4rbNvixbF_oeU82PyiZWpEVVoTqMf6eQJWl7uRMQyvIWA94vNp88ew46W52Kh7QkFeihWUfB8cQkB5dI5c?expiry=1735084800000&hmac=qrh74hdKii9C89uv8vesQ39b1s2CPaUgI-uRd7IGvF0)

- **Fungsi**: Mengumpulkan dan menganalisis log data dari berbagai perangkat untuk memantau aktivitas kritis.
- **Keunggulan**:
  - Mengintegrasikan data dari IDS, IPS, firewall, VPN, dan log lainnya ke dalam satu dashboard (single pane of glass).
  - Memberikan wawasan real-time kepada analis keamanan.
- **Keterbatasan**:
  - Tidak secara langsung menghentikan atau mencegah aktivitas mencurigakan.

## Tambahan: Full Packet Capture Devices

- **Fungsi**: Merekam dan menganalisis semua data yang dikirim melalui jaringan, mendukung investigasi lebih dalam terhadap alert dari IDS atau SIEM.

## Pertimbangan Penting

- **Keuntungan**: Kombinasi alat ini meningkatkan perlindungan jaringan secara bertahap.
- **Keterbatasan**: Biaya pembelian, instalasi, dan pemeliharaan; membutuhkan tenaga ahli tambahan untuk memantau alat keamanan seperti SIEM.
- **Keputusan**: Memilih alat dan tingkat keamanan harus disesuaikan dengan anggaran dan risiko organisasi.

Dengan memahami perangkat ini, Anda dapat mengintegrasikan strategi keamanan yang sesuai untuk melindungi jaringan dari berbagai ancaman.

## Key Takeaway

Berikut adalah rangkuman dalam tabel dengan bahasa Indonesia:

| **Perangkat / Alat**                                 | **Keunggulan**                                                                                                                  | **Kekurangan**                                                                                                                                                |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Firewall**                                         | Mengizinkan atau memblokir lalu lintas berdasarkan aturan tertentu.                                                             | Hanya dapat menyaring paket berdasarkan informasi yang terdapat di header paket.                                                                              |
| **Intrusion Detection System (IDS)**                 | Mendeteksi dan memberi peringatan kepada admin tentang kemungkinan intrusi, serangan, atau lalu lintas berbahaya.               | Hanya dapat memindai serangan yang sudah dikenal atau anomali yang jelas. Tidak dapat menghentikan lalu lintas yang masuk.                                    |
| **Intrusion Prevention System (IPS)**                | Memantau aktivitas sistem untuk intrusi dan anomali serta mengambil tindakan untuk menghentikannya.                             | Perangkat inline—jika gagal, koneksi antara jaringan pribadi dan internet terputus. Berisiko menghasilkan false positive yang memblokir lalu lintas yang sah. |
| **Security Information and Event Management (SIEM)** | Mengumpulkan dan menganalisis data log dari berbagai mesin jaringan. Menggabungkan peristiwa keamanan dalam dashboard terpusat. | Hanya melaporkan potensi masalah keamanan; tidak mengambil tindakan untuk menghentikan atau mencegah peristiwa mencurigakan.                                  |
