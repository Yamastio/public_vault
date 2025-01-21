Tags: [[mysql]]

## Order by

```powershell
 SELECT * FROM customers
    -> ORDER BY name LIMIT 20;
```

```powershell
 SELECT * FROM customers
    -> ORDER BY name DESC LIMIT 20;
```

```powershell
 SELECT * FROM customers
    -> ORDER BY country ASC, name DESC LIMIT 50;
```