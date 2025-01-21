---
id: More about regular expressions
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Pengantar Regex (Regular Expression)

Regular expression (regex) adalah rangkaian karakter yang membentuk pola tertentu untuk mencari data pada string. Regex sering digunakan dalam keamanan siber, misalnya untuk mencari alamat IP, email, atau ID perangkat. Di Python, regex diakses menggunakan modul **`re`**, yang harus diimpor terlebih dahulu dengan:

```python
import re
```

Fungsi utama yang digunakan adalah **`re.findall()`**, yang akan mengembalikan semua kecocokan regex dalam bentuk daftar.

---

## Simbol dalam Regex

### Simbol untuk Tipe Karakter

1. **`\w`**

   - Mencocokkan semua karakter alfanumerik (huruf, angka, dan underscore `_`).
   - Contoh:
     ```python
     re.findall(r"\w", "h32rb17")  # Output: ['h', '3', '2', 'r', 'b', '1', '7']
     ```

2. **`\d`**

   - Mencocokkan semua digit (angka 0–9).
   - Contoh:
     ```python
     re.findall(r"\d", "h32rb17")  # Output: ['3', '2', '1', '7']
     ```

3. **`\s`**

   - Mencocokkan semua spasi.

4. **`.`**

   - Mencocokkan semua karakter, termasuk simbol.

5. **`\.`**
   - Mencocokkan karakter titik (`.`).

---

### Simbol untuk Menghitung Jumlah Kemunculan

1. **`+`**

   - Mencocokkan satu atau lebih kemunculan karakter.
   - Contoh:
     ```python
     re.findall(r"\d+", "h32rb17")  # Output: ['32', '17']
     ```

2. **`*`**

   - Mencocokkan nol, satu, atau lebih kemunculan karakter.
   - Contoh:
     ```python
     re.findall(r"\d*", "h32rb17")
     # Output: ['', '', '32', '', '', '17', '']
     ```

3. **`{n}`**

   - Mencocokkan tepat **n** jumlah kemunculan karakter.
   - Contoh:
     ```python
     re.findall(r"\d{2}", "h32rb17 k825t0m c2994eh")  # Output: ['32', '17', '82', '99']
     ```

4. **`{n,m}`**
   - Mencocokkan **n** hingga **m** jumlah kemunculan karakter.
   - Contoh:
     ```python
     re.findall(r"\d{1,3}", "h32rb17 k825t0m c2994eh")
     # Output: ['32', '17', '825', '0', '299', '4']
     ```

---

## Contoh Penggunaan

Misalkan Anda memiliki data login karyawan seperti ini:

```plaintext
"1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"
```

Tujuan: Ambil username dan jumlah login karyawan.

Langkah-langkah:

1. Pola username adalah teks alfanumerik: **`\w+`**.
2. Username diikuti tanda titik dua `:`: **`:`**.
3. Setelah titik dua, ada spasi: **`\s`**.
4. Diikuti jumlah login berupa angka: **`\d+`**.

Regex untuk pola ini adalah:

```python
pattern = r"\w+:\s\d+"
```

Kode lengkap:

```python
import re
employee_logins = "1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"
result = re.findall(r"\w+:\s\d+", employee_logins)
print(result)
# Output: ['bmoreno: 12', 'tshah: 7', 'sgilmore: 5']
```

---

## Hal yang Perlu Diingat

- **Raw string** (`r'...'`) sangat penting agar Python tidak salah menginterpretasikan backslash.
- **Regex** harus diuji untuk memastikan pola yang digunakan sudah sesuai.

---

## Kesimpulan

Regex memungkinkan Anda untuk mencari pola tertentu dalam sebuah string. Di Python, Anda bisa memanfaatkan modul **`re`** dengan fungsi seperti **`re.findall()`**. Dengan regex, Anda bisa mendefinisikan pola menggunakan simbol-simbol tertentu untuk mencocokkan tipe karakter dan mengontrol jumlah kemunculannya.
