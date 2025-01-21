Tags: [[android_studio_jetpack_compose]]

- Disetiap layout punya sifat alignment dan arragement yang berbeda
- Alignment
    - cross axis
    - Row = Vertical
    - Column = Horizontal
- Arrangement
    - Main Axis
    - Row = Horizontal
    - Column Vertical

## Alignment

Mengatur di sumbu `cross axis`, menyeberang.

- Row = Vertikal
- Column = Horizontal

| Row               | Column             |
| ----------------- | ------------------ |
| Top               | Start              |
| Center Vertically | Center Horizontaly |
| Bottom            | End                |

## Arrangement

Mengatur posisi di sumbu utama(`main axis`)

- Row = Horizontal
- Column = Vertikal

| Row                                                   | Column                                    |
| ----------------------------------------------------- | ----------------------------------------- |
| Start                                                 | Top                                       |
| Center                                                | Center                                    |
| End                                                   | Bottom                                    |
| Space Between, Space Around, Space evenly, Absolute…. | Space Between, Space Around, Space evenly |

## Box

Di dalam box adanya hanya alignment
Secara default akan mengikuti parentnya, jika ingin ubah gunakan modifier
### Box Parameters

| Top Start    | Top Center    | Top End    |
| ------------ | ------------- | ---------- |
| Center Start | Center        | Center End |
| Bottom Start | Bottom Center | Bottom end |
