---
id: Search methods with SIEM tools
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

### Metode Pencarian dengan SIEM Tools

SIEM (Security Information and Event Management) adalah aplikasi yang mengumpulkan dan menganalisis log data untuk memantau aktivitas kritis dalam organisasi. SIEM tools seperti **Splunk** dan **Chronicle** memungkinkan kita untuk mencari, memfilter, dan mengolah data log guna mendukung investigasi keamanan. Berikut adalah metode pencarian pada kedua tools tersebut:

---

## Splunk

![splunk](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zmjvpMvASVuLzBl6p1-KJg_48cf882e1ea14f6ca2f3ceee91e1f2e1_cIW5xo7oKZMktF78z_u5eTeEJANj9wPgAG39QVCd8PDuvdrztqt2N1fJMbJOFms1QoIgAk0YNgHWjR1LQMLg__bhWqMMWmWke6kQmoWLpyxM5eVwNDyW7_2KttYjVSz2fYPCX4arj1TUHKrSfANwCU8?expiry=1736726400000&hmac=3T83TEjHHVYLjkTDeiArJ5V-R-6jhwAiwudfS6U72OI)

Splunk menggunakan **Search Processing Language (SPL)** untuk mencari dan mengambil event dari indeks. Beberapa fitur penting SPL:

### Dasar Pencarian SPL

- **Perintah dasar:**
  Contoh: `index=main fail`

  - `index=main`: Menunjukkan Splunk untuk mengambil event dari indeks bernama `main`.
  - `fail`: Mengembalikan semua event yang mengandung kata _fail_.

- **Manfaat:**
  - Menghemat waktu pencarian.
  - Memberikan hasil spesifik sesuai kebutuhan.

---

### Pipes dalam SPL

- **Fungsi Pipes (|):** Menggabungkan output satu perintah ke input perintah berikutnya.
  Contoh: `index=main fail | chart count by host`

  - **`index=main fail`:** Mencari event di indeks `main` dengan kata _fail_.
  - **`|`:** Mengirim hasil pencarian sebelumnya ke perintah berikutnya.
  - **`chart count by host`:** Membuat grafik berdasarkan jumlah event yang dikelompokkan menurut _host_.

- **Manfaat:**
  - Memungkinkan manipulasi data yang kompleks hanya dengan satu perintah.

---

### Wildcard

- **Wildcard (\*):** Mengganti karakter apa saja dalam string.
  Contoh: `index=main fail*`

  - Mengembalikan hasil seperti _fail_, _failed_, atau _failure_.

- **Tips:** Gunakan tanda kutip ganda untuk pencarian frase spesifik.
  Contoh: `"login failure"` hanya mencari event berisi frase _login failure_.

## Chronicle

![chronicle](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/aM2yKauvThC6hDgvWmzbSQ_0e4167e2b3ab436d92d7cab63fc844e1_7Gwfz8thmYUWWdxjQiQtHM6omUL7OLjOSSD_fShq4yrmkr7sAJs4pBDBJ2Azy26HdkyF3K50mIQEtIqW4FaA2F-eN9G1Ev4WM_Drze0i3-5-Et_l51y9nTnh9eHqQFitE0f5Yzr5YsTzf7qL-MQbDHI?expiry=1736726400000&hmac=i-kr-bkiSaD-S3MYES1YeTSHNN4MiAJn4oG76m1jzlQ)

Chronicle menawarkan dua jenis pencarian untuk menemukan event: **Unified Data Model (UDM) Search** dan **Raw Log Search**. Berikut penjelasannya:

---

### UDM Search

- **Deskripsi:**

  - Pencarian default di Chronicle menggunakan data yang telah diindeks, di-_parse_, dan dinormalisasi.
  - Lebih cepat dibandingkan Raw Log Search karena data sudah terstruktur.

- **Contoh Pencarian UDM:**

  ```
  metadata.event_type = "USER_LOGIN"
  ```

  - **`metadata.event_type`:** Field yang mendeskripsikan tipe event, seperti autentikasi pengguna.
  - **`"USER_LOGIN"`:** Mencari event yang berhubungan dengan login pengguna.

- **Field UDM Umum:**

  - **Entities:** Memberikan konteks perangkat, pengguna, atau proses terkait, seperti _hostname_, _username_, dan IP.
  - **Event Metadata:** Informasi dasar tentang event, termasuk tipe dan _timestamp_.
  - **Network Metadata:** Informasi tentang koneksi jaringan dan protokol.
  - **Security Results:** Hasil keamanan, seperti deteksi virus atau tindakan karantina.

- **Manfaat:**
  - Cepat dalam mencari event tertentu.
  - Cocok untuk investigasi dengan data yang sudah terstruktur.

---

### Raw Log Search

- **Deskripsi:**

  - Mencari data mentah yang belum di-_parse_ atau dinormalisasi.
  - Lebih lambat dari UDM Search karena bekerja dengan log mentah.

- **Contoh Penggunaan:**

  - Mencari _username_, _hash_, atau _filename_ di log mentah.

- **Keunggulan:**
  - Mendukung penggunaan **regular expressions** untuk menyaring pola tertentu.
  - Cocok untuk pencarian detail yang tidak ditemukan di data yang dinormalisasi.

---

### Kesimpulan

- **Splunk:** Gunakan **SPL** untuk pencarian fleksibel, termasuk transformasi data dengan pipes dan wildcard.
- **Chronicle:** Gunakan **UDM Search** untuk pencarian cepat pada data terstruktur, atau **Raw Log Search** untuk analisis log mentah.

---

## Referensi Tambahan

- [Splunk Search Manual](https://docs.splunk.com/Documentation/Splunk/latest/SearchTutorial/WelcometotheSearchTutorial)
- [Chronicle Quickstart Guide](https://cloud.google.com/chronicle/docs)

---
