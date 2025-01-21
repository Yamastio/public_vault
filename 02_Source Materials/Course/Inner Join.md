Tags: [[mysql]]

Dalam cross dan straight join, tidak bisa menggabungkan dari foreign key nya/primery key nya.

Di sini kita akan menggabungkan data `customers_id` di tabel `orders`, dengan tabel `customers` data `id`.

```php
SELECT * FROM customers
INNER JOIN orders
ON customers.id = orders.customer_id;
```