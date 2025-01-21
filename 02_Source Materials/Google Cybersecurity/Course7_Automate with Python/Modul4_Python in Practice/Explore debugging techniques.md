---
id: Explore debugging techniques
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Debugging Python: Teknik dan Strategi

Mengembangkan kode di Python sering kali disertai error. Namun, kemampuan untuk memahami dan memperbaiki error ini adalah bagian penting dari proses belajar. Berikut adalah rangkuman tentang jenis error dalam Python dan strategi untuk mengatasinya.

### Jenis-Jenis Error

1. **Syntax Errors**

   - Error ini terjadi akibat kesalahan pada sintaks Python, misalnya:
     - Lupa menutup tanda kutip.
     - Tidak menyertakan titik dua (`:`) setelah header fungsi.
   - Output biasanya menampilkan pesan seperti:
     - `SyntaxError: invalid syntax`
     - `SyntaxError: unexpected EOF while parsing`
   - **Contoh**:

     ```python
     message = "You are debugging a syntax error
     print(message)
     ```

     Output: `SyntaxError: EOL while scanning string literal`
     Penyebab: Tanda kutip di akhir string hilang.

   - **Catatan**:
     Jika terkait indentasi, pesan error akan menjadi `IndentationError`.

2. **Logic Errors**

   - Terjadi ketika logika dalam kode menghasilkan hasil yang tidak diinginkan.
   - Tidak ada pesan error; kode tetap berjalan tetapi hasilnya salah.
   - **Contoh**:
     ```python
     login_attempts = 5
     if login_attempts >= 5:
         print("User has not reached maximum number of login attempts.")
     else:
         print("User has reached maximum number of login attempts.")
     ```
     Output: `User has not reached maximum number of login attempts.`
     Penyebab: Operator logika (`>=`) salah, seharusnya `<`.

3. **Exceptions**
   - Error yang terjadi ketika kode tidak dapat dieksekusi meskipun sintaksnya benar.
   - Contoh pesan error:
     - `NameError`: Variabel belum didefinisikan.
     - `IndexError`: Indeks di luar rentang dalam list.
     - `TypeError`: Operasi dengan tipe data yang salah.
     - `FileNotFoundError`: File yang diminta tidak ditemukan.
   - **Contoh**:
     ```python
     print("Unusual logins:", unusual_logins)
     ```
     Output: `NameError: name 'unusual_logins' is not defined`
     Penyebab: Variabel `unusual_logins` belum diberi nilai.

### Strategi Debugging

1. **Debugger**

   - Gunakan debugger dalam Integrated Development Environment (IDE) seperti PyCharm atau VSCode.
   - Fitur utama:
     - **Breakpoints**: Menentukan bagian kode yang dieksekusi saat debugging.
     - Melihat nilai variabel secara real-time untuk melacak perubahan.

2. **Print Statements**
   - Tambahkan perintah `print()` sementara untuk mengetahui nilai variabel atau lokasi eksekusi kode.
   - **Contoh**:
     ```python
     new_users = ["sgilmore", "bmoreno"]
     approved_users = ["bmoreno", "tshah", "elarson"]
     def add_users():
         for user in new_users:
             print("line 5 - inside for loop")
             if user in approved_users:
                 print("line 7 - inside if statement")
                 print(user, "already in list")
             print("line 9 - before .append method")
             approved_users.append(user)
     ```
     Output menunjukkan bahwa `approved_users.append(user)` dipanggil dua kali, meskipun tidak seharusnya.
     Solusi: Tambahkan logika `else` agar `append()` hanya dilakukan jika pengguna belum ada dalam list.

### Kesimpulan

- **Syntax Errors**: Kesalahan sintaks yang ditandai dengan pesan error spesifik.
- **Logic Errors**: Kesalahan logika yang tidak menghasilkan pesan error tetapi membuat hasil kode salah.
- **Exceptions**: Kesalahan eksekusi meskipun sintaks benar, dengan pesan error seperti `NameError`, `IndexError`, dll.
- Gunakan **debugger** dan **print statements** untuk melacak sumber error.
- Debugging adalah proses penting untuk meningkatkan pemahaman dan kemampuan Anda dalam pemrograman.
