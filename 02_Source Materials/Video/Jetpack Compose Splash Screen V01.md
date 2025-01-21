Tags: [[android_studio_jetpack_compose]]

## SplashScreen

1. Gunakan API, build gradle
    
    ```kotlin
    Implementation("androidx.core:core-splashscreen:1.0.0")
    ```
    
2. Buat warna background di directori `values` di dalam file `colors.xml`
    
3. Masukan icon gambarnya
    
    - Branded Image : 200 x 80 dp
    - Icon with background:
        - 240 x 240 dp → background
        - 160 dp → icon
    - Icon without background:
        - 288 x 288 dp
        - 192 dp
4. Di bagian `Themes.xml` = pastikan parent, no Action bar
    
5. Masukan style baru
    
    ```kotlin
    <style name = "Theme.MySplashScreen" parent="Theme.SplashScreen">
    windowSplashScreenBackground -> warna di color.xml
    windowSplashScreenAnimation -> icon
    postSplashScreenTheme -> tema yang akan muncul setelah splashscreen
    </style>
    
    ```
    
6. Ke `Manifest.xml` → ubah theme ke “MySplashScreen”. Di application & Activity
    
7. ke `MainActivity.kt` tambahkan
    
    ```kotlin
    installSplashScreen()
    ```
    
    Sebelum set content.
