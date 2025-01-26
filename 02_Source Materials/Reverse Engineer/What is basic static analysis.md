---
id: What is basic static analysis
aliases: []
tags:
  - malware_analysis
---

## Apa itu Static Analysis

- Dikenal juga dengan Initial Malware Triage
- Mengumpulkan informasi basic dari malware
- Melihat sekilas dari kode program
- Mencari compiler yang digunaakan, dll

## Bagian Laporan(Report)

- Filename
- File Size/date
- Compiler/packer: untuk mencompile dan mengemas atau mengompress file
- MD5 Hash: algoritma hash kriptografi yang dirancang untuk menghasilkan nilai hash 128-bit
- SHA1 Hash: menghasilkan nilai 160-bit, digunakan untuk SSL
- SHA256 Hash: menghasilkan nilai 256-bit, digunakan untuk digital signature, bitcoin, TSL/SSL
- **Strings of Interest**: merujuk pada urutan karakter yang dapat dibaca manusia (readable text) yang ditemukan dalam file atau program yang sedang dianalisis.
- Import
- Export
- File created/modifed/deleted
- Registry Keys Created/Modifed/Deleted
- Networking
- OSR(Open Source Resources)
- Analysis Notes
