# Comentarios

Los comentarios son declaraciones explicativas utilizadas para describir el código fuente.
Su objetivo principal es hacerlo más fácil de entender para otros programadores, a menudo explicando preguntas como "¿para qué se escribió este código?" o "¿qué hace este código?" en casos de código complejo.
No afectan la ejecución del código.

## Comentarios de una línea

Un comentario de una sola línea comienza con `//`.
La mayoría de editores de código marcan los comentarios con su propio color, distinto al del resto de código.

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

Los comentarios no son reconocidos si se escriben dentro de un `String`.

```kotlin
// Este es un comentario
println("// Este no es un comentario")
```

También es muy común poner comentarios al final de una línea, para explicar el código que está antes de él.

```kotlin
var edad = 33 // Edad del cliente
```

## Comentarios multilínea

Si se necesita un comentario más largo que abarque múltiples líneas, se debe escribir comenzando con `/*` y terminando con `*/`.

```kotlin
/* Este es un
comentario
multilínea */
```

También es común identar el contenido del comentario con algunos `*`, con el fin de mantener el orden del texto.
Esta tarea es realizada automáticamente por muchos IDEs y editores de código.

```kotlin
/* 
 * Este es un
 * comentario
 * multilínea
 */
```

## Otros usos

Los comentarios no tienen fines meramente explicativos.
También se pueden usar para esconder líneas de código, con el propósito de probar su funcionamiento.

```kotlin
fun main() {
    // print("Hola mundo")
    print("Probando código...")
}
```

Se debe recordar borrar los comentarios de este tipo después de terminar las pruebas arbitrarias de código, ya que no son de utilidad y existen herramientas mejores, como [Git](https://git-scm.com) (un sistema de control de versiones), que sirven para mantener guardado código antiguo en caso de que algún error ocurra.

## Comentarios innecesarios

Se debe recordar no abusar del uso de comentarios.
No es conveniente llenar el código de comentarios o comentar cosas que son demasiado obvias para programadores experimentados.

```kotlin
fun main() {
    // Ejemplo de comentario innecesario:

    //  Muestra el texto "hola mundo" en pantalla
    print('hola mundo')
}
```

La excepción a esta regla podría ser cuando se usan con fines educativos.
Por ejemplo, para introducir a alguien sin conocimiento sobre programación a Kotlin u otro lenguaje de programación.
Sin embargo, es importante recordar que en la práctica los comentarios de este tipo deben evitarse.
