# Operaciones con arreglos

Además de permitir el almacenamiento de datos, Kotlin también permite la realización de operaciones entre arreglos.

## Tamaño de un arreglo

Se puede obtener el tamaño (número de elementos) de un arreglo accediendo a su propiedad `size`.

```kotlin
val vocales = charArrayOf('a', 'e', 'i', 'o', 'u')
println(vocales.size) // 5
```

Los índices de un arreglo son números entre `0` (el primer elemento) y `arreglo.size - 1` (el último elemento).
De forma más cómoda, se puede acceder a la propiedad `lastIndex`, que contiene el índice del último elemento.

```kotlin
val vocales = charArrayOf('a', 'e', 'i', 'o', 'u')
println(vocales.lastIndex) // 4
```

## Reasignación de elementos

El elemento en un índice determinado de un arreglo se puede reasignar.

```kotlin
val numeros = IntArray(4)
numeros[2] = 1

print(numeros.joinToString())
```

Como se puede ver, esto se puede hacer incluso si el arreglo fue declarado con `val`, como se puede ver en la salida.

```text
0, 0, 1, 0
```

## Primer y último elemento

Kotlin provee formas convenientes de acceder el primer y último elemento de un arreglo, mediante los métodos `first()` y `last()`.

```kotlin
val alfabeto = charArrayOf('a', 'b', 'c', 'd')

println(alphabet.first()) // 'a'
println(alphabet.last()) // 'd'
```

## Comparación de arreglos

La función `contentEquals()` sirve para comparar el contenido de 2 arreglos.

```kotlin
val nums1 = intArrayOf(1, 2, 3, 4)
val nums2 = intArrayOf(1, 2, 3, 4)
val nums3 = intArrayOf(1, 2, 3)

println(nums1.contentEquals(nums2)) // true
println(nums1.contentEquals(nums3)) // false
```

Se debe tener cuidado de no usar los operadores `==` y `!=`, ya que estos comparan los punteros.

```kotlin
val arregloSimple = intArrayOf(1, 2, 3, 4)
val arregloSimilar = intArrayOf(1, 2, 3, 4)

println(arregloSimple == arregloSimple)
println(simpleArray == similarArray)
```

La salida del código anterior es la siguiente:

```text
true
false
```

Esto ocurre porque en la primera comparación ambos identificadores apuntan a la misma instancia, mientras que en la segunda, cada uno apunta a una instancia distinta.

## Conversión a String

Una forma de convertir un `Array` a `String` es utilizando el método `joinToString[]`.

```kotlin
fun main() {
    val resultados = booleanArrayOf(true, false, true)
    println(resultados.joinToString())
}
```

La salida se mostrará con el separador `, ` (una coma seguida de un espacio en blanco).

```kotlin
true, false, true
```

Alternativamente, se le puede entregar un separador personalizado.

```kotlin
fun main() {
    val resultados = booleanArrayOf(true, false, true)
    println(resultados.joinToString(" -- "))
}
```

En este caso, el resultado se mostrará con el nuevo separador.

```kotlin
true -- false -- true
```
