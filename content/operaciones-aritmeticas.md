# Operaciones aritméticas

Kotlin tiene la capacidad de realizar cálculos.
Esto incluye operaciones aritméticas básicas como suma, resta, multiplicación y división.

## Operaciones básicas

Los operadores `+`, `-`, `*` y `/` representan suma, resta, multiplicación y división, respectivamente.

```kotlin
println(1 + 1)  // suma
println(5 - 2)  // resta
println(2 * 2)  // multiplicación
println(4 / 4)  // división
```

Los espacios entre los signos y los números son opcionales, pero hacen que el código sea más fácil de leer.
Todas las operaciones se pueden combinar entre sí como si fuera una calculadora.

```kotlin
print(1 + 2 - 3 + 10 - 7)
```

## Cociente y resto

Al realizar una división entre números enteros, el resultado es la parte entera que queda al realizar la división, también conocida como cociente.

```kotlin
val cociente = 7 / 2 // 3
```

Para obtener el resto al realizar una división entera entre números positivos, se debe usar el operador módulo `%`.

```kotlin
val resto = 7 % 2 // 1
```

Se puede que estas operaciones cumplen con el [teorema del resto](https://es.khanacademy.org/computing/computer-science/cryptography/modarithmetic/a/the-quotient-remainder-theorem).

```kotlin
fun main() { 
    val dividendo = 7
    val divisor = 2
    
    val cociente = dividendo / divisor
    val resto = dividendo % divisor
    
    println(dividendo == cociente*divisor + resto)
}
```

Al confirmar esta igualdad, se confirma que el resultado es correcto.

```text
true
```

Lo mismo ocurre para números negativos, como el ejemplo a continuación.

```kotlin
fun main() { 
    val dividendo = -19
    val divisor = -5
    
    val cociente = dividendo / divisor
    val resto = dividendo % divisor
    
    println(dividendo == cociente*divisor + resto)
}
```

## Divisores

Un uso común de el operador `%` es para saber si un número es divisor de otro

```kotlin
fun main() { 
    println(10 % 2) // Usado para saber si es par o impar
    println(15 % 3)
    println(16 % 7)
}
```

En el caso mostrado anteriormente, se infiere que 10 es múltiplo de 2, que 15 es múltiplo de 3 y que 16 no es múltiplo de 7, debido a la salida.

```text
0
0
2
```
