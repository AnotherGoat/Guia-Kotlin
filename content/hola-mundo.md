# Hola mundo

## En Kotlin

El ejemplo clásico del hola mundo en Kotlin se puede conseguir al ejecutar el siguiente código:

```kotlin
fun main() {
    println("Hola mundo")
}
```

Al ejecutarse, se mostrará el siguiente mensaje:

```text
Hola mundo
```

Todo programa escrito en Kotlin necesita una función main para funcionar, la cual retorna implícitamente una variable de tipo `Unit` y puede incluir un argumento de tipo `Array<String>`, utilizado para entregar parámetros por línea de comandos.

```kotlin
fun main(args: Array<String>) {
    println("Hola mundo")
}
```

Sin embargo, este argumento puede omitirse sin problemas si no se necesita entregar este tipo de parámetros.

La función `println()` permite mostrar en pantalla el texto que se le entrega, mediante el envío de este al flujo de salida estándar del sistema operativo.

## Comparación con Java

Como ya sabrás, Kotlin tiene una sintaxis muy parecida a la de Java y es 100% interoperable con él.
Aquí se muestra el mismo programa "Hola mundo" escrito en Java.

```java
class HolaMundoKt {
    public static void main(String[] args) {
        System.out.println("Hola mundo"); 
    }
}
```

A diferencia de Java, Kotlin no requiere la creación de una clase contenedora del método `main()`, ya que la genera automáticamente durante la ejecución del programa.
Tampoco requiere de los modificadores `public` y `static` ni de especificar el tipo de retorno `void` (el cual se convierte a `Unit` en Kotlin).

La clase antes mencionada tiene como nombre el mismo nombre del archivo .kt que contiene el código junto al sufijo `Kt`.
Por ejemplo, si el archivo se llama `HolaMundo.kt`, la clase generada se llama `HolaMundoKt`.
