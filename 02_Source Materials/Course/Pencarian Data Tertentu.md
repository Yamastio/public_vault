Tags: [[mysql]]

Pencarian country Indonesia

```powershell
 SELECT * FROM customers
    -> WHERE country = "Indonesia";
```

```powershell
SELECT* FROM customers
    -> WHERE id < 5;
```

Negasi

```powershell
 SELECT* FROM customers
    -> WHERE NOT country = "Indonesia" LIMIT 10;
```

```powershell
SELECT* FROM customers
    -> WHERE country IN ("Indonesia", "Russia", "German", "Japang") LIMIT 10;
```

Like

```powershell
 SELECT* FROM customers
    -> WHERE city LIKE "ber%";
```

```powershell
SELECT* FROM customers
    -> WHERE city LIKE "%lin";
```

```powershell
SELECT* FROM customers
    -> WHERE city LIKE "%ne%";
```