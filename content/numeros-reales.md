# Números reales

Además del conjunto de números enteros, Kotlin permite trabajar con el conjunto de números reales.

## El tipo Double

Un número `Double` representa un número de punto flotante de doble precisión de 64 bits.
Representa la forma en la que Kotlin almacena números decimales por defecto.
Kotlin utiliza el punto `.` como separador entre la parte entera y la parte decimal.

```kotlin
val decimal = 999.5
```

Además de números decimales, el tipo `Double` permite almacenar valores como infinito y `NaN` (Not a Number).
Estos valores pueden ser accedidos desde constantes de la clase.

```kotlin
fun main() {
    println(Double.NaN)
    println(Double.POSITIVE_INFINITY)
    println(Double.NEGATIVE_INFINITY)
}
```

Estos valores se muestran de la siguiente forma:

```text
NaN
Infinity
-Infinity
```

## El tipo Float

Un número `Float` representa un número de punto flotante de precision simple de 32 bits.
Para forzar un número decimal a `Float` en vez de `Double` tan solo basta con añadir la letra `f` o `F` al final.

```kotlin
println(0.25F)
println(.5f)
```

## Notación corta

Si el número decimal empieza con `0`, este se puede omitir.

```kotlin
// Son equivalentes
val numero1 = 0.5
val numero2 = .5
```

Esta notación se asemeja a decir "punto cinco" en vez de "cero punto cinco".

## Precisión del punto flotante

Se debe tener en cuenta que los computadores [no pueden almacenar perfectamente](http://puntoflotante.org/formats/fp/) el valor de números enteros, lo cual a menudo conduce a errores.

El siguiente ejemplo da como resultado `0.30000000000000004` en vez de `0.3`.

```kotlin
print(0.1 + 0.2) // 0.30000000000000004
```

El error mostrado arriba es un error clásico de la aritmética de punto flotante.
Es un error tan conocido que incluso tiene su propio \link{}{[sitio web](https://0.30000000000000004.com).
