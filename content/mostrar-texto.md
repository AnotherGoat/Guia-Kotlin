# Mostrar texto en pantalla

Las forma más sencilla de mostrar texto en pantalla es utilizando las funciones `print()` y `println()`.
La función `println()` muestra el texto que se le entregue y añade un salto de línea al final.

```kotlin
fun main() {
    println("Hola")
    println("mundo")
    println("123")
}
```

La salida muestra cada mensaje en una línea separada:

```
Hola
mundo
123
```

La función `print()` realiza la misma acción pero sin añadir un salto de línea al final.

```kotlin
fun main() {
    print("Hola")
    print("mundo")
    print("123")
}
```

A diferencia del caso anterior, la salida queda toda en una misma línea.

```
Holamundo123
```

# Punto y coma

En Kotlin no es necesario finalizar cada línea de código con un punto y coma `;`, al contrario de otros lenguajes de programación como Java, C++ o C#.
Ambos ejemplos mostrados a continuación son válidos y equivalentes.

```kotlin
println("Hola");
println("Hola")
```

De este modo, el uso de `;` al final de cada sentencia queda como opcional.
Sin embargo, puede ser de utilidad si por algún motivo se desea escribir 2 líneas de código en una sola.

```kotlin
println("Hola"); println("mundo")
```
