---
id: Identity and access management
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Rangkuman: Identity and Access Management (IAM)

**Prinsip Keamanan Dasar:**
- **Prinsip Least Privilege**: Pengguna hanya diberikan akses minimum yang diperlukan untuk menyelesaikan tugas.
- **Separation of Duties**: Pengguna tidak diberikan izin yang dapat disalahgunakan dalam sistem.

Kedua prinsip ini mendukung satu sama lain untuk membatasi akses yang berlebihan pada satu individu dan mencegah penyalahgunaan.

**Identity and Access Management (IAM):**
- **IAM** adalah sekumpulan proses dan teknologi yang membantu organisasi mengelola identitas digital di lingkungan mereka.
- Tujuan utama IAM adalah untuk **memverifikasi identitas pengguna**, **menentukan hak akses**, dan **melacak aktivitas pengguna** dalam sistem.
- Kedua model IAM dan AAA bertujuan untuk **mengautentikasi pengguna**, **menentukan hak akses mereka**, dan **melacak aktivitas mereka**.

**Proses Autentikasi Pengguna:**
- Pengguna harus membuktikan identitas mereka menggunakan:
  - **Knowledge** (sesuatu yang diketahui pengguna)
  - **Ownership** (sesuatu yang dimiliki pengguna)
  - **Characteristic** (sesuatu yang dimiliki pengguna)
- Teknologi seperti **Single Sign-On (SSO)** dan **Multi-Factor Authentication (MFA)** sering digunakan untuk mengautentikasi pengguna.

**User Provisioning:**
- **Provisioning** adalah proses untuk membuat dan memelihara identitas digital pengguna.
- **Deprovisioning** adalah proses menghapus akses ketika seorang pengguna tidak lagi memerlukannya.

**Granting Authorization:**
- Setelah pengguna terautentikasi, hak akses diberikan menggunakan tiga framework utama:
  1. **Mandatory Access Control (MAC)**: Akses diberikan oleh otoritas pusat berdasarkan kebutuhan.
  ![MAC](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/AxrWM2DLTSunrTWYAtwc4Q_49abc18d6b1c48748e222045153881f1_image3.png?expiry=1736035200000&hmac=I15C30wkmRDmOiNrB5nCKqr6xOOLf7dihxpF67IPO7M)
  2. **Discretionary Access Control (DAC)**: Pemilik data memutuskan siapa yang memiliki akses.
  ![DAC](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LHnKRh7ISfCc379NmCXMlw_5c65648b2a77437ab6998e6b978afcf1_image2.png?expiry=1736035200000&hmac=NpMYTrWXwzDHO6o3c81rjf_40Dzy8gO3-Lh6SOH78fY)
  3. **Role-Based Access Control (RBAC)**: Akses diberikan berdasarkan peran pengguna dalam organisasi.
  ![RBAC](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1EBo9jW3TGW_7Hulb3cUpA_16c10e1f1de94b3c95d88760722733f1_image1.png?expiry=1736035200000&hmac=fbxhSQ_97twfM8ocsSXMKG4JnejnmB-RuRiKUThc1mM)

**Teknologi Kontrol Akses:**
- IAM dan AAA sering menggunakan **teknologi kontrol akses** yang memungkinkan pengelolaan hak akses dengan cepat dan otomatis.
- Teknologi ini mencakup **direktori pengguna**, **sistem otorisasi**, dan **sistem audit** yang dapat dikustomisasi atau menggunakan solusi pihak ketiga.

**Takeaways:**
- **IAM** dan **AAA** adalah kerangka kerja yang umum untuk menerapkan prinsip **least privilege** dan **separation of duties**.
- Sebagai **security analyst**, memahami dan bekerja dengan kedua model ini sangat penting untuk membantu organisasi mencapai tujuan keamanannya.

**Sumber Tambahan:**
- **IDPro** adalah organisasi profesional yang berbagi pengetahuan penting dalam industri IAM.
