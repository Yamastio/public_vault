---
id: Automated Task
aliases: []
tags: []
---

Tags: [[linux_fundamental]]

## Penjelasan Tentang Automated Task dan Cron Jobs di Linux

#### **Apa Itu Automated Task di Linux?**

Automated task adalah proses menjalankan skrip, perintah, atau aplikasi secara otomatis tanpa campur tangan pengguna. Tujuan utama adalah untuk menghemat waktu, menghindari kesalahan manual, dan memastikan tugas berjalan sesuai jadwal.

Contohnya:

- Membackup data setiap malam.
- Membersihkan file sementara (temporary files).
- Menjalankan skrip untuk pemeliharaan sistem.
- Memantau server atau aplikasi.

#### **Apa Itu Cron dan Cron Jobs?**

- **Cron** adalah layanan (daemon) bawaan di sistem Linux yang digunakan untuk menjalankan tugas otomatis pada waktu tertentu.
- **Cron jobs** adalah tugas yang dijadwalkan di sistem Linux untuk dieksekusi oleh cron.

Cron bekerja dengan membaca file konfigurasi yang disebut **crontab** (cron table), di mana pengguna menentukan:

1. **Waktu** kapan tugas akan dijalankan.
2. **Perintah/Skrip** yang akan dieksekusi.

---

### **Cara Kerja Cron Jobs**

#### **Crontab File**

File **crontab** adalah tempat Anda mendefinisikan tugas otomatis Anda. Setiap pengguna di sistem Linux memiliki file crontab masing-masing.

Struktur dasar entri di crontab:

```
* * * * * /path/to/command
| | | | |
| | | | +--- Hari dalam seminggu (0 - 7) (Minggu = 0 atau 7)
| | | +----- Bulan (1 - 12)
| | +------- Tanggal (1 - 31)
| +--------- Jam (0 - 23)
+----------- Menit (0 - 59)
```

Contoh:

```
30 2 * * * /usr/bin/python3 /home/user/backup.py
```

Penjelasan:

- **30**: Menit ke-30.
- **2**: Jam 2 pagi.
- **\***: Setiap hari, setiap bulan, setiap hari dalam seminggu.
- Skrip `backup.py` akan dijalankan setiap hari pukul **02:30 pagi**.

---

### **Mengelola Cron Jobs**

#### 1. **Melihat Cron Jobs**

Gunakan perintah:

```bash
crontab -l
```

Untuk pengguna root:

```bash
sudo crontab -l
```

#### 2. **Menambahkan Cron Job**

Edit crontab:

```bash
crontab -e
```

Atau untuk pengguna root:

```bash
sudo crontab -e
```

Tambahkan entri baru sesuai format. Contoh:

```bash
0 6 * * 1 /home/user/weekly_backup.sh
```

Tugas di atas akan menjalankan `weekly_backup.sh` setiap **Senin pukul 6 pagi**.

#### 3. **Menghapus Cron Job**

- Buka crontab dengan `crontab -e`.
- Hapus baris cron job yang ingin dihapus.
- Simpan dan keluar.

---

### **Contoh Penggunaan Cron Job**

#### Contoh 1: Backup Harian

Skrip backup `/home/user/backup.sh` dijalankan setiap hari pukul 01:00 pagi:

```bash
0 1 * * * /home/user/backup.sh
```

#### Contoh 2: Membersihkan Cache Setiap Minggu

```bash
0 0 * * 0 rm -rf /var/tmp/*
```

Penjelasan: Membersihkan folder `/var/tmp/` setiap Minggu pukul 12:00 AM.

#### Contoh 3: Menjalankan Python Script Setiap Jam

```bash
0 * * * * /usr/bin/python3 /home/user/script.py
```

Penjelasan: Skrip `script.py` dijalankan setiap jam pada menit ke-0.

---

### **Cron Syntax Shortcut**

1. `@reboot` - Menjalankan perintah saat sistem reboot.
   ```bash
   @reboot /path/to/script.sh
   ```
2. `@hourly` - Menjalankan setiap jam.
   ```bash
   @hourly /path/to/script.sh
   ```
3. `@daily` - Menjalankan setiap hari.
   ```bash
   @daily /path/to/script.sh
   ```
4. `@weekly` - Menjalankan setiap minggu.
   ```bash
   @weekly /path/to/script.sh
   ```
5. `@monthly` - Menjalankan setiap bulan.
   ```bash
   @monthly /path/to/script.sh
   ```

---

### **Log Cron Job**

Log dari cron job bisa dilihat di file:

```bash
/var/log/syslog
```

Filter log untuk cron:

```bash
grep CRON /var/log/syslog
```

---

### **Alternatif Cron: Systemd Timer**

Jika ingin mengganti cron, Anda bisa menggunakan **systemd timer** untuk mengatur tugas otomatis. Systemd timer lebih fleksibel dan mendukung event-driven tasks.

---
