# Declaración continue

La declaración continue se usa para finalizar la iteración actual de un bucle y pasar a la siguiente.

## Uso en bucle while

Cuando el flujo de ejecución del programa llegue a la línea que contiene `continue`, saltará a la próxima iteración.

```kotlin
var i = 0

while (i < 7) {
    i++

    if (i == 4) {
        continue // Omite el número 4
    }

    println(i)
}
```

El ejemplo anterior mostrará la siguiente salida:

```text
1
2
3
5
6
7
```

## Uso en bucle do-while

## Uso en bucle for
