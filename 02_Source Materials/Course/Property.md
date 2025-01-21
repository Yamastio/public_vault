Tags: [[php_oop]]

## Property pada Class

- **Property** adalah variabel yang didefinisikan di dalam sebuah _class_ untuk menyimpan nilai yang terkait dengan objek dari _class_ tersebut.
- Property juga dikenal dengan nama **attribute**, **class variable**, atau **instance variable**.

## Poin Penting tentang Property

1. **Definisi Property**  
    Property dideklarasikan di dalam _class_ menggunakan kata kunci `var` (versi lama PHP) atau lebih baik menggunakan `public`, `private`, atau `protected` (PHP versi modern).
    
2. **Akses Property**
    
    - Property diakses menggunakan operator `->` pada objek (_instance_) dari _class_.
    - Contoh: `$customer->first_name`.
3. **Inisialisasi Nilai Default**
    
    - Property dapat didefinisikan tanpa nilai awal, atau langsung diberi nilai default.

---

## Contoh Kode: Definisi dan Akses Property

```PHP
<?php

class Person {
    var $first_name;         // Property tanpa nilai awal
    var $last_name;
    var $student = false;    // Property dengan nilai default
    var $country = "None";   // Property dengan nilai default
}

// Membuat objek (instance)
$customer = new Person();

// Memberi nilai pada property
$customer->first_name = "Hakim";

// Mengakses property
echo $customer->first_name . "<br>"; // Output: Hakim
echo $customer->country . "<br>";   // Output: None

// Mengubah nilai property
$customer->country = "Indonesia";
echo $customer->country . "<br>";   // Output: Indonesia
```

---

## Contoh Lain: Beberapa Objek dan Cek Properti

```PHP
<?php

class Student {
    var $name;                // Property tanpa nilai default
    var $country = "None";    // Property dengan nilai default
}

// Membuat beberapa instance dari class Student
$student1 = new Student();
$student2 = new Student();

// Memberikan nilai pada property setiap instance
$student1->name = "Miku";
$student2->name = "Akane";

// Menampilkan nilai property
echo $student1->name . "<br>";  // Output: Miku
echo $student2->name . "<br>";  // Output: Akane
echo $student1->country . "<br>"; // Output: None

// Mengecek properti yang dimiliki oleh class
$class_vars = get_class_vars("Student");
echo "Properti milik Student: ";
echo "<pre>";
print_r($class_vars);
echo "</pre>";

// Mengecek apakah properti tertentu ada
if (property_exists("Student", "name")) {
    echo "Properti 'name' tersedia.<br>";
} else {
    echo "Properti 'name' tidak tersedia.<br>";
}
```

---

### Output dari Contoh Kode

```plaintext
Miku
Akane
None
Properti milik Student: 
Array
(
    [name] => 
    [country] => None
)
Properti 'name' tersedia.
```

---

## Tips Penting

1. **Gunakan Visibilitas Modern**  
    Gunakan `public`, `private`, atau `protected` sebagai pengganti `var` untuk mendeklarasikan property.  
    Contoh:
    
    ```PHP
    class Student {
        public $name;         // Public property
        private $id;          // Private property
        protected $country;   // Protected property
    }
    ```
    
2. **Gunakan Constructor**  
    Untuk inisialisasi nilai properti dengan cara yang lebih terorganisir:
    
    ```PHP
    class Student {
        public $name;
        public $country;
    
        public function __construct($name, $country = "None") {
            $this->name = $name;
            $this->country = $country;
        }
    }
    
    $student1 = new Student("Miku", "Japan");
    echo $student1->name;    // Output: Miku
    echo $student1->country; // Output: Japan
    ```
    
3. **Periksa Properti**  
    Gunakan fungsi bawaan seperti `get_class_vars()` dan `property_exists()` untuk memeriksa properti dari _class_.
    
