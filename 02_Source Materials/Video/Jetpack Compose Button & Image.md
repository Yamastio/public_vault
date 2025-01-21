Tags: [[android_studio_jetpack_compose]]

## Button

Ketika membuat button pastikan sudah berada di dalam layout agar tidak memenuhi layar

### Cara buat

1. Buat layout dulu, di dalam nya isikan
    
    ```kotlin
    Button(ketikaDiKlik = {Ekspresi ketika di klik, paramteter lain()}{
    	//isi dari button nya
    	Text(text = "Login")
    ```
    

### Toast

1. Buat variable Local Context
    
    ```kotlin
    val context = LocalContext.current.applicationContext
    ```
    
2. Listener
    
    ```kotlin
    onClikc = {Toast.makeText(context, text:"Login Sukses", Toast.LENGT_SHORT).show()}
    ```
    

## Image

1. Cara deklare
    
    ```kotlin
    @Composable
    fun LearnImage(){
    	Image(painter = ..., contentDescription = ...)
    }
    ```
    
    ```kotlin
    @Composable
    fun LearnImage(){
    	Image(painter = painterResource(id = R.drawable.namaGambar), contentDescription = "Ini deskripsi gambar, digunakan untuk backend nantinya")
    }
    ```
