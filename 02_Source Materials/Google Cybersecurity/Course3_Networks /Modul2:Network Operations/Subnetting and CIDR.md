---
id: Subnetting and CIDR
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Apa Itu Subnetting?

![subnet](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vzbgwk8-RoCJ8Ppet89raA_1a225a330b8b4eaeb4a2b8bc5baaaef1_qvNCswL7ECbUiKTyL6rjp35BTSD-bbfoAoajmAyy4hHvmBJwwr22RU8T5aGDunmwKb1kvZ5TneMbG-nngVlkPXF6W-BTMap_a6XP-kAy5jgW13XvT5OTSCmI7U9YVNX4JzC1qn-zCkiZSXhbKjm2zq7SESzmANYH17_p4jub1mNikwElbJZECK0VuM_4Yrwljgfgdx2VpNad7gx2lFHMiu01wfeRKp-sjRa_kQ?expiry=1734998400000&hmac=DPSY9IGtMoVR-TEaT1JPiFBiks2Z32mUoSFm2pdPxks)

- **Subnetting** adalah proses membagi jaringan menjadi kelompok logis yang lebih kecil, yang disebut **subnets**.
- Subnetting memungkinkan jaringan lebih efisien, meningkatkan kecepatan komunikasi antar perangkat dalam subnet yang sama, dan bisa digunakan untuk membuat **security zones**.
- Dalam subnetting, rentang alamat jaringan dibagi menjadi subnets berdasarkan **alamat IP** dan **network mask** perangkat di jaringan.

## CIDR (Classless Inter-Domain Routing)

- **CIDR** adalah metode untuk menetapkan **subnet masks** pada alamat IP untuk membuat subnet.
- CIDR menggantikan sistem **classful addressing** yang digunakan pada tahun 1980-an, yang membagi alamat IP menjadi kelas (Class A hingga Class E).
- **CIDR** memberikan lebih banyak alamat IPv4 yang tersedia dengan cara membagi jaringan menjadi bagian yang lebih kecil.
- Alamat IP CIDR ditulis dalam format seperti `198.51.100.0/24`, yang mencakup semua alamat IP antara **198.51.100.0** dan **198.51.100.255**.

## Keuntungan Keamanan dari Subnetting

- **Efisiensi Bandwidth**: Subnetting memungkinkan penggunaan bandwidth lebih efisien, karena komunikasi antar perangkat dalam subnet tidak perlu melewati router.
- **Meningkatkan Kinerja**: Membagi jaringan menjadi subnet yang lebih kecil dapat meningkatkan kinerja dengan mengurangi lalu lintas jaringan.
- **Pengisolasi Subnet**: Subnetting juga berfungsi untuk membuat **subnet terisolasi** yang dapat diperkuat dengan isolasi fisik, konfigurasi routing, dan penggunaan firewall untuk meningkatkan keamanan.

## Manfaat Keamanan Subnetting

- **Membuat Jaringan Internal yang Lebih Aman**: Dengan subnetting, organisasi dapat membuat **jaringan kecil** di dalam jaringan privat mereka sendiri tanpa perlu meminta alamat IP baru dari penyedia layanan internet.
- **Penggunaan Bandwidth yang Lebih Efisien**: Dengan subnetting, kinerja jaringan dapat meningkat, dan lebih banyak perangkat dapat terhubung dengan lebih efisien.

## Kesimpulan Utama

- **Subnetting** adalah strategi keamanan umum yang memungkinkan organisasi untuk membuat jaringan yang lebih kecil di dalam jaringan mereka sendiri.
- Ini meningkatkan efisiensi jaringan dan dapat digunakan untuk membuat **security zones**.
