# Variables

Las variables se utilizan para almacenar datos, con el fin de poder trabajar con ellos más tarde, reutilizarlos y modificarlos como se desee.

Cada variable tiene un tipo de dato, que define el tipo de información que contiene.

## Variables mutables

A continuación se muestran algunos ejemplos de variables, declaradas con la palabra clave var.

```kotlin
var num = 100
var saludo = "Hola"
var x = 'x'
var esPosible = true
```

El contenido a la derecha del nombre de la variable se conoce como literal.
Cada tipo de variable tiene su propia sintaxis de literal, la cual es utilizada por Kotlin para inferir su tipo.

## Reasignación de valores

Las variables mutables pueden ser pasadas como argumentos a funciones y su valor se puede reasignar durante la ejecución del programa.

Al momento de reasignar el valor de una variable no es necesario volver a utilizar la palabra var, ya que esta sólo se utiliza al momento de declararla.

```kotlin
fun main() {
    var num = 1000
    println(num)
    
    num = 9999
    println(num)
}
```

El código mostrado arriba muestra la siguiente salida:

```text
1000
9999
```

Es importante recordar que toda variable tiene un nombre que actúa como identificador.

## Variables inmutables

Además de las variables mutables, Kotlin permite la creación de variables inmutables.
Para declarar una variable inmutable es necesario usar la palabra clave val.

```kotlin
val nombre = "Juan"
println(nombre)
```

Se diferencia de las variables mutables en que su valor sólo puede ser asignado una vez.

```kotlin
fun main() {
    val decimal = 3.14
    decimal = 1.5
}
```

El codigo anterior no se podrá ejecutar ya que el compilador detectará el error y mostrará el siguiente mensaje, interrumpiendo cualquier intento de ejecución:

```text
Kotlin: Val cannot be reassigned
```

Si se quiere almacenar un dato que puede variar durante la ejecución del programa, se debe usar la palabra var, en caso contrario, se recomienda usar val.
