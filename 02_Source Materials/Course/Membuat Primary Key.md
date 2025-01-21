Tags: [[mysql]]

Fungsi : Identitas unik, sebagai kunci referensi antara tabel

Cara membuat

```php
	CREATE TABLE anggota( 
	id INT NOT NULL AUTO_INCREMENT, 
	nama VARCHAR(50) NOT NULL, 
	PRIMARY KEY(id));
```

```sql
MariaDB [mysql_latihan]> DESCRIBE anggota
    -> ;
+-------+-------------+------+-----+---------+----------------+
| Field | Type        | Null | Key | Default | Extra          |
+-------+-------------+------+-----+---------+----------------+
| id    | int(11)     | NO   | PRI | NULL    | auto_increment |
| nama  | varchar(50) | NO   |     | NULL    |                |
+-------+-------------+------+-----+---------+----------------+
```

Cara menambahkan

```sql
ALTER TABLE siswa ADD PRIMARY KEY(id);
```

Cara menghapus

```sql
ALTER TABLE siswa DROP PRIMARY KEY;
```

