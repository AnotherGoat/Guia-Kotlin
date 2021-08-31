# Funciones de arreglos

Otra forma de trabajar con arreglos es con las funciones que proporciona el lenguaje.
Aquí se muestran algunas de las más comunes.


## Conversión a String

Una forma de convertir un `Array` a `String` es utilizando el método `joinToString()`.

```kotlin
fun main() {
    val resultados = booleanArrayOf(true, false, true)
    println(resultados.joinToString())
}
```

La salida se mostrará con el separador `, ` (una coma seguida de un espacio en blanco).

```kotlin
true, false, true
```

Alternativamente, se le puede entregar un separador personalizado.

```kotlin
fun main() {
    val resultados = booleanArrayOf(true, false, true)
    println(resultados.joinToString(" -- "))
}
```

En este caso, el resultado se mostrará con el nuevo separador.

```kotlin
true -- false -- true
```

Para realizar el mismo proceso con arreglos multidimensionales, se puede usar el método `contentDeepToString()`.

```kotlin
val identidad = arrayOf(
    arrayOf(1, 0, 0),
    arrayOf(0, 1, 0),
    arrayOf(0, 0, 1),
)
println(identidad.contentDeepToString())
```

El resultado se mostrará con corchetes `[]` para hacer más fácil la identificación de cada sub-arreglo.

```text
[[1, 0, 0], [0, 1, 0], [0, 0, 1]]
```
