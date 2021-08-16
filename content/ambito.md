# Ámbito

El concepto de ámbito indica el espacio al que pertenece y desde el cual se puede hacer referencia a una variable.

## Variables locales

Generalmente, las variables definidas dentro de funciones se conocen como variables locales, como en el caso siguiente:

```kotlin
fun mostrarEdad(){
    val edad = 25
    println(edad)
}
```

La variable está definida dentro del ámbito de la función, pero no fuera de ella.
De este modo, intentar hacer lo siguiente no funcionará.

```kotlin
fun definirEdad(){
    val edad = 25
}

fun main(){
    println(edad)
}
```

El compilador no permitirá la ejecución del código anterior, ya que si bien ambas variables tienen el mismo nombre, no pertenecen el mismo ámbito.

```text
Kotlin: Unresolved reference: edad
```

## Variables globales

Las variables globales o de nivel superior son definidas fuera de cualquier bloque de código, ya sea una clase o una función.
Esto permite que sean usadas por cualquier bloque de código que esté en su mismo nivel.

```kotlin
var numero = 500

fun main(){
    println(numero)
}

fun sumar1(){
    numero++
}
```

Además, se puede sobreescribir una variable global con una local del mismo nombre que esté en un ámbito más reducido.

```kotlin
val saludo = "Hola"

fun main(){
    val saludo = "Buenos días"
    println(saludo)
}
```

El código anterior mostrará el valor almacenado en la variable local `saludo`, en vez de usar el de la variable global.

```text
Buenos días
```

## Declaraciones de nivel superior

Es importante saber que el nivel superior sólo se usa para declarar nombres y asignar valores.
Operaciones como reasignación de variables no están permitidas en este nivel.

```kotlin
var fruta = "Naranja"
fruta = "Pomelo"

fun main() {
    //
}
```

Kotlin lo indicará con un mensaje.

```text
Kotlin: Expecting a top level declaration
```
