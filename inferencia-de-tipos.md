# Inferencia de tipos

Kotlin infiere el tipo de dato de una variable automáticamente, utilizando una serie de reglas básicas.
Para revisar que el tipo de un dato sea el preferido, se puede usar la palabra clave is.
Todos los ejemplos mostrados a continuación muestran la palabra true en pantalla, indicando que el tipo de dato inferido es el indicado a su lado derecho.

Por defecto, todos los números que no sean excesivamente grandes son Int.
Esto incluye los números negativos.

```kotlin
println(33 is Int)
println(-25 is Int)
```

Un número más grande que un Int o un número pequeño con la letra L en su final será un Long.

```kotlin
println(33L is Long)
println(12489189918498234 is Long)
```

Todo número decimal requiere un punto como separador entre la parte entera y la parte decimal, y será inferido como Double.
Esto incluye la notación "punto cinco", que omite el cero.

```kotlin
println(0.25 is Double)
println(.5 is Double)
```

Para forzar un número decimal a Float tan solo basta con añadir la letra f o F al final.

```kotlin
println(0.25F is Float)
println(.5f is Float)
```

Las palabras clave true y false serán convertidas a Boolean.

```kotlin
println(true is Boolean)
println(false is Boolean)
```

Todo carácter escrito por sí solo entre comillas simples será un Char.
Si se escribe más de un carácter entre las comillas, no se considera como un tipo de dato válido.

```kotlin
println('M' is Char)
println('%' is Char)
```

Finalizando con los tipos básicos, cualquier cadena de caracteres escrita entre comillas dobles se considera como un String.
Lo mismo ocurre con cadenas puras.

```kotlin
println("Palabra" is String)
println("""
    Texto
""" is String)
```

# Casos más complejos

Si se utiliza un constructor, se infiere el tipo como el de la clase que intenta construir.

```kotlin
import java.util.*

fun main() {
    println(Random() is Random)
}
```

Y por último, si se utiliza una función, se infiere el tipo como el tipo de dato que retorna dicha función.

```kotlin
println(arrayOf(1, 2, 3) is Array<Int>)
println(intArrayOf(1, 2, 3) is IntArray)
```
