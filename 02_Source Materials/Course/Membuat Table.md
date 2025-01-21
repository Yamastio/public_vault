Tags: [[mysql]]

- Membuat table
    
    1. cara 1
        
        ```php
        CREATE TABLE anggota ( id int, nama varchar(254) );
        ```
        
    2. cara 2
        
        ```php
        CREATE TABLE anggota ( 
        -> id int, 
        -> nama varchar(254) 
        -> );
        ```
        
- Menampilkan Table
    
    ```php
    SHOW TABLES;
    ```
    
- Menghapus
    
    ```php
    DROP TABLE anggota;
    ```
    
- Mengubah nama
    
    ```php
    ALTER TABLE anggota
    -> RENAME TO siswa;
    ```