---
id: Basis Bilangan
aliases:
  - Base 16
  - Base 8
  - hexadecimal
  - octal
  - basis bilangan
tags: []
---

Tags: [[computer_fundamental]]

Tentu! Mari kita bahas lebih dalam tentang **basis bilangan**, khususnya hubungan antara **biner (base 2)** dengan **oktal (base 8)** dan **heksadesimal (base 16)**.

---

### **1. Apa Itu Basis Bilangan?**

Basis bilangan adalah sistem numerik yang menentukan jumlah simbol yang digunakan untuk merepresentasikan angka. Beberapa basis umum meliputi:

- **Desimal (Base 10):** Menggunakan 10 digit (0-9) → yang kita gunakan sehari-hari.
- **Biner (Base 2):** Menggunakan 2 digit (0 dan 1) → digunakan dalam komputer.
- **Oktal (Base 8):** Menggunakan 8 digit (0-7) → sering digunakan dalam sistem komputer lama dan Unix file permissions.
- **Heksadesimal (Base 16):** Menggunakan 16 digit (0-9 dan A-F) → digunakan dalam pemrograman dan alamat memori.

---

### **2. Mengapa Oktal dan Heksadesimal Digunakan sebagai Shorthand untuk Biner?**

Dalam komputer, data disimpan dalam bentuk biner (0 dan 1). Namun, menuliskan angka dalam biner bisa menjadi panjang dan sulit dibaca. **Oktal (base 8) dan heksadesimal (base 16) digunakan sebagai cara yang lebih ringkas untuk merepresentasikan angka biner.**

**Hubungan antara basis:**

- **Oktal (Base 8) → Mengelompokkan 3 bit biner menjadi 1 digit oktal**
- **Heksadesimal (Base 16) → Mengelompokkan 4 bit biner menjadi 1 digit heksadesimal**

Ini karena:

- \(2^3 = 8\) → Jadi, setiap 3 digit biner dapat direpresentasikan dengan 1 digit oktal.
- \(2^4 = 16\) → Jadi, setiap 4 digit biner dapat direpresentasikan dengan 1 digit heksadesimal.

---

### **3. Konversi Biner ke Oktal dan Heksadesimal**

#### **(a) Konversi Biner ke Oktal**

1. **Pisahkan biner menjadi grup 3 bit dari kanan ke kiri**
2. **Konversikan setiap grup ke oktal**

**Contoh:**
Konversi biner **`110101`** ke oktal:

1. Pisahkan menjadi grup 3 bit: `110 101`
2. Konversikan ke oktal:
   - `110` = **6**
   - `101` = **5**
3. Hasil dalam oktal: **65₈**

---

#### **(b) Konversi Biner ke Heksadesimal**

1. **Pisahkan biner menjadi grup 4 bit dari kanan ke kiri**
2. **Konversikan setiap grup ke heksadesimal**

**Contoh:**
Konversi biner **`10111011`** ke heksadesimal:

1. Pisahkan menjadi grup 4 bit: `1011 1011`
2. Konversikan ke heksadesimal:
   - `1011` = **B**
   - `1011` = **B**
3. Hasil dalam heksadesimal: **BB₁₆**

---

### **4. Mengapa Oktal dan Heksadesimal Digunakan di Komputer?**

- **Lebih mudah dibaca dibanding biner**
  - Biner `110101101110` panjang dan sulit dibaca.
  - Jika dikonversi ke heksadesimal: `D6E` lebih ringkas.
- **Lebih cepat dalam perhitungan manual dan debugging**
- **Sesuai dengan struktur komputer**
  - Heksadesimal lebih cocok karena komputer umumnya bekerja dengan **byte (8 bit)** yang bisa dipecah menjadi **dua digit heksadesimal**.

---

### **5. Contoh Penggunaan di Dunia Nyata**

- **Oktal dalam UNIX/Linux File Permissions**
  - Contoh: `chmod 755 file.txt`
  - `755` dalam oktal merepresentasikan `rwxr-xr-x` dalam permission.
- **Heksadesimal dalam Pemrograman**
  - Digunakan dalam warna HTML/CSS (`#FF5733`).
  - Digunakan dalam alamat memori (`0x1A3F`).
  - Digunakan dalam representasi karakter ASCII (`0x41` untuk 'A').

---

### **6. Ringkasan**

| **Basis**             | **Simbol yang Digunakan** | **Hubungan dengan Biner** | **Contoh**    |
| --------------------- | ------------------------- | ------------------------- | ------------- |
| **Biner (2)**         | 0, 1                      | -                         | 110101        |
| **Oktal (8)**         | 0-7                       | 3 bit biner per digit     | 110101 → 65₈  |
| **Desimal (10)**      | 0-9                       | -                         | 53            |
| **Heksadesimal (16)** | 0-9, A-F                  | 4 bit biner per digit     | 110101 → 35₁₆ |

---

### **7. Kesimpulan**

- **Oktal dan heksadesimal adalah cara lebih ringkas untuk merepresentasikan bilangan biner.**
- **Oktal menggunakan 3 bit per digit, sedangkan heksadesimal menggunakan 4 bit per digit.**
- **Heksadesimal lebih banyak digunakan karena sesuai dengan ukuran byte dalam komputer.**
- **Keduanya sering digunakan dalam dunia IT, terutama dalam debugging, pemrograman, dan administrasi sistem.**
