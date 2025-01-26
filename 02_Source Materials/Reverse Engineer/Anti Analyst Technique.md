---
id: Anti Analyst Technique
aliases: []
tags:
  - malware_analysis
---

## File Packing

- File dimodifikasi sedemikian rupa untuk dikompres secara berurutan untuk mengaburkan file, keuntungan untuk malware antara lain:
  - Menyembunyikan malware hashes dan banyak strings
  - Lebih susah untuk antivirus mendeteksi
  - Lebih susah untuk malware analisis untuk melakukan analisis via pembongkaran dan debugging
- Alat untuk mendeteksi packing:
  - PEiD, PEView, Strings
  - Bytehist

## Encoding and encryption

- malware biasanya menggunakan untuk encoding dan encryption untuk membingungkan
- encoding sepertii base64, mudah di reverse, tapi enkripsi seperti AES bisa lebih susah untuk di reverse.
- encoding skema bisa diakses publik, kunci untuk enkrpsi mungkin tersedia atau tidak
- Ada beberapa jalan malware menggunakan encoding dan encryption, beberapa mengandung:
  - strings
  - File pada host yang terinfeksi
  - Lalu lintas jaringan
- alat untuk mengidentifikasi pola encoding atau enkripsi:
  - Notepad ++
  - CyberChef

## Stack-built strings

- String yang dibuat sesuai kebutuhan

  - Didalam malware, mungkin di hardcode sebagai single karakter
  - Ketika berjalan, karakter biasanya digabungkan untuk menjadi string

- Keuntungan:
  - Tidak akan dilihat di string list
  - Menghindari antivirus deteksi
  - Lebih susah untuk dianalisis

## Anti-disassembly

Susah di reverse engineering, beberapa teknik:

- Kondisional jump instuction (jika nol lompat, jika tidak nol tidak lompat) mengarah ke kode yang sama
- Junk code insertion
- Return pointer abuse
- Impossible dissasembly

## Anti debuggin teknik

- teknik untuk mencegah debugging
- Contoh:
  - Menggunakan windows APIs untuk mencegah debugging
  - GettickCount
  - Deteksi hardware dan software breakpoint
  - Detection of debuggers lib
  - Checking if various flags are set
  - Exception handling
- alat:
  - Immunity and OllyDbg plugins
  - IDA Pro plugins
  - Modifying code

## VM Deteksi

- Malwar bisa mendetksi jika malware dijalankan di VM
- Teknik:
  - Check registry
  - Mencari host untuk spesifik file
  - Melihat proses yang berjalan
  - Mengambil Mac Address
  - Memverifikasi hardware
