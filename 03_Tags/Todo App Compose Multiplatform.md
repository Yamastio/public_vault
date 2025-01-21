Tags: [[android_project]]
Reference: [ToDoApp](https://youtu.be/1TLk36FdmMA?si=qeqhtcwOgx4eaYP7)

## Cara Membuat
### Project Setup
1. Pergi ke Web [KMP Wizard](https://kmp.jetbrains.com/)
2. Isi Project name & Project ID
3. Pilih platform Android dan IOS
4. Klik Download
5. Setelah download ekstrak zip, dan buka dengan android studio
### Material 3 Theming
7. Pergi ke Build.gradle.kts (:ComposeApp)
8. Pastikan Material 3 terinstall, defaultnya material 2, jadi ubah seperti dibawah
	```Kotlin
	implementation(compose.material3)
	```
	Jika sudah ubah, klik sync now
8.  Bisa kunjungi link web Material 3 Builder: [Material3](https://material-foundation.github.io/material-theme-builder/)
9. Atau bisa gunakan simpel color seperti berikut
	- Pergi ke App.kt, di folder
		```
		package com.nekogram.todo  
  
		import androidx.compose.animation.AnimatedVisibility  
		import androidx.compose.foundation.Image  
		import androidx.compose.foundation.isSystemInDarkTheme  
		import androidx.compose.foundation.layout.Column  
		import androidx.compose.foundation.layout.fillMaxWidth  
		import androidx.compose.material3.MaterialTheme  
		import androidx.compose.material3.darkColorScheme  
		import androidx.compose.material3.lightColorScheme  
		import androidx.compose.runtime.*  
		import androidx.compose.ui.Alignment  
		import androidx.compose.ui.Modifier  
		import androidx.compose.ui.graphics.Color  
		import org.jetbrains.compose.resources.painterResource  
		import org.jetbrains.compose.ui.tooling.preview.Preview  
		import todokmp.composeapp.generated.resources.Res  
		import todokmp.composeapp.generated.resources.compose_multiplatform  
  
		val lightRedColor = Color(color = 0xFFF57D88)  
		val darkRedColor = Color(color = 0xFF77000B)  
  
		@Composable  
		@Preview  
		fun App() {  
		    MaterialTheme {  
		        val lightColors = lightColorScheme(  
		            primary = lightRedColor,  
		            onPrimary = darkRedColor,  
		            primaryContainer = lightRedColor,  
		            onPrimaryContainer = darkRedColor,  
		        )  
		        val darkColors = darkColorScheme(  
		            primary = lightRedColor,  
		            onPrimary = darkRedColor,  
		            primaryContainer = lightRedColor,  
		            onPrimaryContainer = darkRedColor,  
		        )  
		        val colors by mutableStateOf(  
		            if (isSystemInDarkTheme()) darkColors else lightColors  
		        )  
		    }  
			MaterialTheme(colorscheme = colors){
			
			}
		}
		```
### Navigation Setup
10. 