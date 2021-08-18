# Booleanos

El término "booleano" proviene del álgebra de Boole, una rama del álgebra que esquematiza las operaciones lógicas.
En el álgebra booleana las variables sólo pueden tener los valores "verdadero" y "falso", a menudo representados como 1 y 0.

## El tipo Boolean

El tipo de dato `Boolean` sólo puede contener 2 posibles valores: `true` y `false`.
Se pueden declarar directamente, aunque esto no es de utilidad en la mayoría de los casos.

```kotlin
var verdadero = true
var falso = false
```

Su uso más común es como el resultado obtenido después de realizar comparaciones, por ejemplo, usando el operador de igualdad `==`.

```kotlin
fun main() {
    println(0 == 0)
    println(1 == 2)
    println("hola" == "hola")
}
```

El resultado de las operaciones anteriores se muestra como un `Boolean`.

```kotlin
true
false
true
```

Se debe tener cuidado de no confundir el operador de asignación `=` con el operador de igualdad `==`.

```kotlin
fun main() {
    println(-10 = 10)
}
```

Kotlin siempre le recordará al programador cuando encuentre sintaxis incorrecta, como la mostrada en el bloque de código anterior.

```text
Assignments are not expressions, and only expressions are allowed in this context
```

## Equivalencia con 1 y 0

En algunos lenguajes de programación, se considera que `1` y `true` son el mismo valor, y que `0` y `false` son equivalentes también.
Esto a veces se conoce como "truthy" y "falsy", pero no ocurre en el caso de Kotlin.

```kotlin
fun main() {
    println(1 == true)
}
```

El compilador detectará este error para evitar cualquier problema futuro.

```text
Kotlin: Operator '==' cannot be applied to 'Int' and 'Boolean'
```
