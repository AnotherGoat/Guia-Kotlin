# Extremos numéricos

Todos los tipos de datos básicos en Kotlin ocupan un espacio de memoria predefinido.
Esto significa que tienen valores máximos y mínimos que no se pueden superar.
Existen tipos de datos más avanzados que no tienen estas limitaciones, pero su uso generalmente se reserva a casos más específicos.

## Tipos enteros

Los tipos de datos enteros representan números enteros, es decir, números positivos, negativos y el 0.
Existen 4 tipos de datos enteros.

|Tipo de dato|Tamaño (en bits)|Valor mínimo|Valor máximo|
|-|-|-|-|
|`Byte`|8|-128|127|
|`Short`|16|-32 768|32767|
|`Int`|32|-2 147 483 648 (-2³¹)|2 147 483 647 (2³¹- 1)|
|`Long`|64|-9 223 372 036 854 775 808 (-2⁶³)|9 223 372 036 854 775 807 (2⁶³ - 1)|

## Tipos de punto flotante

Para números reales, Kotlin proporciona los tipos de datos `Float` y `Double`.
Estos se basan en el [estándar IEEE 754](https://en.wikipedia.org/wiki/IEEE_754) que define su nivel de precisión.
Un `Float` representa un número de precisión simple y un `Double` representa un número de precisión doble, de acuerdo a lo que define el estándar mencionado.

|Tipo de dato|Tamaño (en bits)|Bits significantes|Bits del exponente|Dígitos decimales|
|-|-|-|-|-|
|`Float`|32|24|8|6-7|
|`Double`|64|53|11|15-16|

## Constantes de utilidad

Las clases contenedoras de cada tipo de dato numérico básico contienen constantes estáticas que se pueden utilizar para acceder fácilmente los valores máximos (`MAX_VALUE`) y mínimos (`MIN_VALUE`) que puede almacenar cada uno.

A continuación se muestran estas constantes:

```kotlin
fun main() {
    println("Byte")
    println(Byte.MAX_VALUE)
    println(Byte.MIN_VALUE)

    println("Short")
    println(Short.MAX_VALUE)
    println(Short.MIN_VALUE)

    println("Int")
    println(Int.MAX_VALUE)
    println(Int.MIN_VALUE)

    println("Long")
    println(Long.MAX_VALUE)
    println(Long.MIN_VALUE)

    println("Float")
    println(Float.MAX_VALUE)
    println(Float.MIN_VALUE)

    println("Double")
    println(Double.MAX_VALUE)
    println(Double.MIN_VALUE)
}
```

El código anterior mostrará sus valores máximos y mínimos.

```text
Byte
127
-128
Short
32767
-32768
Integer
2147483647
-2147483648
Long
9223372036854775807
-9223372036854775808
Float
3.4028235E38
1.4E-45
Double
1.7976931348623157E308
4.9E-324
```

Otras constantes útiles son las que indican el tamaño que ocupa cada tipo numérico en bits.
Estas constantes tienen el nombre `SIZE_BITS`.

```kotlin
fun main() {
    println(Byte.SIZE_BITS) // 8
    println(Short.SIZE_BITS) // 16
    println(Int.SIZE_BITS) // 32
    println(Long.SIZE_BITS) // 64
    println(Float.SIZE_BITS) // 32
    println(Double.SIZE_BITS) // 64
}
```
