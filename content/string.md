# Cadenas de caracteres

Las cadenas de caracteres son una secuencia ordenada e inmutable de caracteres y son uno de los tipos de datos más importantes en la programación.

## El tipo String

El tipo de dato de las cadenas de caracteres es su nombre en inglés, `String`.
Estas se definen como cualquier texto escrito entre comillas dobles.

```kotlin
val apellido = "Martínez"
```

## Conversión a String

Los métodos `println()` y `print()` funcionan con cualquier tipo de dato porque realizan una conversión de ellos al tipo `String` mediante el método `toString()`.

```kotlin
fun main() {
    println("Hola mundo") // String
    println(true) // Convertido implícitamente a String
    println(22.15) // Convertido implícitamente a String
}
```

Algunos IDEs detectarán el siguiente código como redundante, debido a este motivo.

```kotlin
fun main() {
    print(11223344.toString())
}
```
