Tags: [[mysql]]

Fungsi unique key: Untuk menentukan suatu kolom bernilai unik

Perbedaan dengan Primary key: Hanya untuk menyimpan data unik, tanpa menjadi identitas dari suatu data, kita bisa beri lebih dari 1 unique key

Cara Menambahkan

```powershell
CREATE TABLE penduduk (

id INT NOT NULL AUTO_INCREMENT,

nik VARCHAR(50) NOT NULL,

PRIMARY KEY(id),

UNIQUE KEY(nik)

);
```

Menambahkan unique key

```powershell
ALTER TABLE

siswa

ADD COLUMN no_induk VARCHAR(10);
```

Menambahkan unique key pada no_induk

```powershell
ALTER TABLE siswa

ADD UNIQUE KEY(no_induk, name, id);
```

Menghapus

```powershell
ALTER TABLE siswa
DROP INDEX no_induk;
```