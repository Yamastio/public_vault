Tags: [[mysql]]

Bisa gunakan data generator:

[https://www.mockaroo.com/](https://www.mockaroo.com/)

Pertama hapus dulu dengan truncate

```powershell
 SET FOREIGN_KEY_CHECKS = 0;
```

```powershell
TRUNCATE TABLE customers;
```

Jika sudah, ubah foreign key menjadi 1 lagi

```powershell
 SET FOREIGN_KEY_CHECKS = 1;
```

Import dengan menuliskan fullpath file yang ingin di upload

```powershell
source C://....
```

Menghitung jumlah data

```powershell
SELECT COUNT(id)
FROM customers;
```