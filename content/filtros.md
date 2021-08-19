

## Filtrar una lista

```kotlin
val nums = arrayOf(-1, 2, 4, -10, 25, -33, -2, -21, 44)
val positives = nums.filter { x -> x > 0 }
```

```kotlin
val nums = arrayOf(-1, 2, 4, -10, 25, -33, -2, -21, 44)
val positives = nums.filter { it > 0 }
```
