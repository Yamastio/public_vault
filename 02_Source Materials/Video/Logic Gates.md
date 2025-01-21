Tags: [[computational]]

## Apa itu Logic Gates
Electronic Circuits ini bisa membuat sebuah gerbang logika (logic gates) yaitu dasar dari sebuah komputasi.

Logic Gates == Mengatur logika dengan menggunakan transsistor, membuat logika kelistrikan 0 / 1

Macam macam logic gates:

- AND = 2 harus true
- OR = Salah satu true
- NAND = Tidak AND
- NOR = sama seperti OR hanya dibalik saja
- XOR = Exlussive OR (harus milih 1 true untuk jadi true, jika 2 true = false)
- XNOR
- NOT = Kebalikan saja, 0 menjadi 1

Logic Gates menjadi Komputasi

- Half Adder, terdiri dari SUM dan Carry (input hanya A dan B)
    
    Di dalam logic gates ada yang namanya Carry, apa itu carry?
    
    Carry contohnya ketika melakukan penjumlahan 11 + 99 yang terjadi ketika kita menambahkan yang satuan dulu maka jadi 10, disitu ditulis 0 saja lalu angka 1 inilah yang berfungsi sebagai carry, dia pindah ke atas dan menjadi penjumlah untuk angka puluhan. Yang terjadi menjadi 1 + 1 + 9 = 11, maka total nya menjadi 110. Disitu angka 1 menjadi carry.
    
- Full Adder
    
    Ada dua half adder didalamnya, tidak hanya A dan B, ada juga C yang berfungsi sebagai carry
    

Dari sini maka muncullah 8 bit, bagaimana 8 bit dibuat?

8 bit terbuat dari logic gates tadi, dari kumpulan half adder dan full adder, yang pertama pasti half adder, dan selanjutnya akan full adder, karena nilai pertama tidak mungkin membawa carry