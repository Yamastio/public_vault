Tags: [[php_oop]]

## Membuat dan Menggunakan Instance

Instance adalah objek yang dibuat dari suatu class. Dalam PHP, instance memungkinkan kita untuk mengakses properti dan method dari class.

### Contoh Kesalahan pada Akses Properti:

```php
class Person {
    var $first_name;
    var $last_name;

    function fullName() {
        return $first_name . ' ' . $last_name; // Kesalahan: Tidak menggunakan $this
    }
}

$p = new Person;
$p->first_name = "Akane";
$p->last_name = "Miku";

echo $p->fullName; 
// Notice: Undefined variable: first_name, last_name
```

### Mengapa Error Terjadi?

1. **$first_name** dan **$last_name** dalam method `fullName()` tidak diakses melalui `$this`.
2. **$this** adalah referensi ke instance saat ini. Properti atau method dalam class harus diakses dengan `$this->property` di dalam method.

---

## Solusi: Gunakan `$this`

```php
class Person {
    var $first_name;
    var $last_name;

    function fullName() {
        return $this->first_name . ' ' . $this->last_name; // Menggunakan $this
    }
}

$p = new Person;
$p->first_name = "Akane";
$p->last_name = "Miku";

echo $p->fullName(); // Output: Akane Miku
```

---

## Implementasi yang Benar

Berikut implementasi lengkap dengan properti dan method dalam class:

```php
<?php

class Student {
    var $firstName;  // Properti pertama
    var $lastName;   // Properti kedua

    // Method untuk menampilkan sapaan
    function sayHello() {
        return "Hello, Miku!";
    }

    // Method untuk menggabungkan nama depan dan belakang
    function fullName() {
        return $this->firstName . ' ' . $this->lastName; // Properti diakses dengan $this
    }
}

// Membuat instance dari class Student
$student1 = new Student;

// Menetapkan nilai untuk properti
$student1->firstName = "Nakano";
$student1->lastName = "Miku";

// Memanggil method
echo $student1->sayHello() . "<br/>"; // Output: Hello, Miku!
echo $student1->fullName() . "<br/>"; // Output: Nakano Miku
```

---

### Catatan Penting

1. **Properti diakses dengan `$this->property`** di dalam method. Tanpa `$this`, PHP menganggapnya sebagai variabel lokal.
2. **Memanggil Method**:
    - Menggunakan `$object->methodName()`.
3. **Memodifikasi Properti**:
    - `object->property = value;`.

Dengan mengikuti aturan ini, Anda bisa menghindari error terkait properti atau method saat menggunakan instance.