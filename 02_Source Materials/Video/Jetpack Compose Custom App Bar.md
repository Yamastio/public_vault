Tags: [[android_studio_jetpack_compose]]

## Cara Membuat
1. Pergi ke `color.kt` → buat variabel warna baru
    
    ```kotlin
    val greenJC = Color(....)
    ```
    
2. Pergi ke `theme.kt`
    
    1. Ubah primary color
        
        ```kotlin
        primary = greenJC
        ```
        
    2. Ubah jadi format integer
        
        ```kotlin
        val view = LocalView.current
        if(!view.isInEditMode){
        	window.statusBarColor = greenJC.toArgb()
        	windowCompact.getInsetController(window,view).isAppearanceLightStatusBar = darkTheme
        }
        ```
        
3. Masukan Icon ke drawable jika dibutuhkan(.xml/.png)
    
4. Buat di MainActivity.kt
    
    ```kotlin
    @Composable
    fun LearntTopAppBar(){
    	TopAppBar(title = {/*TODO*/})
    }
    ```
    
    Jika ada error bisa klik Opt in for Experimental ….
    
    1. Buat Parameter untuk navigationIcon(disebelah kiri title)
        
        ```kotlin
        TopAppBar(
        	title={Text(text = "WhatsApp")}),
        	navigationIcon ={
        		IconButton(onClick={/*TODO*/})
        		Icon(painter= ...., contentDescription="")
        	}
        )
        ```
        
    2. buat parameter color untuk TopAppBar
        
        ```kotlin
        colors = TopAppBarDefaults.topAppBarColors(
        	containerColor = greenJC,
        	titleContentColor = Color.White,
        	navigationIconColor = Color.white
        )
        ```
        
    3. Menambahkan 3 icon (Sebelah kanan title) → parameter actions
        
        ```kotlin
        actions={
        	IconButton(onClick = {Toast.makeText("Profile")}){
        		//gunakan vector bawaan
        		Icon(imageVector = Icons.Filled.PilihBebas, contentDescription = "Profile", tint = Color.White)
        } x 3: buat sendiri dengan cara yang sama
        ```
        
5. Komentar untuk modifier = Modifier.fillMaxSize() in surface
    
    Karena akan mengambil seluiruh layar(fillMaxSize)
