# Arreglos primitivos

Los arreglos son la estructura de datos más básica y una de las más usadas en Kotlin.
Son colecciones ordenadas posicionalmente de objetos del mismo tipo y son de tamaño fijo.

El nombre "arreglo" proviene de [un error de traducción](https://es.stackoverflow.com/questions/234718/cu%C3%A1l-es-la-traducci%C3%B3n-al-espa%C3%B1ol-correcta-del-t%C3%A9rmino-array) de la palabra "array" del inglés.
La traducción más adecuada sería "formación", pero aquí se identificaran como arreglos debido a que es su traducción más popular.

## Creación de arreglos

Para crear un arreglo de un tipo de dato primitivo se debe usar uno de los tipos de datos primitivos.

```kotlin
val primos = intArrayOf(2, 3, 5, 7, 11)
```

La siguiente tabla muestra las funciones que se deben usar para cada tipo de dato.

|Tipo de dato original|Función|Tipo de arreglo|
|-|-|-|
|`Byte`|`byteArrayOf()`|`ByteArray`|
|`Short`|`shortArrayOf()`|`ShortArray`|
|`Int`|`intArrayOf()`|`IntArray`|
|`Long`|`longArrayOf()`|`LongArray`|
|`Float`|`floatArrayOf()`|`FloatArray`|
|`Double`|`doubleArrayOf()`|`DoubleArray`|
|`Boolean`|`booleanArrayOf()`|`BooleanArray`|
|`Char`|`charArrayOf()`|`CharArray`|

Es importante notar que el tipo `StringArray` no existe, debido a que `String` no es un tipo primitivo.

## Comas sobrantes

Se puede dejar una coma sobrante dentro de la creación de un arreglo (o cualquier otra cosa que use una secuencia de argumentos).
Esta práctica puede ser de utilidad si se quieren añadir o modificar valores del arreglo original.

```kotlin
val primos = intArrayOf(2, 3, 5, 7, 11,) // Coma sobrante
```
