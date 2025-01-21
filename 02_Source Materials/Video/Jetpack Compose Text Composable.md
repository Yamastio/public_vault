Tags: [[android_studio_jetpack_compose]]

## Cara Deskripsikan

1. Langkah pertama
    
    ```kotlin
    @Composable
    fun NamaFungsi(){
    	Text(text="")
    }
    ```
    
    Beberapa paramerter: text, color, fontsize, modifier
    
    ```kotlin
    @Composable
    fun NamaFungsi(){
    	Text(text="Hello World", color= Color.Red)
    }
    ```
    
2. Panggil di set content
    
    ```kotlin
    setContent{
    	LearnTextModifierTheme{
    		Surface(
    			modifier = modifier.fillMaxSize(),
    			color = MaterialTheme.colorScheme.background\\
    			){
    				//Panggil di sini
    				NamaFungsi();
    			}
    		}
    	}
    				
    		
    ```
    

## Cara deklarasikan di `string.xml` (String Resource)

1. Buat resource di `string.xml`
    
    ```kotlin
    <string name= "namaStringXml"> Hello ini adalah text nya</string>
    ```
    
2. Deklarasikan di mainActivity.kt
    
    ```kotlin
    Text(text= StringResource(id = R.String.namaStringXml))
    ```
