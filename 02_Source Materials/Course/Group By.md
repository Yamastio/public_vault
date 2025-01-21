Tags: [[mysql]]

Menghitung jumlah customer dari negara indonesia

```powershell
 SELECT COUNT(id), country FROM customers
    -> GROUP BY country;
```

Dengan alias

```powershell
SELECT COUNT(id) AS `Jumlah Customers`, country
    -> FROM customers
    -> GROUP BY country;
```

Rata rata

```powershell
 SELECT AVG(age), country
    ->     -> FROM customers
    ->     -> GROUP BY country;
```

Nilai maksimal

```powershell
 SELECT MAX(age) AS `Usia Tertua`, country FROM customers
    -> GROUP BY country;
```