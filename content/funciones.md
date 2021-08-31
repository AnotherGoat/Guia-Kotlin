# Funciones

Las funciones son declaraciones que facilitan la reutilización de código.

## Declaración

Para declarar una función se utiliza la palabra clave `fun`, seguida del nombre de la función y de un paréntesis `()` que puede o no incluir parámetros, y del cuerpo de la función entre llaves `{}`, que incluye todos los pasos que realiza.
A continuación se muestra un ejemplo de declaración de una función.

```kotlin
fun duplicar(x: Int) {
    println(2 * x)
}
```

Esta función muestra el doble del valor que se le entrega.
Tiene el parámetro `x` de tipo `Int` y no retorna ningún valor.

Como esta función no retorna ningún valor, se puede indicar que esta indica `Unit` opcionalmente.
El siguiente código es equivalente al anterior, debido a que Kotlin infiere el tipo de retorno.

```kotlin
fun duplicar(x: Int): Unit {
    println(2 * x)
}
```

Los parámetros requieren anotaciones de tipos obligatoriamente.
A Kotlin no le gustará el siguiente ejemplo.

```kotlin
fun duplicar(x) {
    println(2 * x)
}
```

Y se indicará la necesidad de una anotación de tipos para los parámetros

```text
Kotlin: A type annotation is required on a value parameter
```

El cuerpo de la función incluye el código y se recomienda que tenga un grado de indentación mayor que el de la definición.

## Utilización

Una función puede ser utilizada después de haber sido declarada en algún lugar del código.
Si se sigue con el ejemplo de la función `duplicar()` declarada anteriormente, esta puede usarse de la siguiente forma:

```kotlin
fun main() {
    duplicar(2)
    duplicar(10)
    duplicar(-40)
}

fun duplicar(x: Int) {
    println(2 * x)
}
```

A pesar de que la función `duplicar()` fue declarada después que `main()`, no hay problema en referenciarla dentro de él.
El uso de la función anterior entrega la salida duplicada.

```kotlin
4
20
-80
```
