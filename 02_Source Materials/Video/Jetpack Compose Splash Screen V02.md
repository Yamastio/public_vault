Tags: [[android_studio_jetpack_compose]]

## Desain in Figma

1. Select Rectangle Tool
2. Buat Rectangle ukuran 240 x 240
3. Select Elipse tool
4. Buat Elipse dengan menahan `alt+shift` dan buat ukuran 160 x 160
5. Posisikan lingkaran berada di tengah tengah kotak
6. Import image icon, posisikan agar tidak keluar dari lingkaran tadi
7. Hapus Lingkaran
8. Hapus warna dari rectangle, buat jadi trasnparant
9. Pilh semua rectangle dan icon
10. Tekan `ctrl+g` untuk group
11. Export jadi `svg` file

## SplashScreen

1. Import icon ke dir `drawable` , vector asset
    
2. Tambahkan API di `build.gradle`
    
    ```kotlin
    implementation "androidx.core:core-splashscreen:1.0.0"
    ```
    
3. Buat `splash.xml` file di directori `values`
    
    ```kotlin
    <xml? version="1.0" encoding="utf-8"?
    <resources>
    	<style name="Theme.MyApp.MySplash" parent="Theme.SplashScreen">
    		<item name= "windowSplashScreenBackground">#FFFF</item>
    		<item name= "windowSplashScreenAnimatedIcon">@drawable/logo</item>
    		<item name= "windowSplashScreenTheme">@style/Theme.CompTest</item>
    	</style>
    ```
    
4. Buat `splash.xml(night)` file, qualifiers ubah ke `night`
    
5. ke `AndroidManifest.xml` pastikan `theme` yang digunakan sama
    
    ```kotlin
    <activity
    	android:name= ".MainActivity"
    	android:exported="true"
    	android:theme="@style/Theme.MyApp.MySplash">
    ```
    
6. Pergi ke `MainActivity.kt` tambahkan
    
    ```kotlin
    installSplashScreen()
    ```
    
    Sebelum `set Content()`
