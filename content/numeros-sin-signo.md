# Números sin signo

Además de los números normales, Kotlin posee números sin signo (conocidos en inglés como "unsigned").
Estos tipos de datos tienen el mismo nombre que los tipos numéricos enteros pero con una `U` antepuesta.

## Declaración

Para declarar un número sin signo, se debe añadir la letra `u` o `U` al final del literal.
El tipo `UInt` será inferido por defecto.

```kotlin
fun main() {
    val uInt = 42u
    println(uInt is UInt)
}
```

Para cambiarlo a los otros tipos, se debe especificar el tipo de dato.

```kotlin
val uByte: UByte = 42u
val uShort: UShort = 42u
val uLong: ULong = 42u
```

## Tabla informativa

Una característica importante de los números sin signo es que su valor mínimo es `0` y su valor máximo es mayor que el de los con signo, debido a que estos tipos [eliminan el bit utilizado para almacenar el signo](https://spa.kagutech.com/3935043-representation-of-numbers-in-the-computer-representation-of-integers-and-real-numbers-in-computer-memory).

|Tipo de dato|Tamaño (en bits)|Valor mínimo|Valor máximo|
|-|-|-|-|
|`UByte`|8|0|2⁸ - 1|
|`UShort`|16|0|2¹⁶ - 1|
|`UInt`|32|0|2³²- 1|
|`ULong`|64|0|2⁶⁴ - 1|

## Constantes de utilidad

Estos tipos poseen las mismas constantes de utilidad `MAX_VALUE`, `MIN_VALUE` y `SIZE_BITS` de los tipos numéricos con signo.

```kotlin
fun main() {
    println("UByte")
    println(UByte.SIZE_BITS)
    println(UByte.MAX_VALUE)
    println(UByte.MIN_VALUE)

    println("UShort")
    println(UShort.SIZE_BITS)
    println(UShort.MAX_VALUE)
    println(UShort.MIN_VALUE)

    println("UInt")
    println(UInt.SIZE_BITS)
    println(UInt.MAX_VALUE)
    println(UInt.MIN_VALUE)

    println("ULong")
    println(ULong.SIZE_BITS)
    println(ULong.MAX_VALUE)
    println(ULong.MIN_VALUE)
}
```

El código anterior muestra los valores de estas constantes.

```text
UByte
8
255
0
UShort
16
65535
0
UInt
32
4294967295
0
ULong
64
18446744073709551615
0
```