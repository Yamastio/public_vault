---
id: The containment, eradication, and recovery phase of the lifecycle
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## **Rangkuman: Fase Ketiga dalam Incident Response Lifecycle**

### **Gambaran Umum**
- Fase ini mencakup langkah-langkah **containment**, **eradication**, dan **recovery**.
- Langkah-langkah tersebut **saling berhubungan**:
  - **Containment** mendukung eradication.
  - **Eradication** mendukung recovery.
- Fase ini juga terintegrasi dengan fungsi inti **NIST Cybersecurity Framework**, yaitu **Respond** dan **Recover**.

---

### **Langkah-Langkah Fase Ketiga**
1. **Containment (Pembatasan)**
   - **Tujuan**: Membatasi dan mencegah kerusakan lebih lanjut akibat insiden.
   - **Strategi containment** diatur dalam **incident response plans**:
     - Contoh: Untuk insiden malware, sistem yang terkena diisolasi dengan **memutuskan koneksi jaringan**.
     - Langkah ini mencegah malware menyebar ke sistem lain.
   - **Hasil**: Membatasi insiden pada area terdampak untuk mengurangi kerusakan lebih lanjut.

2. **Eradication (Penghapusan)**
   - **Tujuan**: Menghapus semua elemen insiden dari sistem yang terpengaruh.
   - Contoh tindakan:
     - Melakukan **vulnerability testing**.
     - Mengaplikasikan **patch** pada kerentanan yang terkait ancaman.

3. **Recovery (Pemulihan)**
   - **Tujuan**: Mengembalikan sistem yang terdampak ke **operasi normal**.
   - **Dampak insiden**: Operasi bisnis dan layanan utama bisa terganggu.
   - Contoh tindakan pemulihan:
     - **Reimaging** sistem yang terkena.
     - **Reset password**.
     - Mengatur ulang **firewall rules** atau konfigurasi jaringan.

---

### **Catatan Penting**
- **Siklus insiden bersifat siklis**:
  - Insiden baru bisa muncul atau terkait insiden sebelumnya.
  - Tim keamanan mungkin harus kembali ke fase sebelumnya untuk investigasi tambahan.

### **Selanjutnya**
Fase berikutnya akan membahas **tahap akhir dari incident response lifecycle**.
