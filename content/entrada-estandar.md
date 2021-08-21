# Entrada estándar

La entrada estándar es un flujo de datos que se envía al programa.
Por defecto, la entrada estándar recibe información desde el teclado, pero también es posible recibirla del contenido de archivos.
No todos los programas requieren entrada estándar, pero es un concepto importante.

## Lectura de líneas

Kotlin tiene una función muy útil para leer datos ingresados por el usuario.
Esta función es `readLine()`.

```kotlin
val linea = readLine()!!
```

El contenido de esta línea es leído como `String`.

```kotlin
println(readLine()!! is String)
```

Esta operación usa el operador `!!`.
Si este operador no está presente el método `readLine()` no funcionará, lo cual ocurre debido a que Kotlin protege contra el uso de valores nulos.

## Entrada y salida

Un ejemplo clásico de muestra de entrada y salida es hacer que el usuario entregue texto y luego mostrarlo en pantalla.

```kotlin
val texto = readLine()!!
println(texto)
```

Es muy común usar la entrada estándar en formularios e incluir mensajes para que el usuario sepa qué información se está pidiendo, por medio de la salida estándar.
La función `print()` puede ser útil para darle un formato más adecuado.

```kotlin
fun main() {
    println("Iniciar sesión")

    print("Usuario: ")
    val usuario = readLine()!!
    println()

    print("Contraseña: ")
    val clave = readLine()!!
    println()
}
```

El uso de `println()` en este caso es para añadir un salto de línea después de que el usuario ingrese sus datos y evitar que quede todo en la misma línea.

## Conversión de tipos

Debido a que el valor que entrega esta función es un `String`, será necesario convertirlo a otros tipos de datos en caso de que se requiera.

```kotlin
```
