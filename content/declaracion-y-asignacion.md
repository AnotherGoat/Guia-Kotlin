# Declaración y asignación de variables

Al momento de definir una variable es normal darle un nombre y un valor, como lo que se muestra a continuación:

```kotlin
val apellido = "Pérez"
```

En este caso la variable tiene el identificador `apellido` y su valor es un `String` con el contenido `Pérez`.
Además, es una variable inmutable ya que se declaró usando la palabra `val`.

Pronto veremos cómo se pueden separar ambas operaciones.

## Declaración

La declaración consiste en inicializar o reservar el espacio en memoria que ocupa una variable cualquiera, dándole un nombre que la identifique.

```kotlin
val apellido: String
val edad: Int
```

Cabe destacar que es necesario indicarle el tipo también, para que Kotlin sepa cuanta memoria reservar.
Por defecto, Kotlin no permitirá que se intente utilizar una variable que ha sido declarada pero no inicializada.

```kotlin
fun main() {
    val x: Int
    println(x)
}
```

El código anterior no se podrá ejecutar y en vez de la salida se mostrará el siguiente mensaje de error:

```text
Kotlin: Variable 'x' must be initialized
```

Este comportamiento se puede cambiar, pero se verá a fondo más adelante.

## Asignación

Después de declarar una variable, se le puede asignar un valor.
Dicho valor debe ser un literal del tipo de dato esperado.

```kotlin
fun main(){
    val pais: String
    pais = "España"
}
```

Como se vio antes, una variable puede ser declarada y asignada en una misma línea.
En este caso no es obligatorio indicar su tipo de dato, ya que el compilador puede inferirlo por su cuenta.

```kotlin
val pais = "Francia"
```

Pero en caso de que se desee, se puede indicar su tipo explícitamente.
Esto puede hacer que el código sea más claro para otros programadores.

```kotlin
val pais: String = "Francia"
```

## Métodos y constructores

Además de literales, se puede utilizar un constructor para que Kotlin infiera el tipo de la variable automáticamente.

```kotlin
fun main() {
    // Ambos son equivalentes
    val random1 = Random()
    val random2: Random = Random()
}
```

También se puede inferir el tipo como el tipo de variable que retorna un método.

```kotlin
fun main() {
    // Ambos son equivalentes
    val arreglo1 = arrayOf(1, 2, 3)
    val arreglo2: Array<Int> = arrayOf(1, 2, 3)
}
```
