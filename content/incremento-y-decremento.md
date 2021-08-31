# Incremento y decremento

Los operadores de incremento y decremeto proveen una forma conveniente y compacta de aumentar o distiminuir el valor de una variable en `1`.
Por ejemplo, `x = x + 1` se puede reducir a `x += 1` y posteriormente a `++x` o `x++`.

El operador de incremento `++` incrementa el valor de una variable en `1` unidad.

```kotlin
fun main() {
    var prueba = 5
    ++prueba // Prueba es 6 ahora
}
```

El operador de decremento `--` reduce el valor de una variable en `1`.

```kotlin
fun main() {
    var prueba = 5
    --prueba // Prueba es 4 ahora
}
```

## Prefijo

Los operadores `++` y `--` tienen 2 usos: como prefijo y como sufijo.
Si se usan como prefijo (prefix), se aumenta/disminuye el valor antes de usarlo como argumento de una función.

```kotlin
fun main() {
    var numero = 100
    println(--numero)
    println(numero)
}
```

Esto causa que el número se disminuya en `1` antes de usar su valor con `println()`.

```text
99
99
```

Como se puede ver, el valor del número permanece igual la segunda vez que se llama a `println()`.

## Sufijo

Si se usan como sufijo (postfix), se usa como argumento de la función y después se aumenta/disminuye su valor.

```kotlin
fun main() {
    var numero = 100
    println(numero--)
    println(numero)
}
```

Esto causa que se use el valor original del número al llamarlo en `println()` y que su valor disminuya en `1` después.
La salida demuestra que el cambio en el valor original sólo es visible en la segunda llamada a `println()`.

```text
100
99
```

La diferencia entre prefijo o sufijo sólo se nota si el operador se usa como argumento de un proceso más grande, como una función o un bucle while.
