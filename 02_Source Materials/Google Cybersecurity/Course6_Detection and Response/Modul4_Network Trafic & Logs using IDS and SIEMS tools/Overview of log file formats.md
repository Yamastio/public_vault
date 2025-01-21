---
id: Overview of log file formats
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Rangkuman tentang Format File Log

### Pengantar
- **Log** mencatat kejadian di jaringan atau sistem.
- Penting untuk memahami format log yang berbeda agar dapat mengidentifikasi aktivitas mencurigakan atau berbahaya.
- Format log yang dibahas: **JSON**, **Syslog**, **XML**, **CSV**, dan **CEF**.

---

### JSON (JavaScript Object Notation)
- **Karakteristik**:
  - **Ringan** dan **mudah dibaca**.
  - Digunakan di **teknologi web** dan **cloud environments**.
  - Berbasis pada sintaks JavaScript.
- **Komponen utama**:
  - **Key-value pairs**: Contoh: `"Alert": "Malware"`.
  - **Commas**: Memisahkan data, contoh: `"Alert": "Malware", "Severity": 10`.
  - **Double quotes**: Mengapit string, contoh: `"User": "Admin"`.
  - **Curly brackets**: Menandai objek, contoh: `{ "id": "1234" }`.
  - **Square brackets**: Menandai array, contoh: `["Admin", "User"]`.

---

### Syslog
- **Standar logging dan transmisi data**.
- Digunakan untuk:
  - **Protokol**: Mengirim log ke server terpusat (port 514 untuk plaintext, 6514 untuk enkripsi).
  - **Layanan**: Menerima dan meneruskan log.
  - **Format log**: Umumnya digunakan pada sistem Unix.
- **Komponen**:
  - **Header**: Berisi timestamp, hostname, nama aplikasi, dan ID pesan.
  - **Structured-data**: Informasi tambahan dengan key-value pairs.
  - **Message**: Detail tentang kejadian.
  - **Priority (PRI)**: Indikator tingkat urgensi (angka lebih rendah = lebih mendesak).
- **Contoh log**:
  ```plaintext
  <236>1 2022-03-21T01:11:11.003Z virtual.machine.com evntslog - ID01 [user@32473 iut="1" eventSource="Application" eventID="9999"] This is a log entry!
  ```

---

### XML (eXtensible Markup Language)
- **Format untuk menyimpan dan mengirim data** (digunakan pada sistem Windows).
- **Komponen utama**:
  - **Tags**: Penanda awal dan akhir data, contoh: `<tag>data</tag>`.
  - **Elements**: Gabungan tag dan data.
  - **Attributes**: Informasi tambahan di dalam tag, contoh: `<Data Name='Username'>Admin</Data>`.
- **Contoh**:
  ```xml
  <Event>
      <EventID>4688</EventID>
      <Version>5</Version>
  </Event>
  ```

---

### CSV (Comma Separated Value)
- **Menggunakan koma** untuk memisahkan nilai.
- **Penting**: Memahami urutan data karena field name sering kali tidak disertakan.
- **Contoh**:
  ```plaintext
  2009-11-24T21:27:09.534255,ALERT,192.168.2.7,1041,x.x.250.50,80,TCP,ALLOWED,1:2001999:9,"ET MALWARE BTGrab.com Spyware Downloading Ads",1
  ```

---

### CEF (Common Event Format)
- **Struktur log**: Menggunakan **key-value pairs**.
- **Format utama**:
  - `CEF:Version|Device Vendor|Device Product|Device Version|Signature ID|Name|Severity|Extension`.
- **Komponen**:
  - **Versi**: `CEF:1`.
  - **Detail perangkat**: Vendor, produk, versi.
  - **Informasi kejadian**: ID tanda tangan, nama, tingkat keparahan.
  - **Extension**: Data tambahan dalam key-value pairs.
- **Contoh log**:
  ```plaintext
  Sep 29 08:26:10 host CEF:1|Security|threatmanager|1.0|100|worm successfully stopped|10|src=10.0.0.2 dst=2.1.2.2 spt=1232
  ```

---

### Poin Penting
- **Tidak ada standar universal** dalam format log.
- Memahami berbagai format log penting untuk mendukung investigasi keamanan.
- Referensi tambahan:
  - **The Syslog Protocol**: Detail tentang protokol syslog.
  - **Test Data Generator Tool**: Untuk mencoba membuat log.
  - **Date and Time on the Internet**: Format timestamp.
