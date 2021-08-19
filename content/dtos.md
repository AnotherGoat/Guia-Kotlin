
```kotlin
data class Cliente(val nombre: String, val correo: String)
```

Este ejemplo crea una clase DTO de nombre `Cliente` con las siguientes funcionalidades:

- getters
- `equals()`
- `hashCode()`
- `toString()`
- `copy()`
- `component1()`, `component2()`, etc. para todas las propiedades

## DTO con setters

Para crear un DTO que además tiene setters, simplemente se debe reemplazar `val` por `var`.

```kotlin
data class Cliente(var nombre: String, var correo: String)
```
