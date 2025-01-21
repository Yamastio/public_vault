Tags: [[mysql]]

Fungsi: Kolom referensi, untuk melakukan relasi antar tabel

Contoh: dalam data kelas akan memiliki beberapa data siswa, kita harus mendeklarasikan id dari tabel kelas sebagai kunci penghubung

Membuat table kelas

```powershell
CREATE TABLE kelas(

id INT NOT NULL AUTO_INCREMENT,

nama VARCHAR(2),

PRIMARY KEY(id);
```

Hapus data siswa dulu

```powershell
DROP TABLE siswa;
```

Buat table siswa

```powershell
CREATE TABLE siswa(

id INT NOT NULL AUTO_INCREMENT,

kelas_id INT NOT NULL, 

nama VARCHAR(50) NOT NULL,

PRIMARY KEY(id),

FOREIGN KEY(kelas_id) REFERENCES kelas(id)

);
```