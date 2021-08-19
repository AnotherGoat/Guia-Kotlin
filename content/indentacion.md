# Indentación

Al momento de utilizar estructuras de control, las llaves `{}` delimitan un bloque de código interno.
Además de las llaves, se recomienda indentar la sección interna del código.
Indentar significa añadir una cierta cantidad de espacios (generalmente 4) antes de cada línea de código que esté dentro de las llaves.

## Ejemplo de indentación

En este ejemplo se muestra que las declaraciones if se pueden anidar unas dentro de otras y que cada declaración interna añade un nivel de indentación adicional.
Esto significa que la declaración if interna sólo se evalúa si la declaración if externa es válida.

```kotlin
// Nivel 0 de indentación
if (1 == 1) {
    println("Nivel 1 de indentación")

    if (2 == 2) {
        println("Nivel 2 de indentación")
    }
}
```

Algunos programadores prefieren utilizar saltos de tabulador para indentar.
Esto no se considera una buena práctica debido a que cada PC puede configurar el largo de estos saltos, lo cual causa que el código se vea distinto.

Pára evitar que esto ocurra, muchos IDEs tienen la opción "insertar espacios al presionar la tecla Tab", para insertar 4 espacios (o la cantidad que se desee) al pulsar dicha tecla.

## Indentación consistente

Se recomienda mantener la cantidad de espacios usados para cada indentación consistente, es decir, que no varíe su cantidad.
Esto es para evitar confusiones al momento de leer el código.

Se debe evitar lo que ocurre en el bloque de código de abajo.

```kotlin
// 4 espacios
if (1 == 1) {
    println("foo")
}

// 2 espacios
if (2 == 2) {
  println("bar")
}

// 8 espacios
if (3 == 3) {
        println("42")
}
```

Además, se recomienda mantener igual la indentación de un mismo nivel dentro de un mismo bloque de código, evitando casos como los del siguiente ejemplo.

```kotlin
if (10 != 20) {
    println("hola")
println("mundo")
  println("123")
}
```

Varios IDEs y editores de código contienen funciones para formatear automáticamente el código, lo cual corrige errores comunes de indentación y espaciado.
