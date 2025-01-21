---
id: Overview of Suricata
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Suricata Overview

### Apa itu Suricata?

- Suricata adalah **open-source intrusion detection system (IDS)**, **intrusion prevention system (IPS)**, dan alat analisis jaringan.

### Fitur Utama Suricata

1. **Intrusion Detection System (IDS)**:

   - Memantau lalu lintas jaringan dan memberikan alert jika ada aktivitas mencurigakan.
   - Bisa diterapkan sebagai **host-based IDS** untuk memantau aktivitas jaringan pada satu host.

2. **Intrusion Prevention System (IPS)**:

   - Mendeteksi dan memblokir aktivitas atau lalu lintas berbahaya.
   - Memerlukan konfigurasi tambahan, seperti mengaktifkan **IPS mode**.

3. **Network Security Monitoring (NSM)**:
   - Menghasilkan dan menyimpan log lalu lintas jaringan untuk forensik, respons insiden, atau pengujian signature.
   - Bisa menganalisis **live traffic**, file packet capture (PCAP), atau membuat full/conditional packet capture.

---

### Rules (Signatures) di Suricata

- **Rules (atau signatures)** digunakan untuk mendeteksi pola, perilaku, atau kondisi yang menunjukkan aktivitas berbahaya.
- Komponen utama signature:
  1. **Action**: Tindakan yang dilakukan saat signature cocok (contoh: alert, pass, drop, reject).
  2. **Header**: Informasi lalu lintas seperti IP, port, protokol, dan arah lalu lintas.
  3. **Rule Options**: Opsi tambahan untuk menyesuaikan signature.

#### Contoh Signature

![example](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sUAYMHVdQ-2IJCnBysJmzg_c3deef0b2a6c454fbc39b674cc0bc9f1_CS_R-138_Suricata-signature.png?expiry=1736640000000&hmac=6qosP1XqLxseT7JVmxHEuaoB4D-LSrNOHcSE1M8YG4Q)

```
Action | Header | Rule Options
```

- **Catatan**: Urutan pada rule options memengaruhi arti dan hasil rule tersebut.

#### Custom Rules

- **Custom rules** diperlukan untuk menyesuaikan deteksi dengan kebutuhan spesifik organisasi.
- Manfaat:
  - Mengurangi **false positives**.
  - Meningkatkan visibilitas dan relevansi deteksi.

---

### File Konfigurasi

- **suricata.yaml**: File konfigurasi utama untuk Suricata.
- Fungsinya untuk mengatur bagaimana IDS berinteraksi dengan lingkungan.

---

### Log Files

1. **eve.json**:

   - Format standar Suricata dengan detail metadata dan event.
   - Cocok untuk analisis mendalam dan integrasi ke SIEM.
   - Memiliki **flow_id** untuk menghubungkan log terkait.

2. **fast.log**:
   - Format log lama dengan informasi minimal (IP, port, dll.).
   - Tidak cocok untuk investigasi insiden atau threat hunting.

**Perbedaan Utama**:

- **eve.json**: Log detail untuk analisis mendalam.
- **fast.log**: Log sederhana untuk kebutuhan dasar.

---

### Takeaways

- **Suricata** menawarkan fleksibilitas sebagai IDS, IPS, dan NSM.
- Memahami cara menulis dan mengkonfigurasi rules akan meningkatkan kemampuan deteksi dan visibilitas jaringan.
- Praktikkan pembuatan custom rules dan konfigurasi untuk meningkatkan keahlian Anda.

---

### Referensi Tambahan

- [Suricata User Guide](https://suricata.io/docs/)
- Webinar dan artikel tentang rule management, performance analysis, dan threat hunting.
