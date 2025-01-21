Tags: [[android_studio_jetpack_compose]]

## State di Android Jetpack Compose

### 1. Apa itu State?

State dalam Jetpack Compose adalah data yang dapat berubah seiring waktu dan mempengaruhi tampilan UI. Ketika state berubah, Compose akan secara otomatis memperbarui UI untuk mencerminkan perubahan tersebut.

### 2. State vs Variable

Perbedaan utama antara state dan variable biasa:

- State: Perubahan nilainya memicu rekomposisi UI
- Variable: Perubahan nilainya tidak mempengaruhi UI secara otomatis

### 3. Syntax

Syntax dasar untuk mendefinisikan state dalam Compose:

```kotlin
var myState by remember { mutableStateOf(initialValue) }
```

### 4. Kata Kunci 'by'

'by' adalah operator delegasi dalam Kotlin. Dalam konteks state, 'by' mendelegasikan getter dan setter ke objek MutableState yang dihasilkan oleh mutableStateOf().

### 5. remember

'remember' adalah fungsi yang menyimpan state antar rekomposisi. Ini memastikan bahwa nilai state tidak direset setiap kali komposabel dijalankan ulang.

### 6. mutableStateOf()

'mutableStateOf()' adalah fungsi yang membuat objek MutableState. Objek ini dapat diubah nilainya dan memicu rekomposisi ketika nilainya berubah.

## Contoh Penggunaan:

```kotlin
@Composable
fun Counter() {
    var count by remember { mutableStateOf(0) }
    
    Button(onClick = { count++ }) {
        Text("Count: $count")
    }
}
```

Dalam contoh di atas, 'count' adalah state yang akan memicu rekomposisi Button setiap kali nilainya berubah.
