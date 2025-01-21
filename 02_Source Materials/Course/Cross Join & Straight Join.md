Tags: [[mysql]]

Cross Join

```powershell
> SELECT * FROM products
    -> CROSS JOIN customers
    -> LIMIT 10;
```

Straight Join, kita bisa tambahkan clausa where

```php
> SELECT * FROM customers
    -> STRAIGHT JOIN orders
    -> WHERE orders.customer_id = 1
    -> LIMIT 10;
```