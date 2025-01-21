---
id: Work with files in Python
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Bekerja dengan File di Python

### Pengantar

- Anda telah mempelajari cara membuka file, membaca isinya, dan menulis ke file di Python.
- Artikel ini akan membahas metode **`.split()`** dan **`.join()`** untuk membantu memparsing data dan mengelola isi file.

---

### Parsing

**Parsing** adalah proses mengubah data menjadi format yang lebih mudah dibaca.
Proses ini berguna untuk:

1. **Menyesuaikan format data** agar dapat diolah Python.
2. **Membuat data lebih mudah dipahami** oleh programmer.

---

### Metode `.split()`

**Fungsi Utama:**

- Mengubah **string** menjadi **list** dengan memisahkannya berdasarkan karakter tertentu.

#### Cara Kerja:

1. Jika Anda memberikan karakter pemisah ke `.split()`, string akan dipisah berdasarkan karakter tersebut.
2. Jika tidak ada argumen yang diberikan, Python akan memisah string setiap kali bertemu **whitespace** (spasi, tab, atau newline).

#### Contoh:

```python
# Contoh 1: Menggunakan pemisah koma
approved_users = "elarson,bmoreno,tshah,sgilmore,eraab"
print("Sebelum .split():", approved_users)
approved_users = approved_users.split(",")
print("Setelah .split():", approved_users)

# Output:
# Sebelum .split(): elarson,bmoreno,tshah,sgilmore,eraab
# Setelah .split(): ['elarson', 'bmoreno', 'tshah', 'sgilmore', 'eraab']
```

```python
# Contoh 2: Tidak memberikan argumen ke .split()
removed_users = "wjaffrey jsoto abernard jhill awilliam"
print("Sebelum .split():", removed_users)
removed_users = removed_users.split()
print("Setelah .split():", removed_users)

# Output:
# Sebelum .split(): wjaffrey jsoto abernard jhill awilliam
# Setelah .split(): ['wjaffrey', 'jsoto', 'abernard', 'jhill', 'awilliam']
```

---

#### Penerapan `.split()` pada File

1. Gunakan metode **`.read()`** untuk membaca isi file menjadi string.
2. Terapkan **`.split()`** untuk memecah string menjadi list.

Contoh:

```python
with open("update_log.txt", "r") as file:
    updates = file.read()
updates = updates.split()

# Isi file sekarang diubah menjadi list dan siap untuk diolah.
```

---

### Metode `.join()`

**Fungsi Utama:**

- Mengubah **list** kembali menjadi **string** dengan menyisipkan karakter pemisah di antara elemen list.

#### Cara Kerja:

1. Berbeda dengan `.split()`, **`.join()`** ditulis sebagai metode dari karakter pemisah.
2. Elemen list akan digabungkan menjadi string, dipisahkan oleh karakter tersebut.

#### Contoh:

```python
# Contoh: Menggunakan koma sebagai pemisah
approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]
print("Sebelum .join():", approved_users)
approved_users = ",".join(approved_users)
print("Setelah .join():", approved_users)

# Output:
# Sebelum .join(): ['elarson', 'bmoreno', 'tshah', 'sgilmore', 'eraab']
# Setelah .join(): elarson,bmoreno,tshah,sgilmore,eraab
```

---

#### Penerapan `.join()` pada File

Jika isi file telah diubah menjadi list menggunakan `.split()`, Anda dapat mengembalikannya ke bentuk string untuk ditulis kembali ke file menggunakan `.join()`.

Contoh:

```python
# Menggabungkan list menjadi string dengan pemisah spasi
updates = " ".join(updates)

# Menulis kembali string ke file
with open("update_log.txt", "w") as file:
    file.write(updates)
```

---

### **Kesimpulan**

- Parsing membantu mengubah data menjadi lebih terstruktur dan mudah dipahami.
- Gunakan **`.split()`** untuk mengubah **string** menjadi **list**.
- Gunakan **`.join()`** untuk mengubah **list** kembali menjadi **string**.
- Gunakan **`.remove()`** untuk menghapus elemen dari list.
- Keduanya sangat berguna dalam mengolah isi file di Python.
