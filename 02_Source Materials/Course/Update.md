Tags: [[mysql]]

```powershell
UPDATE customers
SET name="Miku", city="Tokyo", country="Japan"
WHERE id = 3;
```

Hati hati untuk `where` karena itu bisa merubah lebih dari satu column:

```powershell
UPDATE customers
SET city="Kyoto"
WHERE country = "Japan";
```

Kode diatas akan merubah semua kolom yang memiliki