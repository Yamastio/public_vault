---
id: While loops
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Iterative Statements: While Loop

Pada pembahasan sebelumnya, kita telah mempelajari tentang **iterative statements** menggunakan **for loop**. Kali ini, kita akan membahas jenis loop lain, yaitu **while loop**.

Berikut adalah rangkuman yang sederhana dan mudah dipahami:

### Apa Itu While Loop?

- **While loop** adalah pernyataan iteratif yang mengeksekusi kode berulang kali selama kondisinya **True** (benar).
- Ketika kondisi menjadi **False** (salah), **while loop** berhenti.

### Struktur Dasar While Loop

1. **Header**

   - Diawali dengan kata kunci `while`.
   - Diikuti oleh **kondisi** (yang menghasilkan nilai Boolean: True atau False).
   - Diakhiri dengan tanda titik dua `:`.

2. **Body**
   - Berisi kode yang diindentasi dan akan dijalankan selama kondisinya True.
   - Penting: Variabel dalam kondisi harus diubah nilainya di dalam body, agar loop bisa berhenti.

### Contoh Dasar While Loop

```python
time = 0  # Variabel loop didefinisikan di luar while
while time <= 10:  # Kondisi
    print(time)  # Aksi pertama
    time += 2  # Increment variabel loop
```

- **Apa yang terjadi?**
  - **time** dimulai dari 0.
  - Selama **time ≤ 10**, angka akan dicetak, lalu ditambah 2.
  - Ketika **time > 10**, loop berhenti.

### Perbedaan Utama dengan For Loop

- Pada **for loop**, kita mengulang berdasarkan **sekuens** yang sudah ditentukan.
- Pada **while loop**, pengulangan terjadi selama **kondisi tertentu** masih terpenuhi.

### Contoh Praktis: Membatasi Koneksi Perangkat

Kita akan membuat program untuk membatasi jumlah perangkat yang dapat terhubung.

#### Kode:

```python
max_devices = 5  # Batas maksimum perangkat
i = 1  # Variabel loop

while i < max_devices:  # Kondisi
    print("User masih bisa menambahkan perangkat.")  # Pesan saat perangkat bisa ditambahkan
    i += 1  # Increment variabel loop

print("User telah mencapai batas maksimum perangkat.")  # Pesan saat loop selesai
```

#### Penjelasan:

1. **max_devices** diatur ke 5 (batas maksimum).
2. **i** dimulai dari 1 (jumlah perangkat yang terhubung saat ini).
3. Selama **i < max_devices**, pesan akan dicetak, dan **i** bertambah 1 setiap iterasi.
4. Ketika **i = 5**, loop berhenti, dan program mencetak pesan bahwa batas telah tercapai.

#### Output:

```
User masih bisa menambahkan perangkat.
User masih bisa menambahkan perangkat.
User masih bisa menambahkan perangkat.
User masih bisa menambahkan perangkat.
User telah mencapai batas maksimum perangkat.
```

### Kesimpulan

- **While loop** cocok digunakan ketika kita tidak tahu pasti berapa banyak iterasi yang dibutuhkan, tapi tahu kondisinya.
- Selalu pastikan kondisi loop pada akhirnya menjadi **False** untuk menghindari **infinite loop** (loop yang tidak pernah berhenti).

Sekarang, dengan pemahaman **for loop** dan **while loop**, kamu memiliki lebih banyak opsi untuk menulis kode Python yang fleksibel dan efisien! 🚀
