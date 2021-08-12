# Hola mundo

El ejemplo clásico del hola mundo en Kotlin se puede conseguir al ejecutar el siguiente código:

```kotlin
fun main() {
    println("Hola mundo")
}
```

Al ejecutarse, se mostrará el siguiente mensaje:

```
Hola mundo
```

Todo programa escrito en Kotlin necesita una función main para funcionar; la cual retorna implícitamente una variable de tipo Unit y puede incluir un argumento de tipo String utilizado para entregar parámetros por línea de comandos.

```kotlin
fun main(args: Array<String>) {
    println("Hola mundo")
}
```

Sin embargo, este argumento puede omitirse perfectamente si no se necesita entregar este tipo de parámetros.

La función println() permite mostrar en pantalla el texto que se le entrega entre comillas dobles, mediante el envío del mensaje al flujo de salida estándar del sistema operativo.

# Comparación con Java

Como ya sabrás, Kotlin es 100% interoperable con Java.
Aquí se muestra el mismo programa escrito en Java.

```java
class HolaMundoKt {
    public static void main(String[] args) {
        System.out.println("Hola mundo"); 
    }
}
```

A diferencia de Java, Kotlin no requiere la creación de una clase contenedora del método main, ya que la genera automáticamente durante la ejecución del programa.
Dicha clase tiene como nombre el nombre del archivo .kt pero reemplazando la extensión por el sufijo Kt.

# Punto y coma

En Kotlin finalizar las sentencias con un punto y coma (;) es opcional, al contrario de otros lenguajes de programación como Java, C++ o C#.
Ambos ejemplos mostrados a continuación son válidos.



Sin embargo, se puede utilizar en medio
