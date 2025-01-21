Tags: [[computational]] 

Binary adalah format bilangan yang terdiri dari angka 1 dan 0. Dan komputer itu hanya mengerti binary ini, walaupun angka di dalam komputer dianggap sebagai ilusi semata.

Contoh macam macam format bilangan:

1. Desimal (10 angka) = 1 2 3 4 5 6 7 8 9
    
2. Binary (2 angka) = 0 1
    
3. Hexadecimal (16 angka) = 0 1 2 3 4 5 6 7 8 9 A B C D E F
    
    Fun Fact → angka 16 bisa ditulis 1 digit = F
    
4. Oktal (8 angka) = 0 1 2 3 4 5 6 7
    

## Desimal vs Binary

### Decimal

Ini adalah angka yang biasa digunakan Manusia. Cara kerja desimal adalah ketika angka telah habis “sampai angka 9”, maka perhitungan akan dimulai lagi dari satu sekaligus mengubah digit terakhir menjadi 0 lagi.

Contoh :

— 009

— 010

Bisa dilihat diatas berubah dari 9 menjadi nol lagi

### Binary

Ini adalah angka yang biasa digunakan Mesin. Cara kerjanya sama seperti angka desimal tetapi hanya terdiri dari 2 angka saja, yaitu 0 dan 1.

- Contoh:
    
    0000 → 0
    
    0001 → 1
    
    0010 → 2
    
    0011 → 3
    
    0100 → 4
    
    0101 → 5
    
    0110 → 6
    
    0111 → 7
    
    1000 → 8
    
- Semua hal yang dikomputer itu formatnya binary, lalu bagaimana dengan wujud text dan lainya yang ada dalam komputer?
    
    - Number 123 → 1111011
    - Character “A” → menjadi angka 65, ini berdasarkan peraturan internasional ASCII, maka menjadi 1000001
    - Text “Hello” → 104 101 108 111 → … (masing masing char diubah ke ASCII)
    - Color “white”→ RGB(255 255 255) → …. (nilai max masing”= 255)
    - Gambar → dalam suatu gambar itu ada sebuah pixel, yang berisi dari 1 warna di setiap kotaknya. Maka dari itu jika ada gambar ukuran 256 pixels == 256 x 256 RGB (x,x,x)
    - Audio → Menggunakan Analog Digital Converter → 000111101
    - Video → Gabungan Audio Gambar Warna == seconds x image + audio → 20 detik x 256 x 256 RGB(x,x,x) + y
- Beberapa Istilah yang Sering digunakan:
    
    1. Bit = 1 digit
    2. Byte = 8 digit —> 01010101