Tags: [[android_studio_jetpack_compose]]

## Cara Membuat
```kotlin
@Composable
fun customText(){
	Text(text="Hello World!")
}
```

Secara default text tidak bisa di select. Maka dari itu kita perlu memasukan ke SelectionContainer

```kotlin
@Composable
fun customTextSelection(){
Column{
	SelectionContainer{
		Text(text="Hello World!")
		}
	}
}
```

### Disabled selection:
Untuk menonaktifkan seleksi teks

```kotlin
@Composable
fun customTextSelection(){
Column{
	SelectionContainer{
		DisableSelection{
			Text(text="Hello World!")
			}
		}
		Text(text="Hello World!")
	}
}
```
