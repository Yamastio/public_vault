Tags: [[php_oop]]

## Apa itu Instance?

- **Instance** adalah representasi atau objek nyata dari sebuah _class_.
- Ketika sebuah _class_ dideklarasikan, ia hanyalah kerangka atau template. Untuk menggunakan _class_ tersebut, kita harus membuat objek dari _class_ tersebut, yang disebut sebagai **instance**.

## Penjelasan dengan Analogi

Bayangkan _class_ adalah cetakan kue (template), dan **instance** adalah kue yang dihasilkan dari cetakan tersebut.  
Setiap kue memiliki bentuk yang sama sesuai cetakan (_class_), tetapi setiap kue bisa memiliki atribut yang berbeda (properti).

---

## Contoh Kode PHP

```PHP
<?php

// Deklarasi class
class Person {
    public $name;
    public $age;

    public function introduce() {
        return "Hi, my name is {$this->name}, and I am {$this->age} years old.";
    }
}

// Membuat instance (objek) dari class Person
$person1 = new Person(); // Instance pertama
$person1->name = "John";
$person1->age = 30;

$person2 = new Person(); // Instance kedua
$person2->name = "Doe";
$person2->age = 25;

// Mengakses method dari instance
echo $person1->introduce(); // Output: Hi, my name is John, and I am 30 years old.
echo $person2->introduce(); // Output: Hi, my name is Doe, and I am 25 years old.
```

---

## Poin Penting tentang Instance

1. **Instance Unik**
    
    - Setiap instance memiliki data/properti tersendiri yang terpisah dari instance lain.
    - Pada contoh di atas, `$person1` dan `$person2` memiliki nilai properti yang berbeda meskipun berasal dari _class_ yang sama.
2. **Kata Kunci `new`**
    
    - Digunakan untuk membuat instance dari sebuah _class_.
    - `new Person()` menciptakan objek baru berdasarkan _class_ `Person`.
3. **Instance dan Memori**
    
    - Setiap instance di alokasi dalam memori secara terpisah.
    - Instance dapat diakses melalui nama variabelnya.
