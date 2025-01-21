---
id: Overview of detection tools
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan: Detection Tools (IDS, IPS, EDR)

**Mengapa Detection Tools Penting?**
- Detection tools seperti sistem keamanan rumah, tetapi untuk jaringan dan sistem organisasi.
- Fungsi utama: **memantau, mendeteksi, dan memberi peringatan** atas aktivitas mencurigakan.
- Memberikan **kesadaran situasional** kepada tim keamanan untuk segera merespons potensi ancaman.

---

**Perbandingan IDS, IPS, dan EDR**
| **Kemampuan**              | **IDS** | **IPS** | **EDR** |
|----------------------------|---------|---------|---------|
| Mendeteksi aktivitas berbahaya | ✓       | ✓       | ✓       |
| Mencegah intrusi            | N/A     | ✓       | ✓       |
| Mencatat aktivitas          | ✓       | ✓       | ✓       |
| Membuat peringatan          | ✓       | ✓       | ✓       |
| Analisis perilaku           | N/A     | N/A     | ✓       |

---

### **IDS (Intrusion Detection System)**
- **Fungsi:**
  - Memantau aktivitas sistem dan jaringan.
  - Mendeteksi aktivitas mencurigakan dan memberi peringatan.
  - **Tidak menghentikan ancaman secara otomatis.**

- **Contoh penggunaan:**
  - Mengirim peringatan jika ada login mencurigakan dari IP tidak dikenal.

- **Contoh tools:**
  - Zeek, Suricata, Snort®, Sagan.

- **Kategori Deteksi IDS:**
  1. **True Positive:** Ancaman terdeteksi dengan benar.
  2. **True Negative:** Tidak ada ancaman dan tidak ada peringatan.
  3. **False Positive:** Peringatan salah, tidak ada ancaman sebenarnya.
  4. **False Negative:** Ancaman ada tetapi tidak terdeteksi (paling berbahaya).

---

### **IPS (Intrusion Prevention System)**
- **Fungsi:**
  - Mirip IDS, tetapi juga menghentikan ancaman secara otomatis.
  - Dapat memblokir lalu lintas berbahaya, misalnya dengan mengubah ACL (Access Control List) di router.

- **Contoh tools:**
  - Suricata, Snort, Sagan (tools ini bisa berfungsi sebagai IDS atau IPS).

---

### **EDR (Endpoint Detection and Response)**
- **Fungsi:**
  - Memantau, mencatat, dan menganalisis aktivitas endpoint.
  - Melakukan **analisis perilaku** menggunakan AI/ML untuk mendeteksi pola ancaman.
  - Menggunakan otomatisasi untuk menghentikan ancaman tanpa intervensi manual.

- **Contoh penggunaan:**
  - Memblokir proses mencurigakan yang berjalan di workstation pengguna.

- **Contoh tools:**
  - Open EDR®, Bitdefender™ EDR, FortiEDR™.

---

### **Kesimpulan Utama**
- IDS, IPS, dan EDR adalah alat penting untuk mendeteksi, mencatat, memberi peringatan, dan menghentikan aktivitas berbahaya.
- Pemahaman perbedaan dan fungsi tiap alat ini membantu organisasi memilih alat yang tepat untuk melindungi lingkungan mereka.
