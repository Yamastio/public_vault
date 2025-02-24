---
id: finding_stuf
aliases: []
tags: []
---

## Mencari dengan locate

```bash
locate aircrack-ng
```

- Kadang kurang akurat
- Jika baru saja membuat file, maka tidak akan muncul
- File yang baru dibuat akan bisa dicari apabila sudah 1 hari dibuat

## Mencari Binary dengan whereis

```bash
whereis aircrack-ng
```

## Mencari binary file di path variable dengan which

```bash
which aircrack-ng
```

## Mencari dengan find

```bash
find directory options expression
```

```bash
find / -type f -name apache2
```

## Filtering with grep

- mencari keyword tertentu
- Bisa digunakan bersamaan dengan piping/pipe

```bash
ps aux
```

- ps aux untuk list semua proses yang berjalan di sistem
- kombinasi dengan grep

```bash
ps aux | grep apache2
```
