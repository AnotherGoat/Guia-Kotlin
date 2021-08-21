# Precedencia de operadores

En Kotlin, todas las operaciones siguen un orden adecuado.
En el caso de operadores aritméticos, las operaciones siguen el orden definido por [la regla PEMDAS](https://byjus.com/maths/pemdas/).

## La regla PEMDAS

La regla usada por Kotlin es muy similar a PEMDAS, pero sin contar la exponenciación debido a que no es una operación básica:

- Paréntesis `()`
- Multiplicación `*` y división `/` (de izquierda a derecha)
- Adición `+` y Sustracción `-` (de izquierda a derecha)

A continuación se muestra un ejemplo del orden en el que se procesan las operaciones.

```kotlin
print(2*7 - 1 + 4/2*3)
// 2*7 - 1 + 4/2*3
// 14 - 1 + 6
// 19
```

## Paréntesis

Se pueden usar paréntesis `()` para agrupar operaciones y hacer que estas se realicen primero, siguiendo la regla PEMDAS.
El uso de paréntesis en Kotlin es exactamente igual a su uso en las matemáticas.
}

```kotlin
print((2 + 3) * 4 / (10 - 5))
// (2 + 3) * 4 / (10 - 5)
// 5 * 4 / 5
// 4
```

Arriba se muestra un ejemplo básico de uso de paréntesis y del orden en el que se procesa.
