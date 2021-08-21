# Operador ternario

Algunos lenguajes de programación poseen un operador ternario, el cual permite hacer declaraciones if de forma rápida.

## Uso en Kotlin

En el caso de Kotlin, no existe el operador ternario.
En vez de este, se usan las palabras clave `if` y `else`, las cuales pueden ser usadas en la misma línea.

```kotlin
val edad = 15
if (edad >= 18) println("Mayor de edad") else println("Menor de edad")
```

Se puede anidar junto a `else if` para introducir más condiciones.

```kotlin
val edad = 30
if (edad >= 65) println("Adulto mayor") else if (edad >= 18) println ("Adulto") else println("Menor de edad")
```

La notación de este estilo también permite introducir cada declaración en una línea separada.

```kotlin
val edad = 45

if (edad >= 65) println("Adulto mayor")
else if (edad >= 18) println ("Adulto")
else if (edad >= 12) println("Adolescente")
else if (edad >= 2) println("Niño")
else println ("Bebé")
```
