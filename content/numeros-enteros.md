# Números enteros

El tipo de dato más básico en Kotlin son los números enteros.
Estos son equivalentes a los números enteros en las matemáticas.

## El tipo Int

Los números enteros se utilizan para contar cosas en el mundo real, y uno de sus usos más comunes es el tipo de dato `Int`.

Un número entero se representa como cualquier número que no tiene parte decimal ni comillas.

```kotlin
val numero = 123
val numeroNegativo = -100
```

Se pueden utilizar guiones bajos `_` para separar dígitos en caso de escribir números muy grandes.

```kotlin
val numero = 1_000_000
```

De hecho, estos guiones bajos pueden estar en cualquier lugar que no sea los extremos del número.

```kotlin
val numero = 1_2_3
```

A continuación se muestra un ejemplo de uso incorrecto de `_` como separador.

```kotlin
val numero = _123_
```

La respuesta de Kotlin frente a este caso es la que se indica abajo.

```text
Kotlin: Unresolved reference: _123_
```

## El tipo Long

En ocasiones se necesita almacenar números de mayor longitud.
Para estos casos el tipo de dato más conveniente es `Long`.

```kotlin
val numero = 999_999_999_999_999_999
```

Kotlin detectará automáticamente que un número es `Long` si es más grande que el valor máximo que puede almacenar un `Int`.
Se puede forzar el almacenamiento de un número pequeño como un `Long` si se pone una `L` al final del número o si se indica su tipo.

```kotlin
val numero = 123L
val otroNumero: Long = 456
```

## Los tipos Byte y Short

En caso de almacenar números pequeños, se puede optar por usar los tipos de dato `Byte` y `Short`.
Estos tipos de dato ocupan menos espacio que un `Int` y por ese motivo tienen un rango de valores menor.

Para asignar valores a variables de estos tipos es necesario especificar explícitamente sus tipos, ya que en caso contrario Kotlin los tomará como `Int`.

```kotlin
val byte: Byte = 123
val short: Short = 123
```

Debido a la poca cantidad de valores que pueden almacenar, estos tipos de dato sólo son utilizados en casos particulares.
