# Declaraciones if

Las declaraciones if son una estructura de control que sirve para ejecutar código dependiendo de la evaluación de determinadas condiciones.

## La declaración if

Para hacer una declaración if, se utiliza la palabra clave `if`.
Si la expresión dentro de ella se evalúa como `true`, se lleva a cabo el bloque de código que le sigue.
En caso contrario, no ocurre nada.


```kotlin
if (3 > 2) {
    print("3 es mayor que 2")
}
```

## Declaración else

Las declaraciones else pueden escribirse después de declaraciones if.
El código dentro de ellas sólo se ejecuta cuando la condición de la delaración if anterior no se cumple.

```kotlin
fun main() {
    val x = 5
    val y = 6

    if (x > y) {
        print("$x es mayor que $y")
    } else {
        print("$y es mayor que $x")
    }
}
```

## Declaración else-if

Entre una declaración if y una declaración se puede introducir cualquier número de declaraciones else-if.
Una declaración else-if introduce una nueva condición, la cual sólo se revisa si las condiciones de los bloques if anteriores se evalúan como `false`.

```kotlin
fun main() {
    val numero = 0

    if (numero > 0) {
        println("Positivo")
    } else if (numero == 0) {
        println("Neutro")
    } else {
        println("Negativo")
    }

    // Continua aquí
}
```

El programa irá evaluando cada expresión una por una hasta que alguna se cumpla.
Cuando esto ocurra, ejecutará las instrucciones en su bloque de código y continuará con las expresiones después del final bloque else.
