Tags: [[android_studio_jetpack_compose]]

## Persiapan

1. Tambahkan dependencies
    
    ```kotlin
    implementation ("androidx.navigation:navigation-compose:2.7.6")
    ```
    
2. Tambahkan warna di file `color.kt`
    
3. Ubah warna `theme.kt` → primary & statusBar
    
4. Buat kotlin file di package nya / buat screen
    
5. Contoh isi dari screen `Home.kt`
    
    ```kotlin
    @Composable
    fun Home(){
    	Box(modifier = Modifier.fillMaxSize()){
    		Column(modifier = Modifier.fillMaxSize().align(Aligment.Center), verticalArrangement = Arrangement.Center, horizontalAlignment= Alignment.CenterHorizontally){
    			Text(text= "Home")
    		}
    	}
    }
    ```
    
    Setelah itu buat @Preview nya, dan buat untuk screen yang lainya
    
6. Buat object/class denga nama `Screens.kt` , untuk NavGraph → NavHost
    
    ```kotlin
    Sealed class Screens(val Screen: String){
    	data object Home: Screens("Home")
    	data object Profile: Screens("Profile")
    	data object Settings: Screens("Settings")
    ```
    

## mainActivity.kt

Bagian Penting → `mainActivity.kt`

- Kita akan melakukan 3 hal
    1. Membuat Navigation Drawer
    2. Membuat Top App Bar
    3. Membuat Nav Host untuk Navigasi

### Navigation Drawer

1. Inisialisasi
    
    ```kotlin
    val navigationController = rememberNavController()
    val corountineScope = rememberCoroutineScope() -> Untuk Buka tutup navbar
    val drawerState = rememberDrawerState(initialValue = DrawerValue.Closed)
    
    ```
    
2. Buat nav drawer
    
    ```kotlin
    ModalNavigationDrawer(
    	drawerState = drawerState,
      gesturesEnabled = true,
    	drawerContent = {
    		ModalDrawerSheet{
    			//awal header
    			Box(modifier = Modifier.background(GreenJC).fillMaxWidth().height(150.dp)){
    				Text(text= "Header")
    			}
    			Divider() //garis pemisah
    			//akhir header
    			
    			//awal NavDrawerItem
    			NavigationDrawerItem(
            label = {Text(text= "Home", color = LapanColor)},
    				selected = false,
    				icon = {Icon(imageVector = Icons.Default.Home, contentDescription = "Home", tint = GreenJC)},
    				onClick = {
    					corountineScope.launch{
    						drawerState.close() // nutup nav draw
    					}
    					navigationController.navigate(Screens.Home.screen){
    						popUpTo(0) // agar tidak meninggalkan screen dibelakang, biar tidak menumpuk screen
    					}
    				}
    		 )
    		){
    		//Top App Bar
    		}
    ```
    
    bisa buat navDrawer untuk yang lain
    

### TopAppBar

- Tulis di dalam kurung kurawal buka di ModalNavigationDrawer{…}
    
    ```kotlin
    ModalNavigationDrawer(NavDrawerYangDibuatDiatas){
    	//Tulis disini
    }
    ```
    

1. Buat dengan Scaffold
    
    ```kotlin
    Scaffold(
    	topBar = {
    		val coroutineScope = rememberCoroutineScope()
    		TopAppBar(title = {
    			Text(text= "WhatsApp")},
    			containerColor = GreenJC,
    			titleContainerColor = Color.White,
    			navigationIconContentColor = Color.White) //Jika ada error, klik OPT di bagian APP Bar
    		),
    		navigationIcon = {
    			IconButton(onClick = {corountineScope.launch{drawerState.open()}}){
    			  Icon(Icons.Rounded.Menu, contentDescription = "MenuButton")
    			}
    		}
    	}
    ){
    	//NavHost
    }
    			
    		
    ```
    

### NavHost

Dibuat di:

```kotlin
Scaffold(YangDibuatDiatas){
	//Buat navHost disini
}
```

Maka akan menjadi seperti dibawah

```kotlin
NavHost(navController = navigationController, startDestination = Screens.Home.screen){
	composable(Screens.Home.screen){Home()}
	composable(Screens.Profile.screen){Profile()}
	composable(Screens.Settings.screen){Settings()}
```

## Kode Full Nav Drawer, Top App Bar, Nav Host

```kotlin
val navigationController = rememberNavController()
val corountineScope = remmberCorountineScope() -> Untuk Buka tutup navbar
val drawerState = rememberDrawerState(initialValue = DrawerValue.closed)

ModalNavigationDrawer(
	drawerState = drawerState,
	gestureEnabled = true,
	drawerContent = {
		ModalDrawerSheet{
			//awal header
			Box(modifier = Modifier.background(GreenJC).fillMaxSize().height(150.dp)){
				Text(text= "Header")
			}
			Divider() //garis pemisah
			//akhir header
			
			//awal NavDrawerItem
			NavigationDrawerItem(
				label = {Text(text= "Home", color(GreenJC))},
				selected = false,
				icon = {Icon(ImageVector = Icons.Default.Home, contentDescription = "Home", tint = GreenJC)},
				onClick = {
					corountineScope.launch{
						drawerState.close() // nutup nav draw
					}
					navigationController.navigate(Screens.Home.screen){
						popUpTo(id:0) // agar tidak meninggalkan screen dibelakang, biar tidak menumpuk screen
					}
				}
		 )
		){
			//topAppBar
			Scaffold(
				topBar = {
					valCorountineScope = rememberCorouintineScope()
					TopAppBar(title = {
						Text(text= "WhatsApp")},
						containerColor = GreenJC,
						titleContainerColor = Color.White,
						navigationIconContentColor = Color.White) //Jika ada error, klik OPT di bagian APP Bar
					),
					navigationIcon = {
						IconButton(onClick = {corountineScope.launch{drawerState.open()}}){
							Icon(Icons.Rounded.Menu.contentDescription = "MenuButton")
						}
					}
				}
			){
				//NavHost
				NavHost(navController = navigationController, startDestination = Screens.Home.screen){
					composable(Screens.Home.screen){Home()}
					composable(Screens.Profile.screen){Profile()}
					composable(Screens.Settings.screen){Settings()}
				}
		}
```
