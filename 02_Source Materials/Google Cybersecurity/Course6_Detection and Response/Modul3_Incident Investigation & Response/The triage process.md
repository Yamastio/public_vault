---
id: The triage process
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Rangkuman: Proses Triage dalam Keamanan Siber**

### **Apa Itu Triage?**
- Triage adalah proses **prioritisasi insiden** berdasarkan tingkat kepentingan atau urgensi.
- Membantu tim keamanan:
  - Mengevaluasi dan memprioritaskan **security alerts**.
  - Mengalokasikan sumber daya dengan efektif.
  - Menangani isu-isu kritis terlebih dahulu.

---

### **Tiga Langkah Proses Triage**
1. **Receive and Assess (Menerima dan Menilai)**
   - **Langkah awal**: Menerima alert dari sistem seperti IDS (Intrusion Detection System).
   - **Analisis alert**:
     - Apakah alert **false positive** atau ancaman nyata?
     - Apakah alert ini pernah terjadi sebelumnya, dan bagaimana penyelesaiannya?
     - Apakah alert disebabkan oleh **known vulnerability**?
     - Seberapa parah tingkat keparahan alert?

2. **Assign Priority (Menentukan Prioritas)**
   - **Faktor-faktor penentuan prioritas**:
     - **Functional Impact**: Dampak pada fungsi sistem atau layanan.
     - **Information Impact**: Kerahasiaan, integritas, dan ketersediaan data yang terpengaruh.
     - **Recoverability**: Kemungkinan pemulihan dan seberapa layak sumber daya digunakan untuk itu.
   - **Catatan**: Banyak alert sudah memiliki tingkat prioritas yang ditentukan sebelumnya.

3. **Collect and Analyze (Mengumpulkan dan Menganalisis)**
   - Melakukan analisis menyeluruh, termasuk:
     - Mengumpulkan bukti.
     - Melakukan riset eksternal.
     - Mendokumentasikan proses investigasi.
   - **Hasil analisis** dapat menentukan apakah insiden perlu eskalasi ke analis level dua atau manajer.

---

### **Manfaat Triage**
- **Manajemen Sumber Daya**:
  - Memfokuskan sumber daya pada ancaman yang paling membutuhkan perhatian.
  - Mengurangi waktu respons dan menghindari pemborosan pada tugas prioritas rendah.
- **Pendekatan Terstandarisasi**:
  - Menggunakan dokumentasi proses seperti **playbooks** untuk memastikan setiap alert diolah secara konsisten.
  - Hanya alert yang valid yang diteruskan untuk investigasi lebih lanjut.

---

### **Key Takeaways**
- **Triage penting** untuk memastikan insiden keamanan ditangani dengan efisien dan prioritas sesuai urgensi.
- Sebagai profesional keamanan, keterampilan triage membantu Anda merespons dan menyelesaikan insiden secara efektif.
- Proses triage memberikan manfaat besar dalam **pengelolaan sumber daya** dan **standarisasi penanganan insiden**.
