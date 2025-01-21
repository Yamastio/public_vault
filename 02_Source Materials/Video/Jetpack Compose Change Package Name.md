Tags: [[android_studio_jetpack_compose]]

For example, if you want to change `com.example.app` to `my.awesome.game`, then:

1. In your _**Project panel**_, click on the little gear icon (  )
    
    ![https://i.sstatic.net/lkezT.png](https://i.sstatic.net/lkezT.png)
    
2. Uncheck the `Compact Empty Middle Packages` option
    
    ![https://i.sstatic.net/QjMZC.png](https://i.sstatic.net/QjMZC.png)
    
3. Your package directory will now be broken down into individual directories
    
4. Individually select each directory you want to rename, and:
    

- Right-click on it
    
- Select `Refactor`
    
- Click on `Rename`
    
- In the pop-up dialog, click on `Rename Package` instead of Rename Directory
    
- Enter the new name and hit **Refactor**
    
- Click **Do Refactor** in the bottom
    
- Allow a minute to let Android Studio update all changes
    
- _Note: When renaming `com` in Android Studio, it might give a warning. In such case, select_ **Rename All**
    
    ![https://i.sstatic.net/EKDWw.png](https://i.sstatic.net/EKDWw.png)
    

1. Now open your _**Gradle Build File**_ (`build.gradle` - Usually `app` or `mobile`). Update the `applicationId` in the `defaultConfig` to your new Package Name and Sync Gradle, if it hasn't already been updated automatically:
    
    ![https://i.sstatic.net/mu8UY.png](https://i.sstatic.net/mu8UY.png)
    
2. You may need to change the `package=` attribute in your manifest.
    
    ```xml
    xml
    Salin kode
    <manifest xmlns:android="<http://schemas.android.com/apk/res/android>"
        xmlns:tools="<http://schemas.android.com/tools>"
        package="my.awesome.game">
    
        <!-- isinya seperti biasa -->
    </manifest>
    
    ```
    
3. Clean and Rebuild.
    
    ![https://i.sstatic.net/xBqWu.png](https://i.sstatic.net/xBqWu.png)
    
4. _**Done!**_ Anyway, Android Studio needs to make this process a little simpler.
