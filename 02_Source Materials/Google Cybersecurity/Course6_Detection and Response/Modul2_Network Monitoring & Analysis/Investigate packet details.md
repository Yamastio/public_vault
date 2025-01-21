---
id: Investigate packet details
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan: Investigasi Detail Paket

### Pengantar
- Packet analysis adalah keterampilan penting untuk mengidentifikasi aktivitas mencurigakan di jaringan.
- Wireshark adalah alat analisis protokol jaringan yang digunakan untuk memvisualisasikan dan menyaring paket-paket dari file tangkapan paket (p-caps).

### Internet Protocol (IP)
- **IPv4 dan IPv6** adalah dua versi IP yang digunakan untuk mengarahkan dan mengalamatkan paket data.
- **IPv4 Header Fields** (13 fields):
![ipv4](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/jkb0TBrPQSq9YoCeruRfqA_e1ec815e1edd4447a9a51b7f8945ccf1_7Fe1r5PP-rO933_0njaasi_PLYxnCK70uwxT7ZVgtLukfU1L_3B4ppP4aiLOiZ1QNlZCuuLku28h-mpQ5lEnQKly8HIeoDkaEvqkdh4Xbb_U9ba52JscXUcrmQFcluGPBPqNqA1v_gYZwv_JqR4di7niNF2R5uy2JBR0r-QshhE6zOIghv4lUCWa96872A?expiry=1736208000000&hmac=SW0aF7D8HXlpfZrWVpDvjtvpmI6NKldYaWCo2my0MKY)

  - Contoh: `Version`, `IHL`, `Total Length`, `TTL`, `Protocol`, `Source Address`, dll.
- **IPv6 Header Fields** (8 fields):
![ipv6](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/i8ZlXBWcQnKMc9AvaOlTrg_9ae604f634bc4ea3b0bced51911d32f1_XjvmdLkZuzfhKQ0zQ_4RnCZGNxP0FDCtB0i8iwWtu30GL05Ziixkcd3YNSK8ng5tiu3X3XVOypCPywtGP01diUAvVWEkjwGWk7E_4fpFZdntBgohToxkS5cNsyZtqKsRCmssQUmWlH8Xhn2oJKG55Kv0-CUjA8Kj3yhZXTWbjjV4pYcCH9EUwPWpyFnhCQ?expiry=1736208000000&hmac=_U5ePWiyrVnGUSMqxfx8mHvbk-qhget9McWxQfLb0f4)

  - Contoh: `Version`, `Traffic Class`, `Payload Length`, `Hop Limit`, `Source Address`, dll.

### Wireshark
![wireshark](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/SrU-DA-pR1eTtgJe4lBOjQ_c841a1d648aa40069fe7e47e84ea79f1_CS_R-125_Wireshark-homepage.png?expiry=1736208000000&hmac=6Dw227-8Qa4eXdgt5ZUz8T5wP_sfIorPehPkAGbxWA8)

- **Display Filters**:
  - Berguna untuk menyaring paket berdasarkan protokol, IP, port, atau properti lainnya.
  - **Operator Perbandingan**:
    - Equal (`==` / `eq`), Not equal (`!=` / `ne`), Greater than (`>` / `gt`), dll.
  - **Operator Contains**:
  ![containts](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/U-VFvCZpR-C7DiBud3CJ6Q_3d58fbc8790a4163b1fbd8d6689cf0f1_CS_R-125_packet-capture.png?expiry=1736208000000&hmac=MwLlQ0RKs2DPCZrxjYXiYLLaijhnOmjHAjzcFZ_YlM4)
    - Menemukan string teks tertentu dalam paket.
  - **Operator Matches**:
    - Menyaring paket menggunakan pola ekspresi reguler (regex).

### Filter Populer
![filterToolbar](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/S2HoKdS_TnS0idDiU9XbJw_cb303cb11f2f45db944a6b22cbf3b4f1_ADA_R-125_DNS.png?expiry=1736208000000&hmac=hUnrI9kx5-DFVVV8FRpLQ7eDcweQMFtk81F2uS2dFXM)
1. **Protokol**: Contoh filter: `dns`, `http`, `ftp`, `ssh`, dll.
2. **IP Address**:
   - Filter untuk IP tertentu: `ip.addr == 172.21.224.2`
   - Filter untuk sumber: `ip.src == 10.10.10.10`
   - Filter untuk tujuan: `ip.dst == 4.4.4.4`
3. **MAC Address**:
   - Contoh filter: `eth.addr == 00:70:f4:23:18:c4`
4. **Port**:
   - UDP: `udp.port == 53`
   - TCP: `tcp.port == 25`

### Fitur Follow Streams
![followStream](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qGiuzTybTNyYJXCUSuSStA_2353ba616b0c404d9b3d6df3af1fdef1_CS_R-125_dialog-box.png?expiry=1736208000000&hmac=1oOjcRFBKmlA1Lx3NRr04nOrdc9Rqv1W2zFVlFKEH3s)
- Berguna untuk menganalisis percakapan antar perangkat dalam protokol tertentu.
- Misalnya: Melihat permintaan dan respons dalam percakapan HTTP.

### Poin Utama
- **Packet analysis** adalah keterampilan penting dalam cybersecurity.
- Gunakan filter Wireshark untuk menyederhanakan investigasi.
- Praktikkan analisis paket untuk memperdalam pemahaman.

### Sumber Tambahan
- Jelajahi **[Panduan Pengguna Wireshark Resmi](https://www.wireshark.org/docs/)** untuk fitur lebih lanjut.
