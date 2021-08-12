# Variables inmutables

Además de las variables mutables, Kotlin permite la creación de variables inmutables.
Para declarar una variable inmutable es necesario usar la palabra clave val.

```kotlin
val nombre = "Juan"
println(nombre)
```

Se diferencia de las variables mutables en que su valor sólo puede ser asignado una vez.

```kotlin
fun main() {
    val decimal = 3.14
    decimal = 1.5
}
```

El codigo anterior no se podrá ejecutar ya que el compilador detectará el error y mostrará el siguiente mensaje, interrumpiendo cualquier intento de ejecución:

```
Kotlin: Val cannot be reassigned
```

Si se quiere almacenar un dato mutable, se debe usar la palabra var, en caso contrario, se recomienda usar val.
