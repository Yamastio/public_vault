---
id: "Exemplar: Explore signatures with Suricata"
aliases: []
tags: []
---

Tags:[[google_cybersecurity]]

### Aktivitas: Jelajahi Signature dengan Suricata

#### Ringkasan Aktivitas

- **Tujuan**: Mengenal lebih dalam tentang Suricata, menciptakan custom rule, memicu alert, dan menganalisis log yang dihasilkan.
- **Suricata**: Tool untuk memantau antarmuka jaringan, menerapkan aturan pada paket, dan memutuskan apakah paket menghasilkan alert, diblokir, atau diteruskan.
- **Log yang Dianalisis**:
  - **`fast.log`**: Cepat memeriksa alert, tapi kurang detail.
  - **`eve.json`**: Log utama yang berisi informasi detail alert dan telemetri jaringan dalam format JSON.

---

### Tugas 1: Memeriksa Custom Rule di Suricata

1. **Lokasi file**:

   - File rule: `/home/analyst/custom.rules`
   - Perintah: `cat custom.rules`

2. **Komponen Custom Rule**:

   - **Action**:
     - Contoh: `alert` → Memberi alert jika kondisi terpenuhi.
     - Alternatif:
       - `drop`: Blokir lalu lintas dan beri alert.
       - `pass`: Izinkan lalu lintas melewati interface.
       - `reject`: Blokir lalu lintas dan kirimkan paket reset TCP.
   - **Header**:
     - Contoh: `http $HOME_NET any -> $EXTERNAL_NET any`
     - Keterangan:
       - `http`: Hanya untuk protokol HTTP.
       - `$HOME_NET`: Jaringan internal.
       - `$EXTERNAL_NET`: Jaringan eksternal.
       - `any`: Semua port.
   - **Rule Options**:
     - `msg:"GET on wire"` → Teks alert.
     - `flow:established,to_server` → Paket dari client ke server.
     - `content:"GET"; http_method` → Cari metode HTTP GET.
     - `sid:12345` → ID signature unik.
     - `rev:3` → Revisi signature ke-3.

3. **Penjelasan Rule**:
   - Rule ini memicu alert jika ada metode HTTP GET pada paket HTTP dari jaringan internal menuju jaringan eksternal.

---

### Tugas 2: Memicu Custom Rule di Suricata

1. **Sebelum Memulai**:

   - Periksa file log: `ls -l /var/log/suricata`
   - Awalnya direktori `/var/log/suricata` kosong.

2. **Menjalankan Suricata**:

   - Perintah:
     ```bash
     sudo suricata -r sample.pcap -S custom.rules -k none
     ```
     - **`-r sample.pcap`**: Memproses file `sample.pcap` sebagai lalu lintas jaringan.
     - **`-S custom.rules`**: Menggunakan aturan di `custom.rules`.
     - **`-k none`**: Menonaktifkan pengecekan checksum.

3. **Setelah Menjalankan**:
   - Periksa kembali file log: `ls -l /var/log/suricata`
   - File baru: `fast.log`, `eve.json`, dll.

---

### Kesimpulan

- Suricata memproses lalu lintas jaringan dan menghasilkan alert sesuai aturan.
- **Log Penting**:
  - `fast.log`: Mudah dan cepat untuk pengecekan kualitas.
  - `eve.json`: Detail lengkap untuk analisis mendalam.
- **Langkah Selanjutnya**:
  - Tambahkan custom rules lain.
  - Analisis output log untuk memahami pola lalu lintas dan alert.
