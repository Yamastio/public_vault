Tags: [[mysql]]

## LEFT DAN RIGHT

Pada saat ingin menggabungkan tabel, yang akan di prioritaskan banyak nya itu sebelah kiri atau kanan, jika nilai lebih sedikit akan muncul nilai null

```php
SELECT customers.id, customers.name, orders.date
FROM customers
LEFT JOIN orders
ON customers.id = orders.customer_id
LIMIT 10;
```

```php
SELECT customers.id, customers.name, orders.date
FROM customers
RIGHT JOIN orders
ON customers.id = orders.customer_id
LIMIT 10;
```