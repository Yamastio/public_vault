Tags: [[java_oop]] 

## Procedural Programming Limitation

- Procedural itu dari atas ke bawah cara kode berjalan
- Yang terjadi adalah kesulitan memanajemen program yang besar atau luas
- Limitation resuable, tidak bisa digunakan kembali
- Sulit merepresentasikan dunia nyata ke programming jika hanya dengan procedural

## Struct in C

Jadi ada masalah gini:

- Ada sebuah mobil (merek, tahun, model, kursi) lalu ingin duplicate ke mobil lain

```C
char car1Brand[100] = "Tesla";

char car2Brand[100]; strcpy(car2Brand, car1Brand);
```

Kode diatas maksudnya kita memasukan nilai car1Brand ke car2Brand.

Nah masalahnya, ketika anda ingin menambahkan komponen baru, perlu nambah juga di masing masing, tidak efektif.

Nah untuk mengatasi masalah tersebut kita bisa gunakan abstraction.

## 4 Pilar OOP

1. Encapsulation
2. Abstarction
3. Inheritance
4. Polymorphism
