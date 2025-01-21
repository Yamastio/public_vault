Tags: [[android_studio_jetpack_compose]]

## Jetpack Compose

```kotlin
@Composable
fun MyFirstText(name: String){
	Text(text= "Hello $name")
}
```

### Preview

```kotlin
@Composable
@Preview
fun MyFirstTextPreview(){
	MyFirstText("Stevda-san")
}
```