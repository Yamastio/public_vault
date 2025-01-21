---
id: Write a simple algorithm
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Algoritma dan Penerapannya di Python

### Apa itu Algoritma?

- **Algoritma** adalah sekumpulan aturan atau langkah yang digunakan untuk menyelesaikan masalah.
- Dalam istilah sederhana, algoritma mengambil input, menjalankan langkah-langkah tertentu, dan menghasilkan output.

#### Contoh Sehari-hari:

Membuat kopi adalah sebuah algoritma:

1. Ambil cangkir favoritmu.
2. Isi air ke dalam mesin kopi.
3. Tambahkan bubuk kopi.
4. Tekan tombol start.
5. Tunggu beberapa menit dan nikmati kopi.

### Contoh Penerapan Algoritma di Python

Sebagai seorang **security analyst**, misalnya, kamu memiliki daftar **IP addresses**. Tujuannya adalah mengekstrak **tiga digit pertama** dari setiap alamat IP untuk mengetahui informasi tentang jaringan asalnya.

#### Langkah-Langkah:

1. Ekstrak tiga digit pertama dari satu alamat IP menggunakan **string slicing**.
2. Terapkan solusi ini ke seluruh daftar alamat IP menggunakan **loop**.
3. Simpan hasilnya dalam daftar baru.

---

### Langkah 1: String Slicing untuk Satu Alamat IP

Misalnya, kita punya satu alamat IP:

```python
address = "198.567"
print(address[0:3])
```

- **address[0:3]**:
  - Mulai dari indeks ke-0 hingga indeks ke-3 (Python menghentikan slice sebelum indeks akhir).
- Output: `198`.

---

### Langkah 2: Terapkan ke Seluruh Daftar Menggunakan Loop

Gunakan **for loop** untuk memproses semua alamat IP dalam daftar:

```python
IP = ["198.567", "172.456", "192.789"]  # Daftar alamat IP
networks = []  # Daftar kosong untuk menyimpan hasil

for address in IP:
    networks.append(address[0:3])  # Tambahkan tiga digit pertama ke daftar networks

print(networks)
```

- **append()**:
  - Menambahkan elemen baru ke akhir daftar.
- Output: `['198', '172', '192']`.

---

### Penjelasan:

1. **Daftar Awal**:
   - `IP = ["198.567", "172.456", "192.789"]`.
2. **Daftar Kosong**:
   - `networks = []`.
3. **Loop**:
   - Untuk setiap `address` dalam daftar `IP`, ambil tiga digit pertama (`address[0:3]`) dan tambahkan ke daftar `networks`.
4. **Hasil Akhir**:
   - `networks = ['198', '172', '192']`.

---

### Tips Mendesain Algoritma:

1. **Pecah Masalah**: Jangan langsung menulis kode, identifikasi bagian-bagian kecil dari masalah.
2. **Uji Solusi Kecil**: Uji langkah kecil sebelum menerapkannya ke seluruh masalah.
3. **Gunakan Metode Python yang Relevan**: Seperti **string slicing** dan **append**.

Dengan latihan, algoritma akan terasa lebih mudah. Kita akan terus mengeksplorasi konsep ini! 🚀
