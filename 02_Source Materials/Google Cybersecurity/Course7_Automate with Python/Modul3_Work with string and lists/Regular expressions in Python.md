---
id: Regular expressions in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Pengenalan Regular Expressions (Regex) untuk Mencari Pola dalam String

### Apa itu Regular Expressions?

- **Regular expression** (regex) adalah urutan karakter yang membentuk pola untuk mencari atau mencocokkan string.
- Berguna untuk mencari pola tertentu di file log atau string, misalnya:
  - Menemukan string yang diawali prefiks tertentu.
  - Menemukan string dengan panjang tertentu.
  - Dalam konteks keamanan, dapat digunakan untuk menemukan alamat IP tertentu atau semua email dalam log file.

### Kenapa Regex Berguna?

- Regex memungkinkan pencarian pola tanpa mengetahui detail spesifik data.
- Contoh: Untuk menemukan semua email dalam log file, regex dapat mencocokkan pola email tanpa harus mengetahui alamat emailnya terlebih dahulu.

---

### Simbol Dasar dalam Regex

#### 1. **Plus Sign (`+`)**

- Merepresentasikan satu atau lebih kemunculan suatu karakter.
- Contoh pola: `a+`
  - Cocok dengan: "a", "aa", "aaa", dst.
- Contoh string: `"a", "aa", "a", "aaa"`
  - Regex `a+` akan mencocokkan semua instance karakter `a`.

#### 2. **`\w`**

- Cocok dengan **karakter alfanumerik** (huruf dan angka) tetapi tidak dengan simbol.
- Contoh yang cocok: `"1"`, `"k"`, `"i"`.

#### 3. **Gabungan `\w+`**

- Kombinasi `\w` dan `+` cocok dengan string alfanumerik dalam panjang berapa pun.
- Contoh yang cocok: `"192"`, `"abc123"`, `"security"`.

---

### Membuat Regex untuk Email

Struktur email: `user1@email1.com`

1. **Bagian pertama**: Alfanumerik dengan panjang bervariasi.
   - Pola: `\w+`
2. **Tanda `@`**: Selalu ada di setiap email.
   - Pola: `@`
3. **Domain name**: Alfanumerik dengan panjang bervariasi.
   - Pola: `\w+`
4. **Tanda titik (`.`)**: Selalu ada, tetapi perlu di-_escape_ agar tidak dikenali sebagai operator regex.
   - Pola: `\.`
5. **Bagian akhir**: Alfanumerik (contoh: `com`, `net`).
   - Pola: `\w+`

**Regex lengkap untuk email**:

```
\w+@\w+\.\w+
```

---

### Implementasi di Python

Regex digunakan melalui modul `re` di Python. Berikut langkah-langkahnya:

1. **Impor modul `re`**:

   ```python
   import re
   ```

2. **Contoh string log**:

   ```python
   email_log = """user1@gmail.com
   admin@yahoo.com
   contact@company.org"""
   ```

3. **Gunakan fungsi `findall()`**:

   - Fungsi ini mencari semua pola yang cocok dan mengembalikan daftar hasil.

   ```python
   emails = re.findall(r"\w+@\w+\.\w+", email_log) #r = raw string
   print(emails)
   ```

4. **Hasil**:
   ```python
   ['user1@gmail.com', 'admin@yahoo.com', 'contact@company.org']
   ```

---

### Kesimpulan

- **Regex** sangat berguna untuk mencari pola dalam string, terutama di konteks keamanan.
- Contoh aplikasi: Menemukan semua alamat email dalam file log besar.
- Regex adalah alat yang kuat dengan banyak simbol lain yang dapat dipelajari lebih lanjut.
  Jelajahi dan praktikkan untuk meningkatkan pemahaman Anda!
