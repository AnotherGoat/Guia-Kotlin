# Arreglos vacíos

En ocasiones se quiere inicializar un arreglo y llenar sus valores después.
Para esos casos Kotlin permite la creación de arreglos con valores predefinidos.

## Inicialización

Para inicializar un arreglo "vacío", se debe usar el constructor en vez de un método, como en los siguientes ejemplos:

```kotlin
val numbers = IntArray(5) // Arreglo de 5 Integer
println(numbers.joinToString())

val doubles = DoubleArray(7) // Arreglo de 7 Double
println(doubles.joinToString())
```

El número que se le entrega al constructor es la cantidad de elementos que tendrá el arreglo.
También se usa el método `joinToString()` para mostrar el contenido de cada arreglo.

```text
0, 0, 0, 0, 0
0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0
```

El tamaño de un arreglo no puede cambiar, pero sí se pueden modificar sus elementos.

## Valores por defecto

Debido a que Kotlin está enfocado a proteger al programador del uso de valores nulos, cada tipo de dato se inicializa con un valor no nulo.
La siguiente tabla muestra los valores por defecto de cada constructor:

|Constructor|Valor por defecto|
|-|-|
|`ByteArray()`|`0`|
|`ShortArray()`|`0`|
|`IntArray()`|`0`|
|`LongArray()`|`0L`|
|`FloatArray()`|`0.0f`|
|`DoubleArray()`|`0.0`|
|`BooleanArray()`|`false`|
|`CharArray()`|`` (Carácter vacío)|

En general, los tipos numéricos toman el valor `0` y los otros tipos toman valores vacíos pero no nulos.

## Arreglos genéricos vacíos

Un arreglo de clase `Array` vacío se puede construir para llenar su contenido después, mediante el método `emptyArray()`.
Para hacer esta operación es necesario especificar su tipo.

```kotlin
val arregloVacio = emptyArray<String>()
```
