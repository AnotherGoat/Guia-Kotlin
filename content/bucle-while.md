# Bucle while

Un bucle while se usa para repetir un bloque de código varias veces, siempre que se cumpla cierta condición.
Generalmente se usan con una variable como contador.

## Declaración

Para declarar un bucle while se debe usar la palabra clave `while`.
También es necesario inicializar un contador en una variable.

```kotlin
var i = 1 // contador

while (i <= 5) {
    println(i)
    i = i + 1
}
```

El código en el cuerpo de un bucle se ejecuta repetidamente.
Esta operación se llama iteración.
En la salida se muestran los números del 1 al 5, ya que el contador inicia en 1 y aumenta hasta llegar a 5, ya que después de tener ese valor se deja de cumplir la condición `i <= 5`.

```text
1
2
3
4
5
```

Se puede realizar cualquier operación con el contador dentro del bucle.

```kotlin
// Ejemplo con multiplicación
val i = 2

while (i <= 100) {
    println(i)
    i *= 2
}

// Ejemplo con división
val j = 1000

while (j >= 2) {
    println(j)
    j /= 2
}
```

Los contadores generalmente tienen identificadores de una sola letra empezando por `i`, `j`, `k`, etc.

## Bucle infinito

Si la condición a evaluar es siempre verdadera, el bucle se ejecutará indefinidamente. Esto se llama bucle infinito.

```kotlin
var i = 1

while (true) {
    println(i)
    i++
}
```

La única forma de detener este bucle es deteniendo la ejecución del programa.
