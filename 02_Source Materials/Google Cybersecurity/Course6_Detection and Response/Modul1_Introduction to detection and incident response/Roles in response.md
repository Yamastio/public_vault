---
id: Roles in response
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Ringkasan Peran dalam Incident Response

**Framework NIST Incident Response Lifecycle**
1. **Preparation**
2. **Detection and Analysis**
3. **Containment, Eradication, and Recovery**
4. **Post-incident Activity**

### **Tim CSIRT (Computer Security Incident Response Team)**
CSIRT bertugas menangani insiden keamanan, dengan fokus pada **command, control, dan communication**.
- **Command:** Kepemimpinan untuk mengarahkan respons.
- **Control:** Pengelolaan aspek teknis seperti alokasi sumber daya dan penugasan.
- **Communication:** Menjaga pemangku kepentingan tetap terinformasi.

**Peran Utama di CSIRT:**
1. **Security Analyst:**
   - Memantau ancaman keamanan.
   - Melakukan analisis akar penyebab dan eskalasi ancaman kritis.
   - Menyelesaikan atau meneruskan masalah ke **Technical Lead**.

2. **Technical Lead:**
   - Mengelola aspek teknis insiden, seperti patching atau pembaruan perangkat lunak.
   - Menentukan akar penyebab dan strategi untuk containment, eradication, serta recovery.
   - Berkolaborasi dengan tim lain untuk memastikan prioritas bisnis tetap berjalan.

3. **Incident Coordinator:**
   - Mengoordinasikan komunikasi lintas departemen (HR, legal, PR, dll.).
   - Menjaga komunikasi yang jelas selama insiden berlangsung.

**Peran Lain:**
- Communication Lead, Legal Lead, Planning Lead, dll., tergantung struktur organisasi.

---

### **Tim SOC (Security Operations Center)**
SOC bertugas memantau jaringan, sistem, dan perangkat untuk ancaman keamanan. Ini merupakan bagian dari tim **blue team**, dengan struktur bertingkat:

![SOC](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CMDszNSgSryqbipKuGOU2Q_222b5865df5f4a72a785cd94279d99f1_CkqInM-0iDHKapM_2jS_68ZBhx11oR2GR_fCveMT5EI39E4h_dsAwBstgiRAXmj-mLFWXeOLNnSpBeMpDrEOiP9N8P9efbhWwLqNx-nDZFmoa6ue7SuqH0iUjmnMPWmpEcZPjKUY7ONnH6qkmt7wqF1XpuxPDe1zCbwGriZcyQRpSru_CG-tzvFvMDe5cg?expiry=1736121600000&hmac=-zpUQ5FVtPbKsy2JtPJqv14TD-qak2TyZk4f6KxYvJU)

**Struktur SOC:**
1. **Tier 1 SOC Analyst (L1):**
   - Memantau dan memprioritaskan alert berdasarkan tingkat kritis.
   - Membuat dan menutup tiket alert menggunakan sistem tiket.
   - Meneruskan tiket ke Tier 2 atau Tier 3.

2. **Tier 2 SOC Analyst (L2):**
   - Menangani tiket yang diteruskan oleh L1 dan menyelidiki lebih dalam.
   - Melakukan konfigurasi dan penyempurnaan alat keamanan.
   - Melaporkan ke SOC Lead.

3. **Tier 3 SOC Lead (L3):**
   - Mengelola operasi tim.
   - Melakukan teknik deteksi lanjutan seperti analisis forensik malware.
   - Melaporkan temuan kepada SOC Manager.

4. **SOC Manager:**
   - Mengelola rekrutmen, pelatihan, dan evaluasi tim SOC.
   - Menyusun metrik performa dan laporan terkait insiden, compliance, serta audit.
   - Menyampaikan temuan kepada manajemen eksekutif.

**Peran Khusus di SOC:**
- **Forensic Investigators:** Mengumpulkan dan menganalisis bukti digital terkait insiden.
- **Threat Hunters:** Mendeteksi dan menganalisis ancaman siber baru menggunakan **threat intelligence**.

---

### **Poin Penting**
- **Kerja tim:** Penting untuk merespons insiden dengan efektif.
- **Struktur organisasi:** Membantu memahami tanggung jawab dan jalur eskalasi saat insiden terjadi.
- **Kolaborasi lintas tim:** Menyediakan berbagai perspektif dan solusi kreatif untuk tantangan keamanan.

---

**Referensi:**
- The Security Operations Ecosystem
- Cyber Career Pathways Tool
- Hacking Google: Episode 2 (Detection and Response)
