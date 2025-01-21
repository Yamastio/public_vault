Tags: [[java_oop]]
## Class

Class ini mirip dengan struct di bahasa C

```C
struct Car {
	char Brand[100];
	int year;
	char model[100];
	short seats;
};
```

- Seperti blueprint
- Seperti cetakanya
- Secara aturan itu ditulis dengan Huruf Capital di Huruf pertamanya
- Menggunakan Cammel Case juga
- Nama class seharusnya adalah Kata Benda
- Clas: Car

## Object

```C
struct Car car1, car2;
```

- Object hasil aslinya
- Object tidak perlu Capital letter
- Object: Audi, Nissan, Volvo

## Java vs C

- Di C, struct itu disimpan di memory stack
- Di java, object disimpan di memory heap
- Di java, untuk class nya itu hanya code biasa, tidak disimpan di memory heap juga. Sedangkan Object tersimpan di memory Heap

## Aturan Class Di Java

- Satu class itu satu file, tidak bisa satu file itu berisi dua class
- Nama class dan nama file nya harus sama persis