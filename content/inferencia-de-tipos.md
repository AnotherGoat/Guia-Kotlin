# Inferencia de tipos

Kotlin infiere el tipo de dato de una variable automáticamente, utilizando una serie de reglas básicas.
Para revisar que el tipo de un dato sea el preferido, se puede usar la palabra clave `is`.

Todos los ejemplos mostrados a continuación muestran la palabra `true` en pantalla, indicando que el tipo de dato inferido es el indicado a su lado derecho.

## Int

Por defecto, todos los números que no sean excesivamente grandes son `Int`.
Esto incluye los números negativos y el `0`.

```kotlin
println(33 is Int)
println(-25 is Int)
```

## Long

Un número más grande que un `Int` o un número pequeño con la letra `L` en su final será un `Long`.

```kotlin
println(33L is Long)
println(12489189918498234 is Long)
```

## Double

Todo número decimal requiere un punto `.` como separador entre la parte entera y la parte decimal, y será inferido como `Double`.

```kotlin
println(1.25 is Double)
println(.5 is Double)
```

Si el número decimal empieza con `0`, este se puede omitir, haciendo que

```kotlin

```

## Float

Para forzar un número decimal a Float tan solo basta con añadir la letra f o F al final.

```kotlin
println(0.25F is Float)
println(.5f is Float)
```

## Boolean

Las palabras reservadas true y false serán convertidas a Boolean.

```kotlin
println(true is Boolean)
println(false is Boolean)
```

## Char

Todo carácter escrito por sí solo entre comillas simples será un Char.
Si se escribe más de un carácter entre las comillas, no se considera como un tipo de dato válido.

```kotlin
println('M' is Char)
println('%' is Char)
```

## String

Finalizando con los tipos básicos, cualquier cadena de caracteres escrita entre comillas dobles se considera como un `String`.
Lo mismo ocurre con cadenas puras.

```kotlin
println("Palabra" is String)
println("""
    Texto
""" is String)
```

## Constructores

Si se utiliza un constructor, se infiere el tipo como el de la clase que intenta construir.

```kotlin
import java.util.*

fun main() {
    println(Random() is Random)
}
```

## Métodos

Si se utiliza una función, se infiere el tipo como el tipo de dato que retorna dicha función.

```kotlin
println(arrayOf(1, 2, 3) is Array<Int>)
println(intArrayOf(1, 2, 3) is IntArray)
```

## Forzado de inferencia

Se puede "forzar" el tipo de una variable al especificado, en vez de dejar que Kotlin lo infiera automáticamente.
Esta acción se puede realizar al momento de declarar y asignar una variable.

```kotlin
val num1: Byte = 8
val num2: Short = 8
val num3: Int = 8
```

En el caso anterior, cada una de las 3 variables es de un tipo diferente, a pesar de haber sido declarada con el mismo valor en el lado derecho.
En ocasiones, indicar el tipo al declarar y asignar una variable puede ser de utilidad para el programador.
