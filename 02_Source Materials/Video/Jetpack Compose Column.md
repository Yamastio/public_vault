Tags: [[android_studio_jetpack_compose]]

## Column in Android Jetpack Compose

In Jetpack Compose, a Column is a layout composable that arranges its children vertically. It's one of the fundamental building blocks for creating user interfaces in Compose.

## Basic Usage

```kotlin
Column {
    Text("First item")
    Text("Second item")
    Text("Third item")
}
```

## Key Properties

- **verticalArrangement:** Controls the vertical spacing between children
- **horizontalAlignment:** Determines how children are aligned horizontally
- **modifier:** Applies modifications like padding, background, etc.

## Example with Properties

```kotlin
Column(
    modifier = Modifier
        .fillMaxSize()
        .padding(16.dp),
    verticalArrangement = Arrangement.SpaceBetween,
    horizontalAlignment = Alignment.CenterHorizontally
) {
    Text("Top")
    Text("Center")
    Text("Bottom")
}
```

## Nesting

Columns can be nested within other layout composables, including other Columns:

```kotlin
Column {
    Text("Main Column")
    Row {
        Text("Nested Row")
    }
    Column {
        Text("Nested Column")
    }
}
```

Understanding how to use Column effectively is crucial for building flexible and responsive layouts in Jetpack Compose.