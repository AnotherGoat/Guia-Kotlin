# Operaciones entre enteros y reales

Al realizar operaciones entre variables del mismo tipo, el tipo de dato no cambia.
Pero al realizar operaciones entre tipos numéricos distintos el tipo de dato no puede mantenerse por razones obvias.

## Operaciones entre tipos distintos

Algunos lenguajes de programación convierten automáticamente el tipo de dato al que pueda almacenar más valores.
En Kotlin ocurre lo mismo.

```kotlin
fun main() {
    val num1: Double = 55.55
    val num2: Long = 100_000
    
    val resultado1 = num1 + num2
    println(resultado1.javaClass) // Double
    
    val num3: Int = 42
    val num4: Byte = 100
    
    val resultado2 = num3 + num4
    println(resultado2.javaClass) // Int
}
```

Al ejecutar el segmento de código anterior, se mostrará la clase con la que se guardan en Kotlin.
Siempre se prioriza el tipo de dato más grande en tamaño, con el fin de intentar mantener la mayor cantidad de precisión posible.

Al trabajar con tipos de datos enteros y no enteros, siempre se priorizará el tipo de punto flotante.

```kotlin
fun main() {
    val num1: Float = 0.82381f
    val num2: Long = 999_999
    
    val resultado = num1 + num2
    println(resultado.javaClass) // Float
}
```

Sin embargo, esto no ocurre al realizar operaciones entre tipos con signo y sin signo.

```kotlin
fun main() {
    val num1: UInt = 918_239_412u
    val num2: Long = 100_000
    
    val resultado = num1 + num2
    println(resultado.javaClass)
}
```

Kotlin mostrará el siguiente mensaje para notificar al programador.

```text
Kotlin: Type mismatch: inferred type is Long but UInt was expected
```
