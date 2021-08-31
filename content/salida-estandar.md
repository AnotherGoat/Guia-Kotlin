# Salida estándar

La salida estándar es la operación básica que muestra información en un dispositivo.
No todos los programas generan una salida de este tipo.

## Motrar texto en pantalla

Las funciones `print()` y `println()` son la forma estándar de enviar texto a la salida estándar, generalmente el terminal donde se ejecuta el programa.

```kotlin
print("Hola ")
println("mundo")
```

La salida estándar mostrará un resultado usando los valores almacenados dentro de las cadenas de texto.

```text
Hola mundo
```

La función `println()` puede ser llamada sin argumentos y sólo mostrar un salto de línea.

```kotlin
fun main() {
    print("1")
    print("2")
    println()
    print("3")
}
```

La salida estándar mostrará lo siguiente:

```kotlin
12
3
```

La función `print()` no funcionará si se llama sin argumentos.

Es importante notar que la salida estándar mostrará los resultados como texto.
Esto significa que los elementos propios de los literales, como las comillas, se eliminarán.
En el siguiente ejemplo, todas las llamadas a `println()` mostrarán lo mismo, a pesar de que se usan con un `Int`, un `Char` y un `String`.

```kotlin
println(3)
println('3')
println("3")
```
