# Operadores de asignación

Los operadores de asignación permiten modificar valores de variables de forma más concisa.
Por ejemplo, la operación `x = x + 10` se puede reducir a `x += 10`.

## Operadores aritméticos

Los operadores aritméticos `+`, `-`, `*` y `/` pueden acortarse añadiendo el símbolo `=` a su lado, de la siguiente forma:

```kotlin
var x = 10

x += 1  // 11
x -= 2  // 9
x *= 3  // 27
x /= 9  // 3
```

También se pueden usar para almacenar valores en otras variables.

```kotlin
var x = 15

y = x += 20 // y = 35, x = 15
```

Esta notación también se puede usar con el operador de concatenación `+` entre `String`.

```kotlin
fun main() {
    var nombre = "Javier"
    nombre += " Fernández"
    
    println(nombre) // Javier Fernández
}
```
