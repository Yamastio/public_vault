---
id: sha512crypt
aliases: []
tags: []
---

Tags: [[linux_fundamental]]

**SHA512crypt** adalah algoritma hashing yang digunakan untuk menyimpan password secara aman di sistem berbasis Unix/Linux. Ini adalah variasi dari algoritma SHA-512 yang dimodifikasi untuk digunakan dalam **crypt(3)**, sistem hashing password yang ada di Linux. Algoritma ini digunakan untuk melindungi password agar sulit ditebak atau dihancurkan dengan metode brute force atau rainbow table.

Berikut adalah penjelasan lebih lanjut mengenai **SHA512crypt** dengan pendekatan yang sederhana:

### 1. **Apa Itu Hashing?**

Hashing adalah proses mengubah data (seperti password) menjadi string karakter tetap yang tidak bisa dibalikkan, artinya tidak ada cara langsung untuk mendapatkan data asli dari hash tersebut. Ini penting karena kita tidak menyimpan password asli di sistem, melainkan hash-nya.

### 2. **SHA512crypt Format**

Ketika sebuah password di-hash menggunakan **SHA512crypt**, hasilnya akan berupa string yang dimulai dengan **`$6$`** diikuti oleh beberapa elemen. Formatnya seperti ini:

```
$6$salt$hashed_password
```

Penjelasan elemen-elemen tersebut:

- **`$6$`**: Menunjukkan bahwa hashing yang digunakan adalah **SHA-512**.
- **`salt`**: Ini adalah string acak yang ditambahkan ke password sebelum dilakukan hashing. Salt memastikan bahwa meskipun dua orang menggunakan password yang sama, hasil hash-nya tetap berbeda.
- **`hashed_password`**: Ini adalah hasil dari proses hashing password menggunakan SHA-512 dengan salt yang diberikan.

Contoh hash yang menggunakan SHA512crypt:

```
$6$rounds=5000$saltstring$hashedpasswordresult...
```

### 3. **Penambahan Rounds**

Pada format **SHA512crypt**, ada opsi untuk menentukan berapa kali hashing akan dilakukan, yang disebut dengan **rounds**. Ini dilakukan untuk memperlambat proses cracking password, sehingga lebih sulit bagi penyerang untuk melakukan brute force.
Contoh:

```
$6$rounds=5000$salt$hashed_password
```

- **`rounds=5000`**: Ini berarti proses hashing dilakukan 5000 kali.

### 4. **Keamanan**

- **Salt**: Dengan adanya salt yang unik untuk setiap password, jika dua orang memiliki password yang sama, hasil hash-nya tetap akan berbeda. Hal ini mencegah serangan **rainbow table**.
- **Rounds**: Menambah jumlah putaran (rounds) pada hashing membuat prosesnya lebih lama, sehingga lebih sulit untuk serangan brute force yang mencoba banyak kombinasi password.
- **Panjang Hash**: SHA-512 menghasilkan hash yang panjang (512 bit), yang juga menambah tingkat keamanannya dibandingkan dengan algoritma yang lebih pendek seperti MD5 atau SHA-256.

### 5. **Contoh Penggunaan**

Misalnya, kita ingin meng-hash password "password123" menggunakan **SHA512crypt** dengan salt acak dan melakukan 5000 rounds, maka format hash-nya akan terlihat seperti ini:

```
$6$rounds=5000$salt123$7eq8d7djsf38f9djf9qks9d8f9w9x...
```

- **$6$** menunjukkan penggunaan SHA-512.
- **rounds=5000** menunjukkan 5000 putaran hashing.
- **salt123** adalah salt yang digunakan.
- **7eq8d7djsf38f9djf9qks9d8f9w9x...** adalah hasil hash dari password yang sudah di-hash.

### 6. **Mengapa SHA512crypt Digunakan?**

SHA512crypt digunakan karena cukup aman untuk melindungi password dengan memanfaatkan salt dan rounds. Dalam konteks administrasi sistem dan penyimpanan password yang aman, SHA512crypt merupakan pilihan yang baik, karena lebih kuat dibandingkan dengan algoritma hashing yang lebih lama seperti MD5 atau DES.

### Kesimpulan

**SHA512crypt** adalah cara yang sangat aman untuk meng-hash password di sistem Unix/Linux. Dengan menggunakan **salt** dan **rounds**, algoritma ini memastikan bahwa password yang disimpan di sistem tidak dapat dengan mudah ditebak atau dihancurkan oleh penyerang, bahkan jika mereka memiliki akses ke hash tersebut.
