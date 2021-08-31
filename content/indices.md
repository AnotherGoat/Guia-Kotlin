# Índices

Todos los elementos de un arreglo se almacenan secuencialmente y pueden ser accedidos mediante un índice autogenerado.
El índice del primer elemento es `0`, en lugar de `1`, como podría esperarse.
Después del índice `0` viene el `1`, luego el `2`, y así sucesivamente.

## Acceso a elementos

Se puede acceder a un determinado elemento de un arreglo escribiendo su índice entre corchetes `[]` después del nombre de este arreglo.

```kotlin
val animales = arrayOf("Perro", "Gato")

println(animales[0]) // Perro
println(animales[1]) // Gato
```

Se debe tener cuidado de no excederse del tamaño del arreglo - 1, debido a que los índices empiezan en `0`.

```kotlin
val constantes = floatArrayOf(3.14f, 2.71f)

println(constantes[2]) // Fuera del rango de índices del arreglo
```

El código anterior compilará, pero durante la ejecución se lanzará una `ArrayIndexOutOfBoundsException`.

```text
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 2
```

Es importante notar que este tipo de error se detecta sólo durante la ejecución, así que se debe tener cuidado de prevenirlo para evitar problemas mayores.
