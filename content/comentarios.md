# Comentarios

Los comentarios son declaraciones explicativas utilizadas para describir el código fuente.
Un comentario de una sola línea comienza con `//`.

```kotlin
// Mi primer programa escrito en Kotlin
fun main() {
    // Declaración y asignación de una variable inmutable
    val nombre = "Juan"

    // Muestra el nombre en la pantalla
    println(nombre)
}
```

Todo el texto que va dentro de un comentario es ignorado por el compilador, incluso si tiene apariencia de código real.

```kotlin
// El siguiente código es ignorado:
// println("Buenos días")
```

Los comentarios no son reconocidos si se escriben dentro de un String.

```kotlin
// Este es un comentario
println("// Este no es un comentario")
```

# Comentarios multilínea

Si se necesita un comentario más largo que abarque múltiples líneas, se debe escribir de la siguiente forma:

```kotlin
/* Este es un
comentario
multilínea */
```
