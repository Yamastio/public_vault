---
id: Develop a parsing algorithm in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Membuat Program untuk Mendeteksi Login Gagal

### Gambaran Masalah

Kita akan membuat program untuk mendeteksi percobaan login gagal berdasarkan log file. Program ini akan berjalan setiap kali ada user login dan memeriksa apakah user tersebut memiliki **tiga atau lebih percobaan login gagal**. Jika iya, program akan memberikan **peringatan** bahwa akun user tersebut terkunci.

### Struktur Input

- **Log file:** File dalam format `.txt` yang berisi satu nama pengguna per baris. Setiap nama pengguna mencerminkan satu percobaan login gagal.
- **Contoh Tujuan Program:** Saat seorang user login, program akan:
  1. Membaca log file.
  2. Menghitung berapa kali nama user tersebut muncul di log.
  3. Memberikan peringatan jika jumlahnya tiga atau lebih.

---

### Strategi Penyelesaian

1. **Baca dan Simpan Data dari File:**

   - Log file dibaca, dipisah, dan disimpan dalam variabel `usernames`.
   - **Contoh Hasil:** List dengan elemen berupa nama pengguna.

2. **Menghitung Kemunculan Nama Pengguna:**

   - Gunakan **loop** untuk memeriksa setiap elemen dalam list.
   - Tambahkan **counter** yang menghitung kemunculan nama pengguna tertentu.
   - Jika nama ditemukan, tambahkan nilai counter.

3. **Logika Final:**
   - Jika **counter** ≥ 3, tampilkan pesan bahwa akun terkunci.
   - Jika kurang dari 3, izinkan login.

---

### Implementasi Python

1. **Membuat Fungsi Utama:**
   Fungsi ini bernama `login_check()` dan memiliki dua parameter:

   - `login_list`: List yang berisi log percobaan login gagal.
   - `current_user`: User yang sedang login.

2. **Langkah-Langkah Fungsi:**

   - Inisialisasi variabel `counter` dengan nilai 0.
   - Gunakan **loop** untuk memeriksa elemen di `login_list`.
   - Jika elemen cocok dengan `current_user`, tambahkan 1 ke `counter`.
   - Buat **if-else statement**:
     - Jika `counter` ≥ 3, tampilkan pesan bahwa akun terkunci.
     - Jika tidak, izinkan login.

3. **Kode Python Lengkap:**

   ```python
   def login_check(login_list, current_user):
       # Inisialisasi counter
       counter = 0

       # Loop untuk menghitung kemunculan nama pengguna
       for i in login_list:
           if i == current_user:
               counter += 1

       # Logika final
       if counter >= 3:
           print(f"Akun {current_user} terkunci! Login gagal.")
       else:
           print(f"Selamat datang, {current_user}! Login berhasil.")
   ```

4. **Contoh Penggunaan:**
   Misalnya kita punya log file seperti berikut:

   ```txt
   elarson
   eraab
   tsmith
   eraab
   jdoe
   eraab
   ```

   Maka, implementasi program:

   ```python
   # Log file dalam list
   log_attempts = ["elarson", "eraab", "tsmith", "eraab", "jdoe", "eraab"]

   # Uji coba login
   login_check(log_attempts, "elarson")  # Output: Login berhasil
   login_check(log_attempts, "eraab")   # Output: Akun eraab terkunci! Login gagal.
   ```

---

### Penutup

Kita baru saja membuat algoritma sederhana untuk mendeteksi percobaan login gagal:

- Membaca file log.
- Menggunakan **loop** untuk menghitung kemunculan nama pengguna.
- Menambahkan logika untuk memberikan peringatan jika diperlukan.

Seiring berkembangnya kemampuan Anda, algoritma ini dapat dioptimalkan lebih lanjut. Namun, solusi ini cukup untuk memulai dan membantu Anda memahami konsep dasar file parsing dan penghitungan data di Python.
