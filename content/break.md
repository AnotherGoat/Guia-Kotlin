# Declaración break

La declaración break se usa para finalizar un bucle prematuramente.

## Uso en bucle while

Para finalizar un bucle se debe usar la palabra clave `break`.
Cuando el flujo de ejecución del programa llegue a la línea que contiene `break`, su ejecución terminará.

```kotlin
var i = 0

while (true) {
    println(i)
    i++

    if (i >= 5) {
        print("fin")
        break
    }
}
```

El ejemplo anterior mostrará la siguiente salida:

```text
0
1
2
3
4
fin
```

## Uso en bucle do-while

## Uso en bucle for
