---
id: NTLM
aliases: []
tags: []
---

Tags: [[windows_fundamental]]

## Penjelasan Format Hash NTLM untuk Menyimpan Password Login Windows

**NTLM (NT LAN Manager)** adalah protokol autentikasi yang digunakan oleh Windows untuk otentikasi login. Password login di Windows **tidak disimpan dalam bentuk teks biasa (plaintext)**, melainkan dalam bentuk hash yang disebut **NTLM hash**. Format ini digunakan untuk mengamankan password, meskipun tidak sepenuhnya bebas dari kelemahan.

---

### Struktur dan Format Hash NTLM

1. **Password Hashing**:

   - NTLM hanya mendukung password dalam format **Unicode (UTF-16 Little Endian)**.
   - Proses hashing menggunakan algoritma **MD4**.
   - NTLM **tidak menggunakan salt**, yang membuatnya lebih mudah untuk diserang dengan teknik seperti **rainbow tables** atau brute force.

2. **Langkah Proses Hashing NTLM**:

   - Password pengguna (plaintext) dikonversi ke Unicode (UTF-16 LE).
   - Password yang sudah dalam bentuk Unicode di-hash menggunakan **algoritma MD4**.
   - Hasil akhirnya adalah hash NTLM sepanjang 128-bit (16 byte).

   **Formula hashing NTLM**:

   ```
   NTLM Hash = MD4(Unicode(password))
   ```

3. **Contoh Format NTLM Hash**:
   Hash NTLM biasanya ditampilkan dalam bentuk **heksadesimal**. Contohnya:

   ```
   b4b9b02e6f09a9bd760f388b67351e2b
   ```

   Penjelasan:

   - Password: `password123`
   - NTLM Hash: `b4b9b02e6f09a9bd760f388b67351e2b`

---

### Di Mana Hash NTLM Disimpan?

- Di sistem operasi Windows, hash NTLM disimpan di file **SAM (Security Account Manager)**. Lokasinya:
  ```
  C:\Windows\System32\config\SAM
  ```
- File ini dilindungi oleh Windows dan hanya bisa diakses oleh proses khusus seperti **LSASS** atau menggunakan metode eskalasi hak akses.

---

### Kerentanan NTLM Hash

1. **Tidak Ada Salt**:

   - Tidak menggunakan salt berarti hash password yang sama akan menghasilkan hash NTLM yang sama. Ini membuat hash rentan terhadap **rainbow table attack**.

2. **Kerentanan terhadap Serangan Offline**:

   - Jika seorang penyerang berhasil mengekstrak hash NTLM dari sistem (misalnya, dari file SAM), mereka bisa melakukan serangan **brute force** atau **dictionary attack** pada hash tersebut di luar jaringan.

3. **Tidak Melibatkan Proses Perulangan**:
   - Hash NTLM hanya menggunakan satu putaran hashing, sehingga lebih cepat untuk dihitung ulang (dan diserang).

---

### Cara Mengekstrak dan Menggunakan Hash NTLM

- Hash NTLM bisa diekstrak menggunakan alat seperti:

  - **mimikatz**
  - **hashdump** (di Metasploit)
  - **impacket-secretsdump**
  - **pwdump**

- Contoh menggunakan **impacket-secretsdump**:

  ```bash
  secretsdump.py administrator@target_ip
  ```

- Hash NTLM yang diekstrak biasanya terlihat seperti ini:
  ```
  Administrator:500:aad3b435b51404eeaad3b435b51404ee:b4b9b02e6f09a9bd760f388b67351e2b:::
  ```
  Penjelasan:
  - `500`: User ID.
  - `aad3b435b51404eeaad3b435b51404ee`: LM hash (biasanya diisi dengan nilai default jika tidak digunakan).
  - `b4b9b02e6f09a9bd760f388b67351e2b`: NTLM hash.

---

### Tips untuk Mengamankan Hash NTLM

1. **Gunakan Password yang Kuat**:

   - Password panjang dan kompleks lebih sulit ditebak atau di-brute force.

2. **Hindari Menggunakan NTLM di Jaringan**:

   - Jika memungkinkan, gunakan autentikasi berbasis Kerberos yang lebih aman.

3. **Gunakan Alat Deteksi Serangan NTLM**:

   - Gunakan alat seperti **Responder** untuk mendeteksi penyalahgunaan NTLM di jaringan.

4. **Implementasikan Account Lockout Policy**:
   - Membatasi jumlah percobaan login untuk mencegah brute force.

---
