---
id: dont-use-client-side
aliases: []
tags: []
---

## Challenge: [dont-use-client-side]

- **Kategori:** [ Web Exploitation, Easy, picoCTF2019 ]
- **Poin:** [None]
- **Deskripsi:**
  ```Plaintext
  Can you break into this super secure portal? https://jupiter.challenges.picoctf.org/problem/29835/ (link) or http://jupiter.challenges.picoctf.org:29835
  ```
- **File terkait:** [https://jupiter.challenges.picoctf.org/problem/29835/]

## Langkah Penyelesaian

1. **Analisis Awal:**

   - Inspecting the website, clue is dont-use-client-side, so use dev mode
   - Found JS to confirm a password

   ```javascript
   function verify() {
     checkpass = document.getElementById("pass").value;
     split = 4;
     if (checkpass.substring(0, split) == "pico") {
       if (checkpass.substring(split * 6, split * 7) == "723c") {
         if (checkpass.substring(split, split * 2) == "CTF{") {
           if (checkpass.substring(split * 4, split * 5) == "ts_p") {
             if (checkpass.substring(split * 3, split * 4) == "lien") {
               if (checkpass.substring(split * 5, split * 6) == "lz_7") {
                 if (checkpass.substring(split * 2, split * 3) == "no_c") {
                   if (checkpass.substring(split * 7, split * 8) == "e}") {
                     alert("Password Verified");
                   }
                 }
               }
             }
           }
         }
       }
     } else {
       alert("Incorrect password");
     }
   }
   ```

2. **Eksploitasi / Penyelesaian:**

   - Setelah dilihat ternyata flag ada disitu, tinggal menyusun berdasarkan urutan nya, split = 4, split*2 = 4*2 = 8
   - Hasilnya:

     ```plaintext
     checkpass.substring(0, split) = "pico" (indeks 0–4)
     checkpass.substring(split*2, split*3) = "no_c" (Indeks 8–12)
     checkpass.substring(split*3, split*4) = "lien" (Indeks 12–16)
     checkpass.substring(split*4, split*5) = "ts_p" (Indeks 16–20)
     checkpass.substring(split*5, split*6) = "lz_7" (Indeks 20–24)
     checkpass.substring(split*6, split*7) = "723c" (Indeks 24–28)
     checkpass.substring(split*7, split*8) = "e}" (Indeks 28–32)
     ```

3. **Bukti / Output:**

   - setelah disusun urut dari index 0-32

   ```plaintext
   "pico" (0–4)
   "CTF{" (4–8)
   "no_c" (8–12)
   "lien" (12–16)
   "ts_p" (16–20)
   "lz_7" (20–24)
   "723c" (24–28)
   "e}" (28–32)
   ```

## Flag

```
[picoCTF{no_clients_plz_7723ce}]
```

## Catatan Tambahan

- Perhatikan detail dan petunjuk sekecil mungkin
