# Arreglos multidimensionales

Los arreglos que se vieron hasta ahora son de una sola dimensión, pero Kotlin permite la anidación de arreglos también.
Una forma sencilla de verlo es como un arreglo de arreglos.
Esto sirve para representar elementos en 2, 3, 4 o más dimensiones, incluso llegando a niveles inimaginables.

## Declaración

Para declarar un arreglo tan solo basta con crear un arreglo compuesto de arreglos.

```kotlin
val arreglo2D = arrayOf(
    arrayOf(1, 2, 3, 4),
    arrayOf(5, 6, 7, 8),
    arrayOf(9, 10, 11, 12)
)
```

El compilador ignora los saltos de línea y la indentación dentro de los métodos `arrayOf()`, lo que permite darle un formato para hacer más fácil su comprensión.
El ejemplo anterior se puede visualizar de la siguiente forma.

|`1`|`2`|`3`|`4`|
|-|-|-|-|
|`5`|`6`|`7`|`8`|
|`9`|`10`|`11`|`12`|

Los arreglos anidados se pueden utilizar para representar cuadrículas 2D, como por ejemplo [matrices](https://es.khanacademy.org/math/algebra-home/alg-matrices).

```kotlin
val identidad = arrayOf(
    arrayOf(1, 0, 0),
    arrayOf(0, 1, 0),
    arrayOf(0, 0, 1),
)
```

Esta estructura tipo matriz es muy conveniente en los casos en los que se necesite almacenar datos en formato tabla (fila-columna).
Una característica importante de los arreglos anidados es que no es necesario que sean del mismo tamaño.

```kotlin
val array2D = arrayOf(
    arrayOf(0), // Largo 1
    arrayOf(1, 2), // Largo 2
    arrayOf(3, 4, 5) // Largo 3
)
```

Los arreglos anidados no necesitan ser del mismo tipo.

```kotlin
val datosCuenta = arrayOf(
    arrayOf("ID", "Precio", "Cantidad"),
    arrayOf(29075, 50000, 10)
)
```

El ejemplo anterior muestra otro uso común de este tipo de arreglos: la representación de tablas.
En general, un arreglo multidimensional se puede usar para hacer mapas donde cada elemento se encuentra en `n` coordenadas.

## Acceso a elementos

Se debe tener en cuenta que cada elemento del primer arreglo es otro arreglo, por lo tanto es necesario usar 2 veces el operador `[]` para acceder a los elementos del arreglo.
Por ejemplo, se define el siguiente arreglo.

```kotlin
val anidados = arrayOf(
    arrayOf(1, 2),
    arrayOf(3),
    arrayOf(4, 5)
)
```

Para acceder a cada sub-arreglo, se haría de la siguiente forma:

```kotlin
val subArreglo1 = anidados[0] // arrayOf(1, 2)
val subArreglo2 = anidados[1] // arrayOf(3)
val subArreglo3 = anidados[2] // arrayOf(4, 5)
```

Y para acceder a cada elemento se debe usar el operador `[]` 2 veces.

```kotlin
// Sub-arreglo 1
val num1 = anidados[0][0] // 1
val num2 = anidados[0][1] // 2

// Sub-arreglo 2
val num3 = anidados[1][0] // 3

// Sub-arreglo 3
val num4 = anidados[2][0] // 4
val num5 = anidados[2][1] // 5
```

## Más de 2 dimensiones

Para crear arreglos de 3 o más dimensiones tan solo se debe repetir el mismo procedimiento que para crear arreglos 2D, pero más veces.

```kotlin
val arreglo3D = arrayOf(
    arrayOf(arrayOf(0,1), arrayOf(2,3)),
    arrayOf(arrayOf(4,5), arrayOf(6,7))
)
```

Se debe tener en cuenta que para acceder un elemento individual de este arreglo se deben especificar 3 índices.

```kotlin
println(arreglo3D[0][0][1])   // 1
println(arreglo3D[1][0][1])   // 5
println(arreglo3D[1][1][1])   // 7
```

De este modo, si un arreglo es de `n` dimensiones, para acceder a uno de sus elementos se debe proporcionar `n` índices.
Es importante tener esto en cuenta al trabajar con arreglos multidimensionales.

## Arreglos multidimensionales vacíos

Para crear arreglos multidimensionales vacíos, se debe anidar el constructor `Array` de la siguiente forma:

```kotlin
fun main() {
    val arreglo2DVacio = Array(3) { IntArray(3) }
    println("Arreglo 2D vacío:")
    println(arreglo2DVacio.contentDeepToString())

    val arreglo3DVacio = Array(3) { Array(3) { IntArray(3) } }
    println("Arreglo 3D vacío:")
    println(arreglo3DVacio.contentDeepToString())
}
```

La salida ayuda a mostrar el ejemplo de forma más comprensible.

```text
Arreglo 2D vacío:
[[0, 0, 0], [0, 0, 0], [0, 0, 0]]
Arreglo 3D vacío:
[[[0, 0, 0], [0, 0, 0], [0, 0, 0]], [[0, 0, 0], [0, 0, 0], [0, 0, 0]], [[0, 0, 0], [0, 0, 0], [0, 0, 0]]]
```
