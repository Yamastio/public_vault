Tags: [[android_studio_jetpack_compose]]

## Apa kegunaan layout

Jika tidak digunakan maka tampilanya akan menumpuk satu sama lain

## Column Layout

Vertical Linear Layout

- Bellow Each other

```kotlin
Column(horizontalAlignment= Alignment.CenterHorizontal){
	Text(text = "Center Horizontal")
}
```

## Row Layout

Horizontal Linear Layout

- Beside each other

```kotlin
Row(parameters){
	content
}
```

## Box Layout

Nesting Of Layout

- Top of Each Other

```kotlin
Box(modifier = Modifier.fillMaxSize().background(Color.Yellow), contentAlignment = Allignment.Center){
	Box(modifier = Modifier.height(300.dp).width(300.dp)){
		Text = (text = "Hello Box")
	}
}
```
