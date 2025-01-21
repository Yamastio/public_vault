Tags: [[php_oop]]

## Apa itu Method

- **Method** adalah fungsi yang didefinisikan di dalam sebuah **class**.
- Ketika fungsi berada di dalam class, kita menyebutnya sebagai **method**, sedangkan fungsi di luar class hanya disebut **function**.
- Method memiliki akses ke properti dan fitur class yang dideklarasikan bersamanya.

---

## Contoh Dasar Penggunaan Method

```php
class Person {
    var $first_name;
    var $country = "None";

    function sayHello() {
        return "Hello World!";
    }
}

// Membuat objek dari class
$customer = new Person;

// Menetapkan nilai properti
$customer->first_name = "Miku";

// Mengakses properti dan method
echo $customer->first_name; // Output: Miku
echo $customer->sayHello(); // Output: Hello World!
```

---

### Studi Kasus: Class dengan Beberapa Method dan Properti

Berikut adalah contoh lengkap yang menunjukkan penggunaan method, properti, dan beberapa fungsi PHP terkait class.

```php
<?php

class Student {
    var $name;     // Properti
    var $country;  // Properti

    // Method untuk menampilkan pesan
    function sayHello() {
        return "Hello, " . $this->name;
    }
}

// Membuat dua objek dari class Student
$student1 = new Student;
$student2 = new Student;

// Menetapkan nilai properti
$student1->name = "Miku";
$student2->name = "Akane";

// Menampilkan properti dan method
echo $student1->name . "<br/>"; // Output: Miku
echo $student2->name . "<br/>"; // Output: Akane

echo $student1->sayHello() . "<br/>"; // Output: Hello, Miku
echo $student2->sayHello() . "<br/>"; // Output: Hello, Akane

// Menampilkan daftar method dalam class
$class_method = get_class_methods("Student");
echo "Method milik Student: ";
echo "<pre>";
print_r($class_method);
echo "</pre>";

// Mengecek apakah method tertentu ada
if (method_exists("Student", "sayHello")) {
    echo "Method sayHello tersedia";
} else {
    echo "Method sayHello tidak tersedia";
}
```

---

### Penjelasan Kode

1. **Properti**:
    
    - `var $name` dan `var $country` adalah properti class yang dapat diakses oleh semua method di dalam class.
2. **Method**:
    
    - `sayHello()` adalah method yang mengembalikan string, termasuk properti `$name`.
3. **Membuat Objek**:
    
    - `$student1 = new Student;` membuat instance dari class `Student`.
4. **Akses Properti dan Method**:
    
    - `$student1->name` untuk mengakses properti.
    - `$student1->sayHello()` untuk memanggil method.
5. **Fungsi PHP**:
    
    - `get_class_methods("Student")`: Mengembalikan array berisi semua method dari class `Student`.
    - `method_exists("Student", "sayHello")`: Mengecek apakah method `sayHello` tersedia dalam class `Student`.

---

### Output Program

```plaintext
Miku
Akane
Hello, Miku
Hello, Akane
Method milik Student: 
Array
(
    [0] => sayHello
)
Method sayHello tersedia
```

---

## Catatan Penting

- Dalam PHP modern, lebih baik menggunakan `public`, `protected`, atau `private` sebagai pengganti `var` untuk mendeklarasikan properti.
- `$this` digunakan dalam method untuk mengakses properti atau method milik class itu sendiri.