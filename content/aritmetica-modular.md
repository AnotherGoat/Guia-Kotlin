# Aritmética modular

***Esto ocurre en Python, se debe corregir.

En los ejemplos anteriores se debe asegurar que tanto el dividendo como el divisor sean positivos.
Esto ocurre porque el operador `%` no sólo sirve para calcular el resto, ya que en realidad su función proviene de la [aritmética modular](https://es.khanacademy.org/computing/computer-science/cryptography/modarithmetic/a/what-is-modular-arithmetic).

## Operador módulo

El siguiente código muestra que `11 mod 5 = 6 mod 5 = 1 mod 5 = -4 mod 5 = -9 mod 5`, tal como ocurre en aritmética modular.

```kotlin
fun main() {
    println(11 % 5)
    println(6 % 5)
    println(1 % 5)
    println(-4 % 5)
    println(-9 % 5)
}
```

Esto se puede ver en la salida, debido a que muestra la misma para todos.

```text
```
