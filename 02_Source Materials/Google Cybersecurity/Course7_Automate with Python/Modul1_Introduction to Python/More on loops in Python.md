---
id: More on loops in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Iterasi dalam Python: Panduan Praktis untuk Pemula

### Pengertian Iterative Statements

Iterative statements adalah perintah yang memungkinkan kode untuk berjalan berulang kali berdasarkan kondisi tertentu. Iterasi dapat terjadi **0 atau lebih kali** tergantung pada kriteria yang diberikan. Dalam Python, iterasi dapat dilakukan menggunakan **for loops** dan **while loops**. Berikut adalah rangkuman cara penggunaannya dan kontrol alurnya menggunakan **break** dan **continue**.

---

### **1. For Loops**

**For loops** digunakan untuk mengulang item dalam sebuah urutan, seperti **list** atau **string**.

#### Contoh:

```python
usernames = ["elarson", "bmoreno", "tshah", "sgilmore"]
for i in usernames:
    print(i)
```

#### Penjelasan:

- **Header loop**: Dimulai dengan kata kunci `for`, diikuti variabel loop (contoh: `i`) yang akan merepresentasikan setiap elemen dalam urutan.
- **In operator**: Memberitahu Python untuk mengiterasi setiap elemen dalam urutan.
- **Loop body**: Kode yang dieksekusi dalam setiap iterasi (contoh: `print(i)`).
- Pastikan **loop body** diindentasikan agar Python dapat mengenali bagian ini sebagai bagian dari loop.

#### Iterasi pada String:

Loop juga dapat digunakan untuk mengiterasi setiap karakter dalam string.

```python
for char in "security":
    print(char)
```

---

### **2. Menggunakan `range()`**

Untuk menghasilkan urutan angka, gunakan fungsi **range()**. Formatnya adalah:

```python
range(start, stop, step)
```

- **Start**: Titik awal (opsional, default = 0).
- **Stop**: Titik akhir (wajib, eksklusif).
- **Step**: Besar langkah (opsional, default = 1).

#### Contoh:

```python
for i in range(5):  # Sama seperti range(0, 5, 1)
    print(i)
```

Hasil: **0, 1, 2, 3, 4** (angka 5 tidak termasuk).

---

### **3. While Loops**

**While loops** digunakan untuk menjalankan kode selama suatu **kondisi bernilai True**.

#### Contoh:

```python
i = 1
while i < 5:
    print(i)
    i += 1
```

#### Penjelasan:

- **Kondisi loop**: Ditentukan dalam header setelah kata kunci `while`.
- **Perubahan nilai**: Variabel kontrol (`i`) harus diperbarui di dalam loop agar tidak terjadi **infinite loop**.

---

### **4. Mengontrol Alur Loop**

#### a. **Break**

Digunakan untuk **menghentikan loop** secara paksa ketika suatu kondisi terpenuhi.

```python
assets = ["laptop1", "desktop20", "smartphone03"]
for asset in assets:
    if asset == "desktop20":
        break
    print(asset)
```

Hasil: Loop berhenti saat mencapai "desktop20". Hanya **laptop1** yang tercetak.

#### b. **Continue**

Digunakan untuk **melewati iterasi tertentu** tanpa menghentikan loop.

```python
assets = ["laptop1", "desktop20", "smartphone03"]
for asset in assets:
    if asset == "desktop20":
        continue
    print(asset)
```

Hasil: "desktop20" dilewati, tetapi loop tetap berlanjut hingga mencetak **laptop1** dan **smartphone03**.

---

### **5. Infinite Loops**

**Infinite loop** terjadi jika kondisi pada loop selalu **True**, sehingga loop tidak pernah berhenti. Contoh sederhana:

```python
while True:
    print("Loop tak berakhir!")
```

**Cara menghentikan**: Tekan **CTRL+C** atau **CTRL+Z** di terminal.

---

### **6. Kondisi pada While Loops**

#### a. Menggunakan Integer

Loop berjalan berdasarkan kondisi angka.

```python
login_attempts = 0
while login_attempts < 5:
    print("Percobaan login:", login_attempts)
    login_attempts += 1
```

#### b. Menggunakan Boolean

Boolean dapat digunakan untuk mengatur kapan loop berhenti.

```python
count = 0
login_status = True
while login_status:
    print("Coba lagi.")
    count += 1
    if count == 4:
        login_status = False
```

Loop berhenti ketika `login_status` berubah menjadi **False**.

---

### **7. Kesimpulan**

- Gunakan **for loops** untuk iterasi berdasarkan urutan yang pasti, seperti list atau string.
- Gunakan **while loops** untuk iterasi berdasarkan kondisi tertentu.
- Gunakan **break** untuk menghentikan loop, dan **continue** untuk melewati iterasi tanpa menghentikan loop.
- Hati-hati terhadap **infinite loops** yang dapat menyebabkan program tidak merespons.

Pemahaman dan praktik loop ini sangat penting bagi **security analyst**, terutama untuk otomatisasi tugas atau analisis data. Selamat mencoba! 🎉
