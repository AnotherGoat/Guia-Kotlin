# Arreglos genéricos

Los arreglos básicos sólo soportan tipos de datos primitivos, pero exite una alternativa para crear arreglos de cualquier tipo.

## Creación de arreglos

Para crear arreglos de cualquier tipo se debe usar el método `arrayOf()`.

```kotlin
import java.util.Random // Importado para mostrar arreglos de cualquier clase

val animales = arrayOf("perro", "gato", "paloma")
val randoms = arrayOf(Random(), Random(), Random())
```

Es importante notar que en este caso todos los arreglos se almacenan con el tipo `Array<T>`, mientras que el genérico `T` indica el tipo de dato que almacena.
En el ejemplo anterior, `animales` es de tipo `Array<String>` y `randoms` es de tipo `Array<Random>`.

La clase `Array` no se relaciona por herencia a arreglos de tipos primitivos como `IntArray`, pero ofrece las mismas funcionalidades.
También se puede especificar el tipo de dato en el método `arrayOf()`, de la siguiente forma:

```kotlin
val arregloDeStrings = arrayOf<String>("arreglo", "de", "strings")
```
