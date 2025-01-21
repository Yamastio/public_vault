Tags: [[android_studio_jetpack_compose]]

## Modifier

Untuk mengatur tinggi , ukuran, padding, allignment

1. Cara Deklarasi
    
    ```kotlin
    modifier = Modifier.padding(22.dp).background(Color.Black)
    ```
    
2. Buat Text Clickable
    
    1. Buat variable dulu untuk listener
        
        ```kotlin
        val clickOnText={}
        ```
        
    2. di dalam parameter text
        
        ```kotlin
        Text(text = "Teks ini",
        	modifier = Modifier.clickable(onClick = clickOnText)
        ```
        
3. Preview
    
    ```kotlin
    @Preview(showBackground = true)
    @Composable
    fun namaPreviewFun(){
    	//Temanya apa dipanggil
    	LearnTextAndModifiers{
    		//Panggil fungsinya di sini
    		LearnTextFun()
    	}
    }
    ```
